---
title: FormBuildTableControl クラス
description: このトピックでは、FormBuildTableControl クラスについて説明します。
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
ms.openlocfilehash: abaa912a92635a544cf7a2e944e7f64b853e28e2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502638"
---
# <a name="class-formbuildtablecontrol"></a><span data-ttu-id="cb845-103">クラス FormBuildTableControl</span><span class="sxs-lookup"><span data-stu-id="cb845-103">Class FormBuildTableControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildTableControl extends FormBuildControl
```

<span data-ttu-id="cb845-104">FormBuildTableControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="cb845-104">The FormBuildTableControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb845-105">備考</span><span class="sxs-lookup"><span data-stu-id="cb845-105">Remarks</span></span>

<span data-ttu-id="cb845-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cb845-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="cb845-107">例</span><span class="sxs-lookup"><span data-stu-id="cb845-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="cb845-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="cb845-108">Methods</span></span>

| <span data-ttu-id="cb845-109">方法</span><span class="sxs-lookup"><span data-stu-id="cb845-109">Method</span></span>                                                                                                      | <span data-ttu-id="cb845-110">説明</span><span class="sxs-lookup"><span data-stu-id="cb845-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb845-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="cb845-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="cb845-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="cb845-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="cb845-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="cb845-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="cb845-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="cb845-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-118">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="cb845-119">public int bottomMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-119">public int bottomMargin(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="cb845-120">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-120">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="cb845-121">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-121">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="cb845-122">public int column(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-122">public int column(\[int value\])</span></span>                                                                            |                                                                                                                                         |
| <span data-ttu-id="cb845-123">public int columns(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-123">public int columns(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="cb845-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="cb845-125">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-125">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="cb845-126">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="cb845-126">public int containerId()</span></span>                                                                                    | <span data-ttu-id="cb845-127">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="cb845-127">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="cb845-128">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-128">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="cb845-129">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-129">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="cb845-130">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-130">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="cb845-131">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-131">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="cb845-132">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-132">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="cb845-133">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-133">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="cb845-134">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-134">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="cb845-135">public boolean gridLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-135">public boolean gridLines(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="cb845-136">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="cb845-136">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="cb845-137">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-137">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="cb845-138">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-138">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="cb845-139">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-139">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="cb845-140">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-140">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="cb845-141">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-141">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="cb845-142">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-142">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="cb845-143">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-143">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="cb845-144">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-144">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="cb845-145">public boolean highlightActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-145">public boolean highlightActive(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="cb845-146">public int id()</span><span class="sxs-lookup"><span data-stu-id="cb845-146">public int id()</span></span>                                                                                             | <span data-ttu-id="cb845-147">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="cb845-147">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="cb845-148">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="cb845-148">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="cb845-149">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="cb845-149">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="cb845-150">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="cb845-150">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="cb845-151">public int leftMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-151">public int leftMargin(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="cb845-152">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-152">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="cb845-153">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-153">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="cb845-154">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="cb845-154">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="cb845-155">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="cb845-155">Moves a specified control to the control.</span></span>                                                                                               |
| <span data-ttu-id="cb845-156">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-156">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="cb845-157">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-157">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="cb845-158">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-158">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="cb845-159">public int rightMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-159">public int rightMargin(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="cb845-160">public int row(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-160">public int row(\[int value\])</span></span>                                                                               |                                                                                                                                         |
| <span data-ttu-id="cb845-161">public int rows(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-161">public int rows(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="cb845-162">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-162">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="cb845-163">public boolean showColLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-163">public boolean showColLabels(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="cb845-164">public boolean showRowLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-164">public boolean showRowLabels(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="cb845-165">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-165">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="cb845-166">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="cb845-166">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="cb845-167">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="cb845-167">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="cb845-168">public int topMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-168">public int topMargin(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="cb845-169">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-169">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="cb845-170">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-170">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="cb845-171">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-171">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="cb845-172">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-172">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="cb845-173">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-173">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="cb845-174">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-174">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="cb845-175">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-175">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="cb845-176">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="cb845-176">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="cb845-177">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="cb845-177">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="cb845-178">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-178">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="cb845-179">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-179">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="cb845-180">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="cb845-180">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="cb845-181">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-181">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="cb845-182">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-182">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="cb845-183">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-183">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="cb845-184">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cb845-184">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="cb845-185">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-185">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="cb845-186">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="cb845-186">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="cb845-187">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="cb845-187">Method alignControl</span></span>

<span data-ttu-id="cb845-188">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-188">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="cb845-189">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="cb845-189">Parameters - alignControl</span></span>

<span data-ttu-id="cb845-190">値</span><span class="sxs-lookup"><span data-stu-id="cb845-190">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="cb845-191">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="cb845-191">Return Value - alignControl</span></span>

<span data-ttu-id="cb845-192">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="cb845-192">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="cb845-193">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="cb845-193">Remarks - alignControl</span></span>

<span data-ttu-id="cb845-194">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-194">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="cb845-195">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="cb845-195">Method allowEdit</span></span>

<span data-ttu-id="cb845-196">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-196">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="cb845-197">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="cb845-197">Parameters - allowEdit</span></span>

<span data-ttu-id="cb845-198">値</span><span class="sxs-lookup"><span data-stu-id="cb845-198">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="cb845-199">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="cb845-199">Return Value - allowEdit</span></span>

<span data-ttu-id="cb845-200">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cb845-200">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="cb845-201">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="cb845-201">Remarks - allowEdit</span></span>

<span data-ttu-id="cb845-202">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="cb845-202">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="cb845-203">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="cb845-203">Method autoDeclaration</span></span>

<span data-ttu-id="cb845-204">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-204">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="cb845-205">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="cb845-205">Parameters - autoDeclaration</span></span>

<span data-ttu-id="cb845-206">値</span><span class="sxs-lookup"><span data-stu-id="cb845-206">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="cb845-207">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="cb845-207">Return Value - autoDeclaration</span></span>

<span data-ttu-id="cb845-208">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cb845-208">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="cb845-209">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="cb845-209">Remarks - autoDeclaration</span></span>

<span data-ttu-id="cb845-210">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="cb845-210">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="cb845-211">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cb845-211">Method backgroundColor</span></span>

<span data-ttu-id="cb845-212">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-212">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="cb845-213">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cb845-213">Parameters - backgroundColor</span></span>

<span data-ttu-id="cb845-214">値</span><span class="sxs-lookup"><span data-stu-id="cb845-214">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="cb845-215">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cb845-215">Return Value - backgroundColor</span></span>

<span data-ttu-id="cb845-216">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="cb845-216">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="cb845-217">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cb845-217">Remarks - backgroundColor</span></span>

<span data-ttu-id="cb845-218">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cb845-218">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="cb845-219">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb845-219">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="cb845-220">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="cb845-220">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="cb845-221">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="cb845-221">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="cb845-222">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="cb845-222">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="cb845-223">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="cb845-223">The maximum value for a single byte is 255.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="cb845-224">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-224">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="cb845-225">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-225">Parameters - bottomMargin</span></span>

<span data-ttu-id="cb845-226">値</span><span class="sxs-lookup"><span data-stu-id="cb845-226">value</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="cb845-227">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-227">Return Value - bottomMargin</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="cb845-228">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="cb845-228">Method colorScheme</span></span>

<span data-ttu-id="cb845-229">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-229">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="cb845-230">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="cb845-230">Parameters - colorScheme</span></span>

<span data-ttu-id="cb845-231">値</span><span class="sxs-lookup"><span data-stu-id="cb845-231">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="cb845-232">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="cb845-232">Return Value - colorScheme</span></span>

<span data-ttu-id="cb845-233">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="cb845-233">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="cb845-234">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="cb845-234">Remarks - colorScheme</span></span>

<span data-ttu-id="cb845-235">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-235">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="cb845-236">値です。</span><span class="sxs-lookup"><span data-stu-id="cb845-236">Value.</span></span> | <span data-ttu-id="cb845-237">スタイル。</span><span class="sxs-lookup"><span data-stu-id="cb845-237">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="cb845-238">0</span><span class="sxs-lookup"><span data-stu-id="cb845-238">0</span></span>      | <span data-ttu-id="cb845-239">既定。</span><span class="sxs-lookup"><span data-stu-id="cb845-239">Default.</span></span>                       |
| <span data-ttu-id="cb845-240">1</span><span class="sxs-lookup"><span data-stu-id="cb845-240">1</span></span>      | <span data-ttu-id="cb845-241">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="cb845-241">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="cb845-242">2</span><span class="sxs-lookup"><span data-stu-id="cb845-242">2</span></span>      | <span data-ttu-id="cb845-243">真の配色。</span><span class="sxs-lookup"><span data-stu-id="cb845-243">The true-color scheme.</span></span>         |

## <a name="method-column"></a><span data-ttu-id="cb845-244">メソッド column</span><span class="sxs-lookup"><span data-stu-id="cb845-244">Method column</span></span>

```xpp
public int column([int value])
```

### <a name="parameters---column"></a><span data-ttu-id="cb845-245">パラメーター - column</span><span class="sxs-lookup"><span data-stu-id="cb845-245">Parameters - column</span></span>

<span data-ttu-id="cb845-246">値</span><span class="sxs-lookup"><span data-stu-id="cb845-246">value</span></span>  

### <a name="return-value---column"></a><span data-ttu-id="cb845-247">戻り値 - column</span><span class="sxs-lookup"><span data-stu-id="cb845-247">Return Value - column</span></span>

## <a name="method-columns"></a><span data-ttu-id="cb845-248">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="cb845-248">Method columns</span></span>

```xpp
public int columns([int value])
```

### <a name="parameters---columns"></a><span data-ttu-id="cb845-249">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="cb845-249">Parameters - columns</span></span>

<span data-ttu-id="cb845-250">値</span><span class="sxs-lookup"><span data-stu-id="cb845-250">value</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="cb845-251">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="cb845-251">Return Value - columns</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="cb845-252">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="cb845-252">Method configurationKey</span></span>

<span data-ttu-id="cb845-253">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-253">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="cb845-254">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="cb845-254">Parameters - configurationKey</span></span>

<span data-ttu-id="cb845-255">値</span><span class="sxs-lookup"><span data-stu-id="cb845-255">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="cb845-256">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="cb845-256">Return Value - configurationKey</span></span>

<span data-ttu-id="cb845-257">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="cb845-257">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="cb845-258">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="cb845-258">Remarks - configurationKey</span></span>

<span data-ttu-id="cb845-259">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-259">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="cb845-260">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="cb845-260">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="cb845-261">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="cb845-261">Method containerId</span></span>

<span data-ttu-id="cb845-262">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="cb845-262">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="cb845-263">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="cb845-263">Return Value - containerId</span></span>

<span data-ttu-id="cb845-264">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="cb845-264">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="cb845-265">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="cb845-265">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="cb845-266">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="cb845-266">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="cb845-267">値</span><span class="sxs-lookup"><span data-stu-id="cb845-267">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="cb845-268">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="cb845-268">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="cb845-269">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="cb845-269">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="cb845-270">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="cb845-270">Parameters - dataRelationPath</span></span>

<span data-ttu-id="cb845-271">値</span><span class="sxs-lookup"><span data-stu-id="cb845-271">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="cb845-272">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="cb845-272">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="cb845-273">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="cb845-273">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="cb845-274">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="cb845-274">Parameters - displayTarget</span></span>

<span data-ttu-id="cb845-275">値</span><span class="sxs-lookup"><span data-stu-id="cb845-275">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="cb845-276">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="cb845-276">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="cb845-277">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="cb845-277">Method dragDrop</span></span>

<span data-ttu-id="cb845-278">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-278">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="cb845-279">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="cb845-279">Parameters - dragDrop</span></span>

<span data-ttu-id="cb845-280">値</span><span class="sxs-lookup"><span data-stu-id="cb845-280">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="cb845-281">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="cb845-281">Return Value - dragDrop</span></span>

<span data-ttu-id="cb845-282">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="cb845-282">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="cb845-283">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="cb845-283">Method enabled</span></span>

<span data-ttu-id="cb845-284">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-284">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="cb845-285">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="cb845-285">Parameters - enabled</span></span>

<span data-ttu-id="cb845-286">値</span><span class="sxs-lookup"><span data-stu-id="cb845-286">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="cb845-287">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="cb845-287">Return Value - enabled</span></span>

<span data-ttu-id="cb845-288">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cb845-288">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="cb845-289">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="cb845-289">Remarks - enabled</span></span>

<span data-ttu-id="cb845-290">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="cb845-290">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="cb845-291">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="cb845-291">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="cb845-292">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cb845-292">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-gridlines"></a><span data-ttu-id="cb845-293">メソッド gridLines</span><span class="sxs-lookup"><span data-stu-id="cb845-293">Method gridLines</span></span>

```xpp
public boolean gridLines([boolean value])
```

### <a name="parameters---gridlines"></a><span data-ttu-id="cb845-294">パラメーター - gridLines</span><span class="sxs-lookup"><span data-stu-id="cb845-294">Parameters - gridLines</span></span>

<span data-ttu-id="cb845-295">値</span><span class="sxs-lookup"><span data-stu-id="cb845-295">value</span></span>  

### <a name="return-value---gridlines"></a><span data-ttu-id="cb845-296">戻り値 - gridLines</span><span class="sxs-lookup"><span data-stu-id="cb845-296">Return Value - gridLines</span></span>

## <a name="method-height"></a><span data-ttu-id="cb845-297">メソッド height</span><span class="sxs-lookup"><span data-stu-id="cb845-297">Method height</span></span>

<span data-ttu-id="cb845-298">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-298">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="cb845-299">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="cb845-299">Parameters - height</span></span>

<span data-ttu-id="cb845-300">値</span><span class="sxs-lookup"><span data-stu-id="cb845-300">value</span></span>  

<!-- -->

<span data-ttu-id="cb845-301">モード</span><span class="sxs-lookup"><span data-stu-id="cb845-301">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="cb845-302">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="cb845-302">Return Value - height</span></span>

<span data-ttu-id="cb845-303">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="cb845-303">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="cb845-304">備考 - height</span><span class="sxs-lookup"><span data-stu-id="cb845-304">Remarks - height</span></span>

<span data-ttu-id="cb845-305">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-305">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="cb845-306">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="cb845-306">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="cb845-307">モード。</span><span class="sxs-lookup"><span data-stu-id="cb845-307">Mode.</span></span>            | <span data-ttu-id="cb845-308">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="cb845-308">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb845-309">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="cb845-309">-1 Exact.</span></span>        | <span data-ttu-id="cb845-310">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-310">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="cb845-311">0 自動。</span><span class="sxs-lookup"><span data-stu-id="cb845-311">0 Auto.</span></span>          | <span data-ttu-id="cb845-312">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-312">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="cb845-313">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="cb845-313">1 Column height.</span></span> | <span data-ttu-id="cb845-314">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="cb845-314">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="cb845-315">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="cb845-315">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="cb845-316">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="cb845-316">Method heightMode</span></span>

<span data-ttu-id="cb845-317">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-317">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="cb845-318">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="cb845-318">Parameters - heightMode</span></span>

<span data-ttu-id="cb845-319">値</span><span class="sxs-lookup"><span data-stu-id="cb845-319">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="cb845-320">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="cb845-320">Return Value - heightMode</span></span>

<span data-ttu-id="cb845-321">計算モード。</span><span class="sxs-lookup"><span data-stu-id="cb845-321">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="cb845-322">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="cb845-322">Remarks - heightMode</span></span>

<span data-ttu-id="cb845-323">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="cb845-323">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="cb845-324">モード。</span><span class="sxs-lookup"><span data-stu-id="cb845-324">Mode.</span></span>          | <span data-ttu-id="cb845-325">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="cb845-325">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb845-326">正確。</span><span class="sxs-lookup"><span data-stu-id="cb845-326">Exact.</span></span>         | <span data-ttu-id="cb845-327">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-327">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="cb845-328">自動。</span><span class="sxs-lookup"><span data-stu-id="cb845-328">Auto.</span></span>          | <span data-ttu-id="cb845-329">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-329">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="cb845-330">列の高さ</span><span class="sxs-lookup"><span data-stu-id="cb845-330">Column height.</span></span> | <span data-ttu-id="cb845-331">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="cb845-331">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="cb845-332">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="cb845-332">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="cb845-333">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="cb845-333">Method heightValue</span></span>

<span data-ttu-id="cb845-334">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-334">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="cb845-335">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="cb845-335">Parameters - heightValue</span></span>

<span data-ttu-id="cb845-336">値</span><span class="sxs-lookup"><span data-stu-id="cb845-336">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="cb845-337">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="cb845-337">Return Value - heightValue</span></span>

<span data-ttu-id="cb845-338">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="cb845-338">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="cb845-339">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="cb845-339">Remarks - heightValue</span></span>

<span data-ttu-id="cb845-340">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="cb845-340">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="cb845-341">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="cb845-341">Method helpText</span></span>

<span data-ttu-id="cb845-342">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-342">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="cb845-343">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="cb845-343">Parameters - helpText</span></span>

<span data-ttu-id="cb845-344">値</span><span class="sxs-lookup"><span data-stu-id="cb845-344">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="cb845-345">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="cb845-345">Return Value - helpText</span></span>

<span data-ttu-id="cb845-346">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="cb845-346">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="cb845-347">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="cb845-347">Remarks - helpText</span></span>

<span data-ttu-id="cb845-348">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-348">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="cb845-349">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="cb845-349">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="cb845-350">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="cb845-350">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="cb845-351">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="cb845-351">Parameters - hierarchyParent</span></span>

<span data-ttu-id="cb845-352">値</span><span class="sxs-lookup"><span data-stu-id="cb845-352">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="cb845-353">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="cb845-353">Return Value - hierarchyParent</span></span>

## <a name="method-highlightactive"></a><span data-ttu-id="cb845-354">メソッド highlightActive</span><span class="sxs-lookup"><span data-stu-id="cb845-354">Method highlightActive</span></span>

```xpp
public boolean highlightActive([boolean value])
```

### <a name="parameters---highlightactive"></a><span data-ttu-id="cb845-355">パラメーター - highlightActive</span><span class="sxs-lookup"><span data-stu-id="cb845-355">Parameters - highlightActive</span></span>

<span data-ttu-id="cb845-356">値</span><span class="sxs-lookup"><span data-stu-id="cb845-356">value</span></span>  

### <a name="return-value---highlightactive"></a><span data-ttu-id="cb845-357">戻り値 - highlightActive</span><span class="sxs-lookup"><span data-stu-id="cb845-357">Return Value - highlightActive</span></span>

## <a name="method-id"></a><span data-ttu-id="cb845-358">メソッド id</span><span class="sxs-lookup"><span data-stu-id="cb845-358">Method id</span></span>

<span data-ttu-id="cb845-359">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="cb845-359">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="cb845-360">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="cb845-360">Return Value - id</span></span>

<span data-ttu-id="cb845-361">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="cb845-361">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="cb845-362">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="cb845-362">Method isContainer</span></span>

<span data-ttu-id="cb845-363">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="cb845-363">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="cb845-364">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="cb845-364">Return Value - isContainer</span></span>

<span data-ttu-id="cb845-365">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="cb845-365">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="cb845-366">メソッド left</span><span class="sxs-lookup"><span data-stu-id="cb845-366">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="cb845-367">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="cb845-367">Parameters - left</span></span>

<span data-ttu-id="cb845-368">値</span><span class="sxs-lookup"><span data-stu-id="cb845-368">value</span></span>  

<!-- -->

<span data-ttu-id="cb845-369">モード</span><span class="sxs-lookup"><span data-stu-id="cb845-369">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="cb845-370">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="cb845-370">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="cb845-371">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-371">Method leftMargin</span></span>

```xpp
public int leftMargin([int value])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="cb845-372">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-372">Parameters - leftMargin</span></span>

<span data-ttu-id="cb845-373">値</span><span class="sxs-lookup"><span data-stu-id="cb845-373">value</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="cb845-374">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-374">Return Value - leftMargin</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="cb845-375">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="cb845-375">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="cb845-376">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="cb845-376">Parameters - leftMode</span></span>

<span data-ttu-id="cb845-377">値</span><span class="sxs-lookup"><span data-stu-id="cb845-377">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="cb845-378">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="cb845-378">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="cb845-379">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="cb845-379">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="cb845-380">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="cb845-380">Parameters - leftValue</span></span>

<span data-ttu-id="cb845-381">値</span><span class="sxs-lookup"><span data-stu-id="cb845-381">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="cb845-382">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="cb845-382">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="cb845-383">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="cb845-383">Method moveControl</span></span>

<span data-ttu-id="cb845-384">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="cb845-384">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="cb845-385">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="cb845-385">Parameters - moveControl</span></span>

<span data-ttu-id="cb845-386">controlId</span><span class="sxs-lookup"><span data-stu-id="cb845-386">controlId</span></span>  

<!-- -->

<span data-ttu-id="cb845-387">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="cb845-387">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="cb845-388">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="cb845-388">Return Value - moveControl</span></span>

<span data-ttu-id="cb845-389">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="cb845-389">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="cb845-390">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="cb845-390">Remarks - moveControl</span></span>

<span data-ttu-id="cb845-391">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="cb845-391">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="cb845-392">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="cb845-392">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="cb845-393">メソッド名</span><span class="sxs-lookup"><span data-stu-id="cb845-393">Method name</span></span>

<span data-ttu-id="cb845-394">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-394">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="cb845-395">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="cb845-395">Parameters - name</span></span>

<span data-ttu-id="cb845-396">値</span><span class="sxs-lookup"><span data-stu-id="cb845-396">value</span></span>  
<span data-ttu-id="cb845-397">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="cb845-397">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="cb845-398">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="cb845-398">Return Value - name</span></span>

<span data-ttu-id="cb845-399">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="cb845-399">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="cb845-400">備考 - name</span><span class="sxs-lookup"><span data-stu-id="cb845-400">Remarks - name</span></span>

<span data-ttu-id="cb845-401">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb845-401">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="cb845-402">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb845-402">It must start with a letter.</span></span>
-   <span data-ttu-id="cb845-403">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="cb845-403">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="cb845-404">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cb845-404">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="cb845-405">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="cb845-405">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="cb845-406">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="cb845-406">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="cb845-407">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="cb845-407">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="cb845-408">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="cb845-408">Parameters - neededPermission</span></span>

<span data-ttu-id="cb845-409">値</span><span class="sxs-lookup"><span data-stu-id="cb845-409">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="cb845-410">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="cb845-410">Return Value - neededPermission</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="cb845-411">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-411">Method rightMargin</span></span>

```xpp
public int rightMargin([int value])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="cb845-412">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-412">Parameters - rightMargin</span></span>

<span data-ttu-id="cb845-413">値</span><span class="sxs-lookup"><span data-stu-id="cb845-413">value</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="cb845-414">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-414">Return Value - rightMargin</span></span>

## <a name="method-row"></a><span data-ttu-id="cb845-415">メソッド row</span><span class="sxs-lookup"><span data-stu-id="cb845-415">Method row</span></span>

```xpp
public int row([int value])
```

### <a name="parameters---row"></a><span data-ttu-id="cb845-416">パラメーター - row</span><span class="sxs-lookup"><span data-stu-id="cb845-416">Parameters - row</span></span>

<span data-ttu-id="cb845-417">値</span><span class="sxs-lookup"><span data-stu-id="cb845-417">value</span></span>  

### <a name="return-value---row"></a><span data-ttu-id="cb845-418">戻り値 - row</span><span class="sxs-lookup"><span data-stu-id="cb845-418">Return Value - row</span></span>

## <a name="method-rows"></a><span data-ttu-id="cb845-419">メソッド rows</span><span class="sxs-lookup"><span data-stu-id="cb845-419">Method rows</span></span>

```xpp
public int rows([int value])
```

### <a name="parameters---rows"></a><span data-ttu-id="cb845-420">パラメーター - rows</span><span class="sxs-lookup"><span data-stu-id="cb845-420">Parameters - rows</span></span>

<span data-ttu-id="cb845-421">値</span><span class="sxs-lookup"><span data-stu-id="cb845-421">value</span></span>  

### <a name="return-value---rows"></a><span data-ttu-id="cb845-422">戻り値 - rows</span><span class="sxs-lookup"><span data-stu-id="cb845-422">Return Value - rows</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="cb845-423">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="cb845-423">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="cb845-424">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="cb845-424">Parameters - securityKey</span></span>

<span data-ttu-id="cb845-425">値</span><span class="sxs-lookup"><span data-stu-id="cb845-425">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="cb845-426">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="cb845-426">Return Value - securityKey</span></span>

## <a name="method-showcollabels"></a><span data-ttu-id="cb845-427">メソッド showColLabels</span><span class="sxs-lookup"><span data-stu-id="cb845-427">Method showColLabels</span></span>

```xpp
public boolean showColLabels([boolean value])
```

### <a name="parameters---showcollabels"></a><span data-ttu-id="cb845-428">パラメーター - showColLabels</span><span class="sxs-lookup"><span data-stu-id="cb845-428">Parameters - showColLabels</span></span>

<span data-ttu-id="cb845-429">値</span><span class="sxs-lookup"><span data-stu-id="cb845-429">value</span></span>  

### <a name="return-value---showcollabels"></a><span data-ttu-id="cb845-430">戻り値 - showColLabels</span><span class="sxs-lookup"><span data-stu-id="cb845-430">Return Value - showColLabels</span></span>

## <a name="method-showrowlabels"></a><span data-ttu-id="cb845-431">メソッド showRowLabels</span><span class="sxs-lookup"><span data-stu-id="cb845-431">Method showRowLabels</span></span>

```xpp
public boolean showRowLabels([boolean value])
```

### <a name="parameters---showrowlabels"></a><span data-ttu-id="cb845-432">パラメーター - showRowLabels</span><span class="sxs-lookup"><span data-stu-id="cb845-432">Parameters - showRowLabels</span></span>

<span data-ttu-id="cb845-433">値</span><span class="sxs-lookup"><span data-stu-id="cb845-433">value</span></span>  

### <a name="return-value---showrowlabels"></a><span data-ttu-id="cb845-434">戻り値 - showRowLabels</span><span class="sxs-lookup"><span data-stu-id="cb845-434">Return Value - showRowLabels</span></span>

## <a name="method-skip"></a><span data-ttu-id="cb845-435">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="cb845-435">Method skip</span></span>

<span data-ttu-id="cb845-436">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="cb845-436">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="cb845-437">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="cb845-437">Parameters - skip</span></span>

<span data-ttu-id="cb845-438">値</span><span class="sxs-lookup"><span data-stu-id="cb845-438">value</span></span>  
<span data-ttu-id="cb845-439">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="cb845-439">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="cb845-440">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="cb845-440">Return Value - skip</span></span>

<span data-ttu-id="cb845-441">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cb845-441">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-top"></a><span data-ttu-id="cb845-442">メソッド top</span><span class="sxs-lookup"><span data-stu-id="cb845-442">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="cb845-443">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="cb845-443">Parameters - top</span></span>

<span data-ttu-id="cb845-444">値</span><span class="sxs-lookup"><span data-stu-id="cb845-444">value</span></span>  

<!-- -->

<span data-ttu-id="cb845-445">モード</span><span class="sxs-lookup"><span data-stu-id="cb845-445">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="cb845-446">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="cb845-446">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="cb845-447">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-447">Method topMargin</span></span>

```xpp
public int topMargin([int value])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="cb845-448">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-448">Parameters - topMargin</span></span>

<span data-ttu-id="cb845-449">値</span><span class="sxs-lookup"><span data-stu-id="cb845-449">value</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="cb845-450">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="cb845-450">Return Value - topMargin</span></span>

## <a name="method-topmode"></a><span data-ttu-id="cb845-451">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="cb845-451">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="cb845-452">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="cb845-452">Parameters - topMode</span></span>

<span data-ttu-id="cb845-453">値</span><span class="sxs-lookup"><span data-stu-id="cb845-453">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="cb845-454">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="cb845-454">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="cb845-455">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="cb845-455">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="cb845-456">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="cb845-456">Parameters - topValue</span></span>

<span data-ttu-id="cb845-457">値</span><span class="sxs-lookup"><span data-stu-id="cb845-457">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="cb845-458">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="cb845-458">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="cb845-459">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="cb845-459">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="cb845-460">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="cb845-460">Parameters - type</span></span>

<span data-ttu-id="cb845-461">値</span><span class="sxs-lookup"><span data-stu-id="cb845-461">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="cb845-462">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="cb845-462">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="cb845-463">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="cb845-463">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="cb845-464">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="cb845-464">Parameters - userData</span></span>

<span data-ttu-id="cb845-465">値</span><span class="sxs-lookup"><span data-stu-id="cb845-465">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="cb845-466">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="cb845-466">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="cb845-467">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="cb845-467">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="cb845-468">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="cb845-468">Parameters - userDataItem</span></span>

<span data-ttu-id="cb845-469">値</span><span class="sxs-lookup"><span data-stu-id="cb845-469">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="cb845-470">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="cb845-470">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="cb845-471">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="cb845-471">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="cb845-472">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="cb845-472">Parameters - userDataItems</span></span>

<span data-ttu-id="cb845-473">値</span><span class="sxs-lookup"><span data-stu-id="cb845-473">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="cb845-474">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="cb845-474">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="cb845-475">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="cb845-475">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="cb845-476">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="cb845-476">Parameters - useUserLayout</span></span>

<span data-ttu-id="cb845-477">値</span><span class="sxs-lookup"><span data-stu-id="cb845-477">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="cb845-478">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="cb845-478">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="cb845-479">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="cb845-479">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="cb845-480">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="cb845-480">Parameters - verticalSpacing</span></span>

<span data-ttu-id="cb845-481">値</span><span class="sxs-lookup"><span data-stu-id="cb845-481">value</span></span>  

<!-- -->

<span data-ttu-id="cb845-482">モード</span><span class="sxs-lookup"><span data-stu-id="cb845-482">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="cb845-483">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="cb845-483">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="cb845-484">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="cb845-484">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="cb845-485">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="cb845-485">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="cb845-486">モード</span><span class="sxs-lookup"><span data-stu-id="cb845-486">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="cb845-487">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="cb845-487">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="cb845-488">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="cb845-488">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="cb845-489">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="cb845-489">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="cb845-490">値</span><span class="sxs-lookup"><span data-stu-id="cb845-490">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="cb845-491">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="cb845-491">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="cb845-492">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="cb845-492">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="cb845-493">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="cb845-493">Parameters - visible</span></span>

<span data-ttu-id="cb845-494">値</span><span class="sxs-lookup"><span data-stu-id="cb845-494">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="cb845-495">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="cb845-495">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="cb845-496">メソッド width</span><span class="sxs-lookup"><span data-stu-id="cb845-496">Method width</span></span>

<span data-ttu-id="cb845-497">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-497">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="cb845-498">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="cb845-498">Parameters - width</span></span>

<span data-ttu-id="cb845-499">値</span><span class="sxs-lookup"><span data-stu-id="cb845-499">value</span></span>  

<!-- -->

<span data-ttu-id="cb845-500">モード</span><span class="sxs-lookup"><span data-stu-id="cb845-500">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="cb845-501">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="cb845-501">Return Value - width</span></span>

<span data-ttu-id="cb845-502">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="cb845-502">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="cb845-503">備考 - width</span><span class="sxs-lookup"><span data-stu-id="cb845-503">Remarks - width</span></span>

<span data-ttu-id="cb845-504">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-504">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="cb845-505">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="cb845-505">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="cb845-506">モード。</span><span class="sxs-lookup"><span data-stu-id="cb845-506">Mode.</span></span>           | <span data-ttu-id="cb845-507">幅計算。</span><span class="sxs-lookup"><span data-stu-id="cb845-507">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb845-508">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="cb845-508">-1 Exact.</span></span>       | <span data-ttu-id="cb845-509">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-509">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="cb845-510">0 自動。</span><span class="sxs-lookup"><span data-stu-id="cb845-510">0 Auto.</span></span>         | <span data-ttu-id="cb845-511">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-511">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="cb845-512">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="cb845-512">1 Column width.</span></span> | <span data-ttu-id="cb845-513">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="cb845-513">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="cb845-514">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="cb845-514">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="cb845-515">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="cb845-515">Method widthMode</span></span>

<span data-ttu-id="cb845-516">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-516">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="cb845-517">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="cb845-517">Parameters - widthMode</span></span>

<span data-ttu-id="cb845-518">値</span><span class="sxs-lookup"><span data-stu-id="cb845-518">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="cb845-519">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="cb845-519">Return Value - widthMode</span></span>

<span data-ttu-id="cb845-520">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="cb845-520">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="cb845-521">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="cb845-521">Remarks - widthMode</span></span>

<span data-ttu-id="cb845-522">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="cb845-522">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="cb845-523">モード。</span><span class="sxs-lookup"><span data-stu-id="cb845-523">Mode.</span></span>         | <span data-ttu-id="cb845-524">幅計算。</span><span class="sxs-lookup"><span data-stu-id="cb845-524">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb845-525">正確。</span><span class="sxs-lookup"><span data-stu-id="cb845-525">Exact.</span></span>        | <span data-ttu-id="cb845-526">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-526">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="cb845-527">自動。</span><span class="sxs-lookup"><span data-stu-id="cb845-527">Auto.</span></span>         | <span data-ttu-id="cb845-528">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cb845-528">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="cb845-529">列の幅。</span><span class="sxs-lookup"><span data-stu-id="cb845-529">Column width.</span></span> | <span data-ttu-id="cb845-530">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="cb845-530">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="cb845-531">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="cb845-531">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="cb845-532">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="cb845-532">Method widthValue</span></span>

<span data-ttu-id="cb845-533">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cb845-533">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="cb845-534">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="cb845-534">Parameters - widthValue</span></span>

<span data-ttu-id="cb845-535">値</span><span class="sxs-lookup"><span data-stu-id="cb845-535">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="cb845-536">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="cb845-536">Return Value - widthValue</span></span>

<span data-ttu-id="cb845-537">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="cb845-537">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="cb845-538">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="cb845-538">Remarks - widthValue</span></span>

<span data-ttu-id="cb845-539">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cb845-539">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="cb845-540">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="cb845-540">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="cb845-541">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="cb845-541">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="cb845-542">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="cb845-542">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="cb845-543">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="cb845-543">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="cb845-544">overrideObject</span><span class="sxs-lookup"><span data-stu-id="cb845-544">overrideObject</span></span>  

