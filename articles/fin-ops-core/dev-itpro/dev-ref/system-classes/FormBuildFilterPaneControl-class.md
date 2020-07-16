---
title: FormBuildFilterPaneControl クラス
description: このトピックでは、FormBuildFilterPaneControl クラスについて説明します。
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
ms.openlocfilehash: 71312564ffd285fbe4a41716616e322ec48b0b80
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502650"
---
# <a name="class-formbuildfilterpanecontrol"></a><span data-ttu-id="5e47a-103">クラス FormBuildFilterPaneControl</span><span class="sxs-lookup"><span data-stu-id="5e47a-103">Class FormBuildFilterPaneControl</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormBuildFilterPaneControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="5e47a-104">備考</span><span class="sxs-lookup"><span data-stu-id="5e47a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="5e47a-105">例</span><span class="sxs-lookup"><span data-stu-id="5e47a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5e47a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="5e47a-106">Methods</span></span>

| <span data-ttu-id="5e47a-107">方法</span><span class="sxs-lookup"><span data-stu-id="5e47a-107">Method</span></span>                                                                                                      | <span data-ttu-id="5e47a-108">説明</span><span class="sxs-lookup"><span data-stu-id="5e47a-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e47a-109">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-109">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="5e47a-110">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-110">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="5e47a-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="5e47a-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-112">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="5e47a-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="5e47a-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-114">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="5e47a-115">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-115">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="5e47a-116">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-116">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="5e47a-117">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-117">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="5e47a-118">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-118">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="5e47a-119">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-119">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="5e47a-120">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-120">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="5e47a-121">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-121">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="5e47a-122">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-122">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="5e47a-123">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-123">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="5e47a-124">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-124">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="5e47a-125">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-125">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="5e47a-126">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-126">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="5e47a-127">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-127">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="5e47a-128">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-128">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="5e47a-129">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-129">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="5e47a-130">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-130">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="5e47a-131">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-131">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="5e47a-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="5e47a-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="5e47a-134">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="5e47a-134">public int containerId()</span></span>                                                                                    | <span data-ttu-id="5e47a-135">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-135">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="5e47a-136">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-136">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="5e47a-137">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-137">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="5e47a-138">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-138">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="5e47a-139">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-139">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="5e47a-140">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-140">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                  |
| <span data-ttu-id="5e47a-141">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-141">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="5e47a-142">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-142">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="5e47a-143">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-143">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="5e47a-144">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-144">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="5e47a-145">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-145">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="5e47a-146">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-146">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="5e47a-147">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-147">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="5e47a-148">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-148">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="5e47a-149">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-149">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="5e47a-150">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-150">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="5e47a-151">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-151">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="5e47a-152">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-152">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="5e47a-153">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-153">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="5e47a-154">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-154">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="5e47a-155">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-155">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="5e47a-156">public int id()</span><span class="sxs-lookup"><span data-stu-id="5e47a-156">public int id()</span></span>                                                                                             | <span data-ttu-id="5e47a-157">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-157">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="5e47a-158">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="5e47a-158">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="5e47a-159">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-159">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="5e47a-160">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-160">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="5e47a-161">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-161">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="5e47a-162">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-162">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="5e47a-163">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-163">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="5e47a-164">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-164">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="5e47a-165">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-165">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="5e47a-166">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-166">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="5e47a-167">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-167">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="5e47a-168">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-168">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="5e47a-169">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-169">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="5e47a-170">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-170">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="5e47a-171">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-171">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="5e47a-172">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-172">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="5e47a-173">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-173">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="5e47a-174">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-174">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="5e47a-175">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-175">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="5e47a-176">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-176">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="5e47a-177">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-177">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="5e47a-178">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-178">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="5e47a-179">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-179">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="5e47a-180">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-180">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="5e47a-181">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-181">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="5e47a-182">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-182">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="5e47a-183">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-183">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="5e47a-184">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-184">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="5e47a-185">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-185">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="5e47a-186">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-186">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="5e47a-187">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-187">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="5e47a-188">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-188">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="5e47a-189">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-189">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="5e47a-190">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-190">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="5e47a-191">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-191">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="5e47a-192">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-192">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="5e47a-193">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-193">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="5e47a-194">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="5e47a-194">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-alignchild"></a><span data-ttu-id="5e47a-195">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="5e47a-195">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="5e47a-196">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="5e47a-196">Parameters - alignChild</span></span>

<span data-ttu-id="5e47a-197">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-197">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="5e47a-198">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="5e47a-198">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="5e47a-199">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="5e47a-199">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="5e47a-200">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="5e47a-200">Parameters - alignChildren</span></span>

<span data-ttu-id="5e47a-201">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-201">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="5e47a-202">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="5e47a-202">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="5e47a-203">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="5e47a-203">Method alignControl</span></span>

<span data-ttu-id="5e47a-204">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-204">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="5e47a-205">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="5e47a-205">Parameters - alignControl</span></span>

<span data-ttu-id="5e47a-206">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-206">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="5e47a-207">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="5e47a-207">Return Value - alignControl</span></span>

<span data-ttu-id="5e47a-208">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5e47a-208">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="5e47a-209">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="5e47a-209">Remarks - alignControl</span></span>

<span data-ttu-id="5e47a-210">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-210">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="5e47a-211">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="5e47a-211">Method allowEdit</span></span>

<span data-ttu-id="5e47a-212">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-212">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="5e47a-213">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="5e47a-213">Parameters - allowEdit</span></span>

<span data-ttu-id="5e47a-214">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-214">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="5e47a-215">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="5e47a-215">Return Value - allowEdit</span></span>

<span data-ttu-id="5e47a-216">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5e47a-216">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="5e47a-217">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="5e47a-217">Remarks - allowEdit</span></span>

<span data-ttu-id="5e47a-218">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-218">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="5e47a-219">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="5e47a-219">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="5e47a-220">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="5e47a-220">Parameters - allowUserSetup</span></span>

<span data-ttu-id="5e47a-221">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-221">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="5e47a-222">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="5e47a-222">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="5e47a-223">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="5e47a-223">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="5e47a-224">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="5e47a-224">Parameters - arrangeGuide</span></span>

<span data-ttu-id="5e47a-225">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-225">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="5e47a-226">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="5e47a-226">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="5e47a-227">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="5e47a-227">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="5e47a-228">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="5e47a-228">Parameters - arrangeMethod</span></span>

<span data-ttu-id="5e47a-229">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-229">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="5e47a-230">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="5e47a-230">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="5e47a-231">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="5e47a-231">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="5e47a-232">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="5e47a-232">Parameters - arrangeWhen</span></span>

<span data-ttu-id="5e47a-233">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-233">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="5e47a-234">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="5e47a-234">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="5e47a-235">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="5e47a-235">Method autoDeclaration</span></span>

<span data-ttu-id="5e47a-236">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-236">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="5e47a-237">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="5e47a-237">Parameters - autoDeclaration</span></span>

<span data-ttu-id="5e47a-238">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-238">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="5e47a-239">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="5e47a-239">Return Value - autoDeclaration</span></span>

<span data-ttu-id="5e47a-240">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5e47a-240">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="5e47a-241">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="5e47a-241">Remarks - autoDeclaration</span></span>

<span data-ttu-id="5e47a-242">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="5e47a-242">Controls cannot have identical names.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="5e47a-243">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-243">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="5e47a-244">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-244">Parameters - bottomMargin</span></span>

<span data-ttu-id="5e47a-245">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-245">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-246">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-246">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="5e47a-247">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-247">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="5e47a-248">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-248">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="5e47a-249">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-249">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="5e47a-250">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-250">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="5e47a-251">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-251">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="5e47a-252">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-252">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="5e47a-253">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-253">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="5e47a-254">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-254">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="5e47a-255">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-255">Return Value - bottomMarginValue</span></span>

## <a name="method-caption"></a><span data-ttu-id="5e47a-256">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="5e47a-256">Method caption</span></span>

<span data-ttu-id="5e47a-257">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-257">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="5e47a-258">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="5e47a-258">Parameters - caption</span></span>

<span data-ttu-id="5e47a-259">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-259">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="5e47a-260">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="5e47a-260">Return Value - caption</span></span>

<span data-ttu-id="5e47a-261">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="5e47a-261">The string that is used as the caption of the control.</span></span>

## <a name="method-columns"></a><span data-ttu-id="5e47a-262">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="5e47a-262">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="5e47a-263">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="5e47a-263">Parameters - columns</span></span>

<span data-ttu-id="5e47a-264">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-264">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-265">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-265">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="5e47a-266">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="5e47a-266">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="5e47a-267">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-267">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="5e47a-268">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-268">Parameters - columnsMode</span></span>

<span data-ttu-id="5e47a-269">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-269">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="5e47a-270">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-270">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="5e47a-271">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="5e47a-271">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="5e47a-272">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="5e47a-272">Parameters - columnspace</span></span>

<span data-ttu-id="5e47a-273">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-273">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-274">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-274">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="5e47a-275">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="5e47a-275">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="5e47a-276">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-276">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="5e47a-277">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-277">Parameters - columnspaceMode</span></span>

<span data-ttu-id="5e47a-278">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-278">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="5e47a-279">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-279">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="5e47a-280">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-280">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="5e47a-281">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-281">Parameters - columnspaceValue</span></span>

<span data-ttu-id="5e47a-282">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-282">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="5e47a-283">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-283">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="5e47a-284">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-284">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="5e47a-285">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-285">Parameters - columnsValue</span></span>

<span data-ttu-id="5e47a-286">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-286">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="5e47a-287">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-287">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="5e47a-288">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="5e47a-288">Method configurationKey</span></span>

<span data-ttu-id="5e47a-289">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-289">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="5e47a-290">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="5e47a-290">Parameters - configurationKey</span></span>

<span data-ttu-id="5e47a-291">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-291">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="5e47a-292">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="5e47a-292">Return Value - configurationKey</span></span>

<span data-ttu-id="5e47a-293">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="5e47a-293">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="5e47a-294">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="5e47a-294">Remarks - configurationKey</span></span>

<span data-ttu-id="5e47a-295">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-295">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="5e47a-296">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="5e47a-296">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="5e47a-297">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="5e47a-297">Method containerId</span></span>

<span data-ttu-id="5e47a-298">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-298">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="5e47a-299">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="5e47a-299">Return Value - containerId</span></span>

<span data-ttu-id="5e47a-300">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="5e47a-300">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="5e47a-301">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="5e47a-301">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="5e47a-302">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="5e47a-302">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="5e47a-303">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-303">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="5e47a-304">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="5e47a-304">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="5e47a-305">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="5e47a-305">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="5e47a-306">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="5e47a-306">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="5e47a-307">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-307">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="5e47a-308">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="5e47a-308">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="5e47a-309">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="5e47a-309">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="5e47a-310">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="5e47a-310">Parameters - dataRelationPath</span></span>

<span data-ttu-id="5e47a-311">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-311">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="5e47a-312">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="5e47a-312">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="5e47a-313">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="5e47a-313">Method dataSource</span></span>

<span data-ttu-id="5e47a-314">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-314">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="5e47a-315">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="5e47a-315">Parameters - dataSource</span></span>

<span data-ttu-id="5e47a-316">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-316">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="5e47a-317">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="5e47a-317">Return Value - dataSource</span></span>

<span data-ttu-id="5e47a-318">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="5e47a-318">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="5e47a-319">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="5e47a-319">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="5e47a-320">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="5e47a-320">Parameters - displayTarget</span></span>

<span data-ttu-id="5e47a-321">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-321">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="5e47a-322">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="5e47a-322">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="5e47a-323">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="5e47a-323">Method dragDrop</span></span>

<span data-ttu-id="5e47a-324">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-324">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="5e47a-325">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="5e47a-325">Parameters - dragDrop</span></span>

<span data-ttu-id="5e47a-326">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-326">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="5e47a-327">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="5e47a-327">Return Value - dragDrop</span></span>

<span data-ttu-id="5e47a-328">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="5e47a-328">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="5e47a-329">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="5e47a-329">Method enabled</span></span>

<span data-ttu-id="5e47a-330">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-330">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="5e47a-331">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="5e47a-331">Parameters - enabled</span></span>

<span data-ttu-id="5e47a-332">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-332">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="5e47a-333">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="5e47a-333">Return Value - enabled</span></span>

<span data-ttu-id="5e47a-334">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5e47a-334">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="5e47a-335">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="5e47a-335">Remarks - enabled</span></span>

<span data-ttu-id="5e47a-336">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-336">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="5e47a-337">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-337">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="5e47a-338">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-338">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="5e47a-339">メソッド height</span><span class="sxs-lookup"><span data-stu-id="5e47a-339">Method height</span></span>

<span data-ttu-id="5e47a-340">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-340">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="5e47a-341">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="5e47a-341">Parameters - height</span></span>

<span data-ttu-id="5e47a-342">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-342">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-343">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-343">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="5e47a-344">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="5e47a-344">Return Value - height</span></span>

<span data-ttu-id="5e47a-345">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="5e47a-345">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="5e47a-346">備考 - height</span><span class="sxs-lookup"><span data-stu-id="5e47a-346">Remarks - height</span></span>

<span data-ttu-id="5e47a-347">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-347">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="5e47a-348">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="5e47a-348">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="5e47a-349">モード。</span><span class="sxs-lookup"><span data-stu-id="5e47a-349">Mode.</span></span>            | <span data-ttu-id="5e47a-350">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="5e47a-350">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e47a-351">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="5e47a-351">-1 Exact.</span></span>        | <span data-ttu-id="5e47a-352">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-352">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="5e47a-353">0 自動。</span><span class="sxs-lookup"><span data-stu-id="5e47a-353">0 Auto.</span></span>          | <span data-ttu-id="5e47a-354">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-354">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="5e47a-355">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="5e47a-355">1 Column height.</span></span> | <span data-ttu-id="5e47a-356">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-356">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="5e47a-357">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-357">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="5e47a-358">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-358">Method heightMode</span></span>

<span data-ttu-id="5e47a-359">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-359">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="5e47a-360">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-360">Parameters - heightMode</span></span>

<span data-ttu-id="5e47a-361">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-361">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="5e47a-362">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-362">Return Value - heightMode</span></span>

<span data-ttu-id="5e47a-363">計算モード。</span><span class="sxs-lookup"><span data-stu-id="5e47a-363">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="5e47a-364">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-364">Remarks - heightMode</span></span>

<span data-ttu-id="5e47a-365">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="5e47a-365">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="5e47a-366">モード。</span><span class="sxs-lookup"><span data-stu-id="5e47a-366">Mode.</span></span>          | <span data-ttu-id="5e47a-367">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="5e47a-367">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e47a-368">正確。</span><span class="sxs-lookup"><span data-stu-id="5e47a-368">Exact.</span></span>         | <span data-ttu-id="5e47a-369">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-369">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="5e47a-370">自動。</span><span class="sxs-lookup"><span data-stu-id="5e47a-370">Auto.</span></span>          | <span data-ttu-id="5e47a-371">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-371">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="5e47a-372">列の高さ</span><span class="sxs-lookup"><span data-stu-id="5e47a-372">Column height.</span></span> | <span data-ttu-id="5e47a-373">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-373">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="5e47a-374">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-374">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="5e47a-375">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-375">Method heightValue</span></span>

<span data-ttu-id="5e47a-376">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-376">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="5e47a-377">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-377">Parameters - heightValue</span></span>

<span data-ttu-id="5e47a-378">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-378">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="5e47a-379">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-379">Return Value - heightValue</span></span>

<span data-ttu-id="5e47a-380">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="5e47a-380">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="5e47a-381">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-381">Remarks - heightValue</span></span>

<span data-ttu-id="5e47a-382">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="5e47a-382">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="5e47a-383">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="5e47a-383">Method helpText</span></span>

<span data-ttu-id="5e47a-384">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-384">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="5e47a-385">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="5e47a-385">Parameters - helpText</span></span>

<span data-ttu-id="5e47a-386">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-386">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="5e47a-387">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="5e47a-387">Return Value - helpText</span></span>

<span data-ttu-id="5e47a-388">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="5e47a-388">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="5e47a-389">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="5e47a-389">Remarks - helpText</span></span>

<span data-ttu-id="5e47a-390">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-390">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="5e47a-391">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="5e47a-391">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="5e47a-392">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="5e47a-392">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="5e47a-393">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="5e47a-393">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="5e47a-394">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-394">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="5e47a-395">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="5e47a-395">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="5e47a-396">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="5e47a-396">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="5e47a-397">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="5e47a-397">Parameters - hierarchyParent</span></span>

<span data-ttu-id="5e47a-398">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-398">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="5e47a-399">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="5e47a-399">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="5e47a-400">メソッド id</span><span class="sxs-lookup"><span data-stu-id="5e47a-400">Method id</span></span>

<span data-ttu-id="5e47a-401">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-401">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="5e47a-402">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="5e47a-402">Return Value - id</span></span>

<span data-ttu-id="5e47a-403">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="5e47a-403">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="5e47a-404">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="5e47a-404">Method isContainer</span></span>

<span data-ttu-id="5e47a-405">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-405">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="5e47a-406">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="5e47a-406">Return Value - isContainer</span></span>

<span data-ttu-id="5e47a-407">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5e47a-407">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="5e47a-408">メソッド left</span><span class="sxs-lookup"><span data-stu-id="5e47a-408">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="5e47a-409">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="5e47a-409">Parameters - left</span></span>

<span data-ttu-id="5e47a-410">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-410">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-411">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-411">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="5e47a-412">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="5e47a-412">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="5e47a-413">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-413">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="5e47a-414">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-414">Parameters - leftMargin</span></span>

<span data-ttu-id="5e47a-415">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-415">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-416">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-416">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="5e47a-417">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-417">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="5e47a-418">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-418">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="5e47a-419">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-419">Parameters - leftMarginMode</span></span>

<span data-ttu-id="5e47a-420">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-420">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="5e47a-421">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-421">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="5e47a-422">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-422">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="5e47a-423">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-423">Parameters - leftMarginValue</span></span>

<span data-ttu-id="5e47a-424">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-424">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="5e47a-425">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-425">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="5e47a-426">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-426">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="5e47a-427">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-427">Parameters - leftMode</span></span>

<span data-ttu-id="5e47a-428">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-428">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="5e47a-429">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-429">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="5e47a-430">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-430">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="5e47a-431">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-431">Parameters - leftValue</span></span>

<span data-ttu-id="5e47a-432">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-432">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="5e47a-433">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-433">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="5e47a-434">メソッド名</span><span class="sxs-lookup"><span data-stu-id="5e47a-434">Method name</span></span>

<span data-ttu-id="5e47a-435">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-435">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="5e47a-436">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="5e47a-436">Parameters - name</span></span>

<span data-ttu-id="5e47a-437">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-437">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="5e47a-438">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="5e47a-438">Return Value - name</span></span>

<span data-ttu-id="5e47a-439">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="5e47a-439">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="5e47a-440">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="5e47a-440">Remarks - name</span></span>

<span data-ttu-id="5e47a-441">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-441">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="5e47a-442">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-442">It must start with a letter.</span></span>
-   <span data-ttu-id="5e47a-443">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="5e47a-443">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="5e47a-444">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-444">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="5e47a-445">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="5e47a-445">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="5e47a-446">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="5e47a-446">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="5e47a-447">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="5e47a-447">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="5e47a-448">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="5e47a-448">Parameters - neededPermission</span></span>

<span data-ttu-id="5e47a-449">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-449">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="5e47a-450">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="5e47a-450">Return Value - neededPermission</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="5e47a-451">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-451">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="5e47a-452">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-452">Parameters - rightMargin</span></span>

<span data-ttu-id="5e47a-453">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-453">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-454">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-454">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="5e47a-455">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-455">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="5e47a-456">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-456">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="5e47a-457">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-457">Parameters - rightMarginMode</span></span>

<span data-ttu-id="5e47a-458">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-458">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="5e47a-459">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-459">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="5e47a-460">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-460">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="5e47a-461">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-461">Parameters - rightMarginValue</span></span>

<span data-ttu-id="5e47a-462">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-462">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="5e47a-463">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-463">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="5e47a-464">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="5e47a-464">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="5e47a-465">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="5e47a-465">Parameters - securityKey</span></span>

<span data-ttu-id="5e47a-466">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-466">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="5e47a-467">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="5e47a-467">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="5e47a-468">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="5e47a-468">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="5e47a-469">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="5e47a-469">Parameters - skip</span></span>

<span data-ttu-id="5e47a-470">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-470">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="5e47a-471">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="5e47a-471">Return Value - skip</span></span>

## <a name="method-top"></a><span data-ttu-id="5e47a-472">メソッド top</span><span class="sxs-lookup"><span data-stu-id="5e47a-472">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="5e47a-473">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="5e47a-473">Parameters - top</span></span>

<span data-ttu-id="5e47a-474">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-474">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-475">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-475">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="5e47a-476">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="5e47a-476">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="5e47a-477">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-477">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="5e47a-478">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-478">Parameters - topMargin</span></span>

<span data-ttu-id="5e47a-479">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-479">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-480">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-480">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="5e47a-481">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="5e47a-481">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="5e47a-482">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-482">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="5e47a-483">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-483">Parameters - topMarginMode</span></span>

<span data-ttu-id="5e47a-484">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-484">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="5e47a-485">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-485">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="5e47a-486">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-486">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="5e47a-487">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-487">Parameters - topMarginValue</span></span>

<span data-ttu-id="5e47a-488">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-488">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="5e47a-489">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-489">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="5e47a-490">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-490">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="5e47a-491">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-491">Parameters - topMode</span></span>

<span data-ttu-id="5e47a-492">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-492">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="5e47a-493">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-493">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="5e47a-494">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-494">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="5e47a-495">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-495">Parameters - topValue</span></span>

<span data-ttu-id="5e47a-496">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-496">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="5e47a-497">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-497">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="5e47a-498">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="5e47a-498">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="5e47a-499">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="5e47a-499">Parameters - type</span></span>

<span data-ttu-id="5e47a-500">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-500">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="5e47a-501">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="5e47a-501">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="5e47a-502">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="5e47a-502">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="5e47a-503">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="5e47a-503">Parameters - userData</span></span>

<span data-ttu-id="5e47a-504">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-504">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="5e47a-505">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="5e47a-505">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="5e47a-506">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="5e47a-506">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="5e47a-507">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="5e47a-507">Parameters - userDataItem</span></span>

<span data-ttu-id="5e47a-508">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-508">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="5e47a-509">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="5e47a-509">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="5e47a-510">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="5e47a-510">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="5e47a-511">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="5e47a-511">Parameters - userDataItems</span></span>

<span data-ttu-id="5e47a-512">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-512">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="5e47a-513">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="5e47a-513">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="5e47a-514">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="5e47a-514">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="5e47a-515">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="5e47a-515">Parameters - verticalSpacing</span></span>

<span data-ttu-id="5e47a-516">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-516">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-517">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-517">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="5e47a-518">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="5e47a-518">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="5e47a-519">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-519">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="5e47a-520">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-520">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="5e47a-521">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-521">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="5e47a-522">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-522">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="5e47a-523">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-523">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="5e47a-524">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-524">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="5e47a-525">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-525">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="5e47a-526">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-526">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="5e47a-527">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="5e47a-527">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="5e47a-528">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="5e47a-528">Parameters - visible</span></span>

<span data-ttu-id="5e47a-529">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-529">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="5e47a-530">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="5e47a-530">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="5e47a-531">メソッド width</span><span class="sxs-lookup"><span data-stu-id="5e47a-531">Method width</span></span>

<span data-ttu-id="5e47a-532">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-532">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="5e47a-533">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="5e47a-533">Parameters - width</span></span>

<span data-ttu-id="5e47a-534">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-534">value</span></span>  

<!-- -->

<span data-ttu-id="5e47a-535">モード</span><span class="sxs-lookup"><span data-stu-id="5e47a-535">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="5e47a-536">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="5e47a-536">Return Value - width</span></span>

<span data-ttu-id="5e47a-537">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="5e47a-537">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="5e47a-538">備考 - width</span><span class="sxs-lookup"><span data-stu-id="5e47a-538">Remarks - width</span></span>

<span data-ttu-id="5e47a-539">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-539">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="5e47a-540">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="5e47a-540">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="5e47a-541">モード。</span><span class="sxs-lookup"><span data-stu-id="5e47a-541">Mode.</span></span>           | <span data-ttu-id="5e47a-542">幅計算。</span><span class="sxs-lookup"><span data-stu-id="5e47a-542">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e47a-543">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="5e47a-543">-1 Exact.</span></span>       | <span data-ttu-id="5e47a-544">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-544">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="5e47a-545">0 自動。</span><span class="sxs-lookup"><span data-stu-id="5e47a-545">0 Auto.</span></span>         | <span data-ttu-id="5e47a-546">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-546">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="5e47a-547">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="5e47a-547">1 Column width.</span></span> | <span data-ttu-id="5e47a-548">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-548">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="5e47a-549">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-549">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="5e47a-550">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-550">Method widthMode</span></span>

<span data-ttu-id="5e47a-551">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-551">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="5e47a-552">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-552">Parameters - widthMode</span></span>

<span data-ttu-id="5e47a-553">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-553">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="5e47a-554">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-554">Return Value - widthMode</span></span>

<span data-ttu-id="5e47a-555">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5e47a-555">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="5e47a-556">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="5e47a-556">Remarks - widthMode</span></span>

<span data-ttu-id="5e47a-557">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="5e47a-557">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="5e47a-558">モード。</span><span class="sxs-lookup"><span data-stu-id="5e47a-558">Mode.</span></span>         | <span data-ttu-id="5e47a-559">幅計算。</span><span class="sxs-lookup"><span data-stu-id="5e47a-559">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e47a-560">正確。</span><span class="sxs-lookup"><span data-stu-id="5e47a-560">Exact.</span></span>        | <span data-ttu-id="5e47a-561">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-561">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="5e47a-562">自動。</span><span class="sxs-lookup"><span data-stu-id="5e47a-562">Auto.</span></span>         | <span data-ttu-id="5e47a-563">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5e47a-563">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="5e47a-564">列の幅。</span><span class="sxs-lookup"><span data-stu-id="5e47a-564">Column width.</span></span> | <span data-ttu-id="5e47a-565">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-565">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="5e47a-566">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="5e47a-566">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="5e47a-567">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-567">Method widthValue</span></span>

<span data-ttu-id="5e47a-568">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-568">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="5e47a-569">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-569">Parameters - widthValue</span></span>

<span data-ttu-id="5e47a-570">値</span><span class="sxs-lookup"><span data-stu-id="5e47a-570">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="5e47a-571">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-571">Return Value - widthValue</span></span>

<span data-ttu-id="5e47a-572">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="5e47a-572">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="5e47a-573">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="5e47a-573">Remarks - widthValue</span></span>

<span data-ttu-id="5e47a-574">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e47a-574">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="5e47a-575">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="5e47a-575">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="5e47a-576">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="5e47a-576">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="5e47a-577">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="5e47a-577">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="5e47a-578">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="5e47a-578">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="5e47a-579">overrideObject</span><span class="sxs-lookup"><span data-stu-id="5e47a-579">overrideObject</span></span>  

