---
title: FormBuildActionPaneTabControl クラス
description: このトピックでは、FormBuildActionPaneTabControl クラスについて説明します。
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
ms.openlocfilehash: 9a623622e31bbb71e08741c88df20f30fccd62e3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502658"
---
# <a name="class-formbuildactionpanetabcontrol"></a><span data-ttu-id="6956e-103">クラス FormBuildActionPaneTabControl</span><span class="sxs-lookup"><span data-stu-id="6956e-103">Class FormBuildActionPaneTabControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildActionPaneTabControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="6956e-104">備考</span><span class="sxs-lookup"><span data-stu-id="6956e-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="6956e-105">例</span><span class="sxs-lookup"><span data-stu-id="6956e-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6956e-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="6956e-106">Methods</span></span>

| <span data-ttu-id="6956e-107">方法</span><span class="sxs-lookup"><span data-stu-id="6956e-107">Method</span></span>                                                                                                      | <span data-ttu-id="6956e-108">説明</span><span class="sxs-lookup"><span data-stu-id="6956e-108">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6956e-109">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-109">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="6956e-110">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-110">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                               |
| <span data-ttu-id="6956e-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="6956e-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-112">Determines whether to align the control.</span></span>                                                                                                      |
| <span data-ttu-id="6956e-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="6956e-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-114">Determines whether the user can change the contents of the control.</span></span>                                                                           |
| <span data-ttu-id="6956e-115">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-115">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6956e-116">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-116">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6956e-117">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-117">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6956e-118">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-118">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="6956e-119">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-119">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="6956e-120">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-120">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="6956e-121">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-121">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="6956e-122">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-122">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                               |
| <span data-ttu-id="6956e-123">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-123">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6956e-124">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-124">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="6956e-125">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-125">Gets or set the caption of the control.</span></span>                                                                                                       |
| <span data-ttu-id="6956e-126">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-126">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                     |                                                                                                                                               |
| <span data-ttu-id="6956e-127">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-127">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                        |                                                                                                                                               |
| <span data-ttu-id="6956e-128">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-128">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="6956e-129">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-129">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                               |
| <span data-ttu-id="6956e-130">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-130">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6956e-131">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-131">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6956e-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="6956e-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="6956e-134">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="6956e-134">public int containerId()</span></span>                                                                                    | <span data-ttu-id="6956e-135">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6956e-135">Retrieves the ID of the parent container for the control.</span></span>                                                                                     |
| <span data-ttu-id="6956e-136">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-136">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="6956e-137">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-137">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                               |
| <span data-ttu-id="6956e-138">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-138">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6956e-139">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-139">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="6956e-140">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-140">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                      |
| <span data-ttu-id="6956e-141">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-141">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6956e-142">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-142">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="6956e-143">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-143">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                             |
| <span data-ttu-id="6956e-144">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-144">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="6956e-145">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-145">Determines whether to enable or disable the object.</span></span>                                                                                           |
| <span data-ttu-id="6956e-146">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-146">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="6956e-147">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-147">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="6956e-148">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-148">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="6956e-149">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-149">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="6956e-150">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-150">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="6956e-151">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-151">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="6956e-152">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-152">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="6956e-153">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-153">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="6956e-154">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-154">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="6956e-155">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-155">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6956e-156">public int id()</span><span class="sxs-lookup"><span data-stu-id="6956e-156">public int id()</span></span>                                                                                             | <span data-ttu-id="6956e-157">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6956e-157">Retrieves the ID of the control.</span></span>                                                                                                              |
| <span data-ttu-id="6956e-158">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-158">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6956e-159">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="6956e-159">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="6956e-160">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6956e-160">Retrieves a value that indicates whether the control is a container control.</span></span>                                                                  |
| <span data-ttu-id="6956e-161">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-161">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                               |
| <span data-ttu-id="6956e-162">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-162">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6956e-163">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-163">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                               |
| <span data-ttu-id="6956e-164">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-164">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="6956e-165">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-165">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6956e-166">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-166">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6956e-167">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-167">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6956e-168">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="6956e-168">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="6956e-169">コントロールに ID で指定されているコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="6956e-169">Moves a control that is specified by ID to the control.</span></span>                                                                                       |
| <span data-ttu-id="6956e-170">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-170">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="6956e-171">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-171">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="6956e-172">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-172">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6956e-173">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-173">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="6956e-174">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-174">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6956e-175">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-175">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="6956e-176">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-176">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                               |
| <span data-ttu-id="6956e-177">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-177">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6956e-178">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-178">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="6956e-179">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-179">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6956e-180">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-180">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6956e-181">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-181">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="6956e-182">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-182">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                               |
| <span data-ttu-id="6956e-183">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-183">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6956e-184">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-184">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="6956e-185">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-185">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6956e-186">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-186">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="6956e-187">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-187">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6956e-188">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-188">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6956e-189">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-189">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6956e-190">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-190">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                               |
| <span data-ttu-id="6956e-191">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-191">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                               |
| <span data-ttu-id="6956e-192">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-192">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="6956e-193">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-193">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="6956e-194">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-194">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6956e-195">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6956e-195">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="6956e-196">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-196">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="6956e-197">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-197">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="6956e-198">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-198">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="6956e-199">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6956e-199">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="6956e-200">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-200">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="6956e-201">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="6956e-201">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                               |

## <a name="method-alignchild"></a><span data-ttu-id="6956e-202">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="6956e-202">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="6956e-203">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="6956e-203">Parameters - alignChild</span></span>

<span data-ttu-id="6956e-204">値</span><span class="sxs-lookup"><span data-stu-id="6956e-204">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="6956e-205">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="6956e-205">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="6956e-206">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="6956e-206">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="6956e-207">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="6956e-207">Parameters - alignChildren</span></span>

<span data-ttu-id="6956e-208">値</span><span class="sxs-lookup"><span data-stu-id="6956e-208">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="6956e-209">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="6956e-209">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="6956e-210">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="6956e-210">Method alignControl</span></span>

<span data-ttu-id="6956e-211">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-211">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="6956e-212">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="6956e-212">Parameters - alignControl</span></span>

<span data-ttu-id="6956e-213">値</span><span class="sxs-lookup"><span data-stu-id="6956e-213">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="6956e-214">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6956e-214">Return Value - alignControl</span></span>

<span data-ttu-id="6956e-215">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6956e-215">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="6956e-216">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6956e-216">Remarks - alignControl</span></span>

<span data-ttu-id="6956e-217">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-217">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="6956e-218">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="6956e-218">Method allowEdit</span></span>

<span data-ttu-id="6956e-219">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-219">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="6956e-220">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6956e-220">Parameters - allowEdit</span></span>

<span data-ttu-id="6956e-221">値</span><span class="sxs-lookup"><span data-stu-id="6956e-221">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="6956e-222">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6956e-222">Return Value - allowEdit</span></span>

<span data-ttu-id="6956e-223">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6956e-223">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="6956e-224">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6956e-224">Remarks - allowEdit</span></span>

<span data-ttu-id="6956e-225">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="6956e-225">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="6956e-226">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="6956e-226">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="6956e-227">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="6956e-227">Parameters - allowUserSetup</span></span>

<span data-ttu-id="6956e-228">値</span><span class="sxs-lookup"><span data-stu-id="6956e-228">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="6956e-229">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="6956e-229">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="6956e-230">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="6956e-230">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="6956e-231">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="6956e-231">Parameters - arrangeGuide</span></span>

<span data-ttu-id="6956e-232">値</span><span class="sxs-lookup"><span data-stu-id="6956e-232">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="6956e-233">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="6956e-233">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="6956e-234">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="6956e-234">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="6956e-235">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="6956e-235">Parameters - arrangeMethod</span></span>

<span data-ttu-id="6956e-236">値</span><span class="sxs-lookup"><span data-stu-id="6956e-236">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="6956e-237">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="6956e-237">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="6956e-238">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="6956e-238">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="6956e-239">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="6956e-239">Parameters - arrangeWhen</span></span>

<span data-ttu-id="6956e-240">値</span><span class="sxs-lookup"><span data-stu-id="6956e-240">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="6956e-241">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="6956e-241">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="6956e-242">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6956e-242">Method autoDeclaration</span></span>

<span data-ttu-id="6956e-243">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-243">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="6956e-244">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6956e-244">Parameters - autoDeclaration</span></span>

<span data-ttu-id="6956e-245">値</span><span class="sxs-lookup"><span data-stu-id="6956e-245">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="6956e-246">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6956e-246">Return Value - autoDeclaration</span></span>

<span data-ttu-id="6956e-247">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6956e-247">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="6956e-248">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6956e-248">Remarks - autoDeclaration</span></span>

<span data-ttu-id="6956e-249">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="6956e-249">Controls cannot have identical names.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="6956e-250">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-250">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="6956e-251">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-251">Parameters - bottomMargin</span></span>

<span data-ttu-id="6956e-252">値</span><span class="sxs-lookup"><span data-stu-id="6956e-252">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-253">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-253">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="6956e-254">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-254">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="6956e-255">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-255">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="6956e-256">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-256">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="6956e-257">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-257">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="6956e-258">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-258">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="6956e-259">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-259">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="6956e-260">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-260">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="6956e-261">値</span><span class="sxs-lookup"><span data-stu-id="6956e-261">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="6956e-262">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-262">Return Value - bottomMarginValue</span></span>

## <a name="method-caption"></a><span data-ttu-id="6956e-263">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="6956e-263">Method caption</span></span>

<span data-ttu-id="6956e-264">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-264">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="6956e-265">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="6956e-265">Parameters - caption</span></span>

<span data-ttu-id="6956e-266">値</span><span class="sxs-lookup"><span data-stu-id="6956e-266">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="6956e-267">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="6956e-267">Return Value - caption</span></span>

<span data-ttu-id="6956e-268">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="6956e-268">The string that is used as the caption of the control.</span></span>

## <a name="method-columns"></a><span data-ttu-id="6956e-269">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="6956e-269">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="6956e-270">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="6956e-270">Parameters - columns</span></span>

<span data-ttu-id="6956e-271">値</span><span class="sxs-lookup"><span data-stu-id="6956e-271">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-272">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-272">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="6956e-273">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="6956e-273">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="6956e-274">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="6956e-274">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="6956e-275">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="6956e-275">Parameters - columnsMode</span></span>

<span data-ttu-id="6956e-276">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-276">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="6956e-277">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="6956e-277">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="6956e-278">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="6956e-278">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="6956e-279">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="6956e-279">Parameters - columnspace</span></span>

<span data-ttu-id="6956e-280">値</span><span class="sxs-lookup"><span data-stu-id="6956e-280">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-281">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-281">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="6956e-282">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="6956e-282">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="6956e-283">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="6956e-283">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="6956e-284">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="6956e-284">Parameters - columnspaceMode</span></span>

<span data-ttu-id="6956e-285">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-285">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="6956e-286">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="6956e-286">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="6956e-287">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="6956e-287">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="6956e-288">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="6956e-288">Parameters - columnspaceValue</span></span>

<span data-ttu-id="6956e-289">値</span><span class="sxs-lookup"><span data-stu-id="6956e-289">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="6956e-290">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="6956e-290">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="6956e-291">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="6956e-291">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="6956e-292">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="6956e-292">Parameters - columnsValue</span></span>

<span data-ttu-id="6956e-293">値</span><span class="sxs-lookup"><span data-stu-id="6956e-293">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="6956e-294">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="6956e-294">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="6956e-295">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="6956e-295">Method configurationKey</span></span>

<span data-ttu-id="6956e-296">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-296">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="6956e-297">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6956e-297">Parameters - configurationKey</span></span>

<span data-ttu-id="6956e-298">値</span><span class="sxs-lookup"><span data-stu-id="6956e-298">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="6956e-299">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6956e-299">Return Value - configurationKey</span></span>

<span data-ttu-id="6956e-300">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="6956e-300">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="6956e-301">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6956e-301">Remarks - configurationKey</span></span>

<span data-ttu-id="6956e-302">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-302">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="6956e-303">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="6956e-303">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="6956e-304">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="6956e-304">Method containerId</span></span>

<span data-ttu-id="6956e-305">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6956e-305">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="6956e-306">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="6956e-306">Return Value - containerId</span></span>

<span data-ttu-id="6956e-307">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="6956e-307">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="6956e-308">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6956e-308">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="6956e-309">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6956e-309">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="6956e-310">値</span><span class="sxs-lookup"><span data-stu-id="6956e-310">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="6956e-311">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6956e-311">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="6956e-312">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6956e-312">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="6956e-313">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6956e-313">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="6956e-314">値</span><span class="sxs-lookup"><span data-stu-id="6956e-314">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="6956e-315">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6956e-315">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="6956e-316">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6956e-316">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="6956e-317">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6956e-317">Parameters - dataRelationPath</span></span>

<span data-ttu-id="6956e-318">値</span><span class="sxs-lookup"><span data-stu-id="6956e-318">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="6956e-319">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6956e-319">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="6956e-320">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="6956e-320">Method dataSource</span></span>

<span data-ttu-id="6956e-321">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-321">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="6956e-322">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="6956e-322">Parameters - dataSource</span></span>

<span data-ttu-id="6956e-323">値</span><span class="sxs-lookup"><span data-stu-id="6956e-323">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="6956e-324">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="6956e-324">Return Value - dataSource</span></span>

<span data-ttu-id="6956e-325">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="6956e-325">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="6956e-326">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="6956e-326">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="6956e-327">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6956e-327">Parameters - displayTarget</span></span>

<span data-ttu-id="6956e-328">値</span><span class="sxs-lookup"><span data-stu-id="6956e-328">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="6956e-329">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6956e-329">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="6956e-330">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="6956e-330">Method dragDrop</span></span>

<span data-ttu-id="6956e-331">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-331">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="6956e-332">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6956e-332">Parameters - dragDrop</span></span>

<span data-ttu-id="6956e-333">値</span><span class="sxs-lookup"><span data-stu-id="6956e-333">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="6956e-334">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6956e-334">Return Value - dragDrop</span></span>

<span data-ttu-id="6956e-335">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="6956e-335">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="6956e-336">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="6956e-336">Method enabled</span></span>

<span data-ttu-id="6956e-337">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-337">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="6956e-338">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="6956e-338">Parameters - enabled</span></span>

<span data-ttu-id="6956e-339">値</span><span class="sxs-lookup"><span data-stu-id="6956e-339">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="6956e-340">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="6956e-340">Return Value - enabled</span></span>

<span data-ttu-id="6956e-341">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6956e-341">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="6956e-342">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="6956e-342">Remarks - enabled</span></span>

<span data-ttu-id="6956e-343">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="6956e-343">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="6956e-344">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6956e-344">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="6956e-345">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6956e-345">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="6956e-346">メソッド height</span><span class="sxs-lookup"><span data-stu-id="6956e-346">Method height</span></span>

<span data-ttu-id="6956e-347">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-347">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="6956e-348">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="6956e-348">Parameters - height</span></span>

<span data-ttu-id="6956e-349">値</span><span class="sxs-lookup"><span data-stu-id="6956e-349">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-350">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-350">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="6956e-351">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="6956e-351">Return Value - height</span></span>

<span data-ttu-id="6956e-352">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="6956e-352">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="6956e-353">備考 - height</span><span class="sxs-lookup"><span data-stu-id="6956e-353">Remarks - height</span></span>

<span data-ttu-id="6956e-354">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-354">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6956e-355">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="6956e-355">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="6956e-356">モード。</span><span class="sxs-lookup"><span data-stu-id="6956e-356">Mode.</span></span>            | <span data-ttu-id="6956e-357">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="6956e-357">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6956e-358">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="6956e-358">-1 Exact.</span></span>        | <span data-ttu-id="6956e-359">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-359">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6956e-360">0 自動。</span><span class="sxs-lookup"><span data-stu-id="6956e-360">0 Auto.</span></span>          | <span data-ttu-id="6956e-361">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-361">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6956e-362">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="6956e-362">1 Column height.</span></span> | <span data-ttu-id="6956e-363">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6956e-363">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="6956e-364">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6956e-364">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="6956e-365">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="6956e-365">Method heightMode</span></span>

<span data-ttu-id="6956e-366">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-366">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="6956e-367">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="6956e-367">Parameters - heightMode</span></span>

<span data-ttu-id="6956e-368">値</span><span class="sxs-lookup"><span data-stu-id="6956e-368">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="6956e-369">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6956e-369">Return Value - heightMode</span></span>

<span data-ttu-id="6956e-370">計算モード。</span><span class="sxs-lookup"><span data-stu-id="6956e-370">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="6956e-371">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6956e-371">Remarks - heightMode</span></span>

<span data-ttu-id="6956e-372">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="6956e-372">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="6956e-373">モード。</span><span class="sxs-lookup"><span data-stu-id="6956e-373">Mode.</span></span>          | <span data-ttu-id="6956e-374">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="6956e-374">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6956e-375">正確。</span><span class="sxs-lookup"><span data-stu-id="6956e-375">Exact.</span></span>         | <span data-ttu-id="6956e-376">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-376">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6956e-377">自動。</span><span class="sxs-lookup"><span data-stu-id="6956e-377">Auto.</span></span>          | <span data-ttu-id="6956e-378">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-378">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6956e-379">列の高さ</span><span class="sxs-lookup"><span data-stu-id="6956e-379">Column height.</span></span> | <span data-ttu-id="6956e-380">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6956e-380">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="6956e-381">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6956e-381">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="6956e-382">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="6956e-382">Method heightValue</span></span>

<span data-ttu-id="6956e-383">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-383">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="6956e-384">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="6956e-384">Parameters - heightValue</span></span>

<span data-ttu-id="6956e-385">値</span><span class="sxs-lookup"><span data-stu-id="6956e-385">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="6956e-386">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6956e-386">Return Value - heightValue</span></span>

<span data-ttu-id="6956e-387">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="6956e-387">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="6956e-388">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6956e-388">Remarks - heightValue</span></span>

<span data-ttu-id="6956e-389">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="6956e-389">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="6956e-390">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="6956e-390">Method helpText</span></span>

<span data-ttu-id="6956e-391">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-391">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="6956e-392">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="6956e-392">Parameters - helpText</span></span>

<span data-ttu-id="6956e-393">値</span><span class="sxs-lookup"><span data-stu-id="6956e-393">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="6956e-394">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="6956e-394">Return Value - helpText</span></span>

<span data-ttu-id="6956e-395">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="6956e-395">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="6956e-396">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="6956e-396">Remarks - helpText</span></span>

<span data-ttu-id="6956e-397">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-397">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="6956e-398">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="6956e-398">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="6956e-399">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="6956e-399">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="6956e-400">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="6956e-400">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="6956e-401">値</span><span class="sxs-lookup"><span data-stu-id="6956e-401">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="6956e-402">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="6956e-402">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="6956e-403">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6956e-403">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="6956e-404">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6956e-404">Parameters - hierarchyParent</span></span>

<span data-ttu-id="6956e-405">値</span><span class="sxs-lookup"><span data-stu-id="6956e-405">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="6956e-406">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6956e-406">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="6956e-407">メソッド id</span><span class="sxs-lookup"><span data-stu-id="6956e-407">Method id</span></span>

<span data-ttu-id="6956e-408">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6956e-408">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="6956e-409">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="6956e-409">Return Value - id</span></span>

<span data-ttu-id="6956e-410">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="6956e-410">The ID of the control.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="6956e-411">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="6956e-411">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="6956e-412">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="6956e-412">Parameters - imageLocation</span></span>

<span data-ttu-id="6956e-413">値</span><span class="sxs-lookup"><span data-stu-id="6956e-413">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="6956e-414">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="6956e-414">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="6956e-415">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="6956e-415">Method isContainer</span></span>

<span data-ttu-id="6956e-416">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6956e-416">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="6956e-417">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="6956e-417">Return Value - isContainer</span></span>

<span data-ttu-id="6956e-418">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6956e-418">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-keytip"></a><span data-ttu-id="6956e-419">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="6956e-419">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="6956e-420">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="6956e-420">Parameters - keyTip</span></span>

<span data-ttu-id="6956e-421">値</span><span class="sxs-lookup"><span data-stu-id="6956e-421">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="6956e-422">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="6956e-422">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="6956e-423">メソッド left</span><span class="sxs-lookup"><span data-stu-id="6956e-423">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="6956e-424">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="6956e-424">Parameters - left</span></span>

<span data-ttu-id="6956e-425">値</span><span class="sxs-lookup"><span data-stu-id="6956e-425">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-426">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-426">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="6956e-427">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="6956e-427">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="6956e-428">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-428">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="6956e-429">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-429">Parameters - leftMargin</span></span>

<span data-ttu-id="6956e-430">値</span><span class="sxs-lookup"><span data-stu-id="6956e-430">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-431">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-431">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="6956e-432">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-432">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="6956e-433">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-433">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="6956e-434">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-434">Parameters - leftMarginMode</span></span>

<span data-ttu-id="6956e-435">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-435">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="6956e-436">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-436">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="6956e-437">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-437">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="6956e-438">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-438">Parameters - leftMarginValue</span></span>

<span data-ttu-id="6956e-439">値</span><span class="sxs-lookup"><span data-stu-id="6956e-439">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="6956e-440">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-440">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="6956e-441">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="6956e-441">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="6956e-442">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="6956e-442">Parameters - leftMode</span></span>

<span data-ttu-id="6956e-443">値</span><span class="sxs-lookup"><span data-stu-id="6956e-443">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="6956e-444">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="6956e-444">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="6956e-445">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="6956e-445">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="6956e-446">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="6956e-446">Parameters - leftValue</span></span>

<span data-ttu-id="6956e-447">値</span><span class="sxs-lookup"><span data-stu-id="6956e-447">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="6956e-448">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="6956e-448">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="6956e-449">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="6956e-449">Method moveControl</span></span>

<span data-ttu-id="6956e-450">コントロールに ID で指定されているコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="6956e-450">Moves a control that is specified by ID to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="6956e-451">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="6956e-451">Parameters - moveControl</span></span>

<span data-ttu-id="6956e-452">controlId</span><span class="sxs-lookup"><span data-stu-id="6956e-452">controlId</span></span>  

<!-- -->

<span data-ttu-id="6956e-453">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="6956e-453">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="6956e-454">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="6956e-454">Return Value - moveControl</span></span>

<span data-ttu-id="6956e-455">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="6956e-455">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="6956e-456">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="6956e-456">Remarks - moveControl</span></span>

<span data-ttu-id="6956e-457">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="6956e-457">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="6956e-458">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="6956e-458">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="6956e-459">メソッド名</span><span class="sxs-lookup"><span data-stu-id="6956e-459">Method name</span></span>

<span data-ttu-id="6956e-460">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-460">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="6956e-461">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="6956e-461">Parameters - name</span></span>

<span data-ttu-id="6956e-462">値</span><span class="sxs-lookup"><span data-stu-id="6956e-462">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="6956e-463">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="6956e-463">Return Value - name</span></span>

<span data-ttu-id="6956e-464">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="6956e-464">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="6956e-465">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="6956e-465">Remarks - name</span></span>

<span data-ttu-id="6956e-466">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6956e-466">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="6956e-467">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="6956e-467">Begins with a letter.</span></span>
-   <span data-ttu-id="6956e-468">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="6956e-468">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="6956e-469">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6956e-469">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="6956e-470">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="6956e-470">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="6956e-471">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="6956e-471">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="6956e-472">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="6956e-472">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="6956e-473">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6956e-473">Parameters - neededPermission</span></span>

<span data-ttu-id="6956e-474">値</span><span class="sxs-lookup"><span data-stu-id="6956e-474">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="6956e-475">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6956e-475">Return Value - neededPermission</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="6956e-476">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="6956e-476">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="6956e-477">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="6956e-477">Parameters - normalImage</span></span>

<span data-ttu-id="6956e-478">値</span><span class="sxs-lookup"><span data-stu-id="6956e-478">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="6956e-479">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="6956e-479">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="6956e-480">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="6956e-480">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="6956e-481">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="6956e-481">Parameters - normalResource</span></span>

<span data-ttu-id="6956e-482">値</span><span class="sxs-lookup"><span data-stu-id="6956e-482">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="6956e-483">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="6956e-483">Return Value - normalResource</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="6956e-484">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-484">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="6956e-485">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-485">Parameters - rightMargin</span></span>

<span data-ttu-id="6956e-486">値</span><span class="sxs-lookup"><span data-stu-id="6956e-486">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-487">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-487">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="6956e-488">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-488">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="6956e-489">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-489">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="6956e-490">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-490">Parameters - rightMarginMode</span></span>

<span data-ttu-id="6956e-491">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-491">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="6956e-492">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-492">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="6956e-493">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-493">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="6956e-494">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-494">Parameters - rightMarginValue</span></span>

<span data-ttu-id="6956e-495">値</span><span class="sxs-lookup"><span data-stu-id="6956e-495">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="6956e-496">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-496">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="6956e-497">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="6956e-497">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="6956e-498">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="6956e-498">Parameters - securityKey</span></span>

<span data-ttu-id="6956e-499">値</span><span class="sxs-lookup"><span data-stu-id="6956e-499">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="6956e-500">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="6956e-500">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="6956e-501">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="6956e-501">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="6956e-502">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="6956e-502">Parameters - skip</span></span>

<span data-ttu-id="6956e-503">値</span><span class="sxs-lookup"><span data-stu-id="6956e-503">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="6956e-504">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="6956e-504">Return Value - skip</span></span>

## <a name="method-top"></a><span data-ttu-id="6956e-505">メソッド top</span><span class="sxs-lookup"><span data-stu-id="6956e-505">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="6956e-506">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="6956e-506">Parameters - top</span></span>

<span data-ttu-id="6956e-507">値</span><span class="sxs-lookup"><span data-stu-id="6956e-507">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-508">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-508">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="6956e-509">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="6956e-509">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="6956e-510">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-510">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="6956e-511">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-511">Parameters - topMargin</span></span>

<span data-ttu-id="6956e-512">値</span><span class="sxs-lookup"><span data-stu-id="6956e-512">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-513">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-513">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="6956e-514">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="6956e-514">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="6956e-515">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-515">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="6956e-516">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-516">Parameters - topMarginMode</span></span>

<span data-ttu-id="6956e-517">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-517">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="6956e-518">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="6956e-518">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="6956e-519">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-519">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="6956e-520">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-520">Parameters - topMarginValue</span></span>

<span data-ttu-id="6956e-521">値</span><span class="sxs-lookup"><span data-stu-id="6956e-521">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="6956e-522">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="6956e-522">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="6956e-523">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="6956e-523">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="6956e-524">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="6956e-524">Parameters - topMode</span></span>

<span data-ttu-id="6956e-525">値</span><span class="sxs-lookup"><span data-stu-id="6956e-525">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="6956e-526">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="6956e-526">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="6956e-527">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="6956e-527">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="6956e-528">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="6956e-528">Parameters - topValue</span></span>

<span data-ttu-id="6956e-529">値</span><span class="sxs-lookup"><span data-stu-id="6956e-529">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="6956e-530">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="6956e-530">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="6956e-531">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="6956e-531">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="6956e-532">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="6956e-532">Parameters - type</span></span>

<span data-ttu-id="6956e-533">値</span><span class="sxs-lookup"><span data-stu-id="6956e-533">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="6956e-534">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="6956e-534">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="6956e-535">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="6956e-535">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="6956e-536">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="6956e-536">Parameters - userData</span></span>

<span data-ttu-id="6956e-537">値</span><span class="sxs-lookup"><span data-stu-id="6956e-537">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="6956e-538">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="6956e-538">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="6956e-539">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="6956e-539">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="6956e-540">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6956e-540">Parameters - userDataItem</span></span>

<span data-ttu-id="6956e-541">値</span><span class="sxs-lookup"><span data-stu-id="6956e-541">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="6956e-542">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6956e-542">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="6956e-543">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="6956e-543">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="6956e-544">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6956e-544">Parameters - userDataItems</span></span>

<span data-ttu-id="6956e-545">値</span><span class="sxs-lookup"><span data-stu-id="6956e-545">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="6956e-546">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6956e-546">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="6956e-547">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="6956e-547">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="6956e-548">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="6956e-548">Parameters - useUserLayout</span></span>

<span data-ttu-id="6956e-549">値</span><span class="sxs-lookup"><span data-stu-id="6956e-549">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="6956e-550">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="6956e-550">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="6956e-551">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6956e-551">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="6956e-552">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6956e-552">Parameters - verticalSpacing</span></span>

<span data-ttu-id="6956e-553">値</span><span class="sxs-lookup"><span data-stu-id="6956e-553">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-554">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-554">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="6956e-555">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6956e-555">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="6956e-556">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6956e-556">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="6956e-557">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6956e-557">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="6956e-558">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-558">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="6956e-559">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6956e-559">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="6956e-560">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6956e-560">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="6956e-561">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6956e-561">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="6956e-562">値</span><span class="sxs-lookup"><span data-stu-id="6956e-562">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="6956e-563">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6956e-563">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="6956e-564">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="6956e-564">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="6956e-565">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="6956e-565">Parameters - visible</span></span>

<span data-ttu-id="6956e-566">値</span><span class="sxs-lookup"><span data-stu-id="6956e-566">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="6956e-567">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="6956e-567">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="6956e-568">メソッド width</span><span class="sxs-lookup"><span data-stu-id="6956e-568">Method width</span></span>

<span data-ttu-id="6956e-569">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-569">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="6956e-570">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="6956e-570">Parameters - width</span></span>

<span data-ttu-id="6956e-571">値</span><span class="sxs-lookup"><span data-stu-id="6956e-571">value</span></span>  

<!-- -->

<span data-ttu-id="6956e-572">モード</span><span class="sxs-lookup"><span data-stu-id="6956e-572">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="6956e-573">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="6956e-573">Return Value - width</span></span>

<span data-ttu-id="6956e-574">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6956e-574">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="6956e-575">備考 - width</span><span class="sxs-lookup"><span data-stu-id="6956e-575">Remarks - width</span></span>

<span data-ttu-id="6956e-576">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-576">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6956e-577">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="6956e-577">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="6956e-578">モード。</span><span class="sxs-lookup"><span data-stu-id="6956e-578">Mode.</span></span>           | <span data-ttu-id="6956e-579">幅計算。</span><span class="sxs-lookup"><span data-stu-id="6956e-579">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6956e-580">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="6956e-580">-1 Exact.</span></span>       | <span data-ttu-id="6956e-581">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-581">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6956e-582">0 自動。</span><span class="sxs-lookup"><span data-stu-id="6956e-582">0 Auto.</span></span>         | <span data-ttu-id="6956e-583">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-583">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6956e-584">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="6956e-584">1 Column width.</span></span> | <span data-ttu-id="6956e-585">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6956e-585">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="6956e-586">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6956e-586">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="6956e-587">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="6956e-587">Method widthMode</span></span>

<span data-ttu-id="6956e-588">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-588">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="6956e-589">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="6956e-589">Parameters - widthMode</span></span>

<span data-ttu-id="6956e-590">値</span><span class="sxs-lookup"><span data-stu-id="6956e-590">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="6956e-591">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6956e-591">Return Value - widthMode</span></span>

<span data-ttu-id="6956e-592">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6956e-592">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="6956e-593">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6956e-593">Remarks - widthMode</span></span>

<span data-ttu-id="6956e-594">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="6956e-594">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="6956e-595">モード。</span><span class="sxs-lookup"><span data-stu-id="6956e-595">Mode.</span></span>         | <span data-ttu-id="6956e-596">幅計算。</span><span class="sxs-lookup"><span data-stu-id="6956e-596">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6956e-597">正確。</span><span class="sxs-lookup"><span data-stu-id="6956e-597">Exact.</span></span>        | <span data-ttu-id="6956e-598">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-598">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6956e-599">自動。</span><span class="sxs-lookup"><span data-stu-id="6956e-599">Auto.</span></span>         | <span data-ttu-id="6956e-600">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6956e-600">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6956e-601">列の幅。</span><span class="sxs-lookup"><span data-stu-id="6956e-601">Column width.</span></span> | <span data-ttu-id="6956e-602">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6956e-602">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="6956e-603">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6956e-603">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="6956e-604">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="6956e-604">Method widthValue</span></span>

<span data-ttu-id="6956e-605">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6956e-605">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="6956e-606">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="6956e-606">Parameters - widthValue</span></span>

<span data-ttu-id="6956e-607">値</span><span class="sxs-lookup"><span data-stu-id="6956e-607">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="6956e-608">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6956e-608">Return Value - widthValue</span></span>

<span data-ttu-id="6956e-609">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6956e-609">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="6956e-610">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6956e-610">Remarks - widthValue</span></span>

<span data-ttu-id="6956e-611">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6956e-611">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="6956e-612">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6956e-612">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="6956e-613">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6956e-613">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="6956e-614">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="6956e-614">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="6956e-615">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="6956e-615">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="6956e-616">overrideObject</span><span class="sxs-lookup"><span data-stu-id="6956e-616">overrideObject</span></span>  

