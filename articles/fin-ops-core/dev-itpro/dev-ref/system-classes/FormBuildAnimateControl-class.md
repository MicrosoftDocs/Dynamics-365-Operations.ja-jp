---
title: FormBuildAnimateControl クラス
description: このトピックでは、FormBuildAnimateControl クラスについて説明します。
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
ms.openlocfilehash: 2e391230b5379a216fdfe595b88afb3adff95a2f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502977"
---
# <a name="class-formbuildanimatecontrol"></a><span data-ttu-id="b335b-103">クラス FormBuildAnimateControl</span><span class="sxs-lookup"><span data-stu-id="b335b-103">Class FormBuildAnimateControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildAnimateControl extends FormBuildControl
```

<span data-ttu-id="b335b-104">FormBuildAnimateControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b335b-104">The FormBuildAnimateControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="b335b-105">備考</span><span class="sxs-lookup"><span data-stu-id="b335b-105">Remarks</span></span>

<span data-ttu-id="b335b-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b335b-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="b335b-107">例</span><span class="sxs-lookup"><span data-stu-id="b335b-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b335b-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="b335b-108">Methods</span></span>

| <span data-ttu-id="b335b-109">方法</span><span class="sxs-lookup"><span data-stu-id="b335b-109">Method</span></span>                                                                                                      | <span data-ttu-id="b335b-110">説明</span><span class="sxs-lookup"><span data-stu-id="b335b-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b335b-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="b335b-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="b335b-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="b335b-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="b335b-115">public str animateFile(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-115">public str animateFile(\[str value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="b335b-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="b335b-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="b335b-118">public boolean autoPlay(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-118">public boolean autoPlay(\[boolean value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="b335b-119">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-119">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="b335b-120">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-120">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="b335b-121">public boolean center(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-121">public boolean center(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="b335b-122">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-122">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="b335b-123">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-123">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="b335b-124">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="b335b-124">public int containerId()</span></span>                                                                                    | <span data-ttu-id="b335b-125">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b335b-125">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="b335b-126">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-126">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="b335b-127">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-127">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="b335b-128">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-128">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b335b-129">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-129">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="b335b-130">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-130">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="b335b-131">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-131">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="b335b-132">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-132">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="b335b-133">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b335b-133">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="b335b-134">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-134">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="b335b-135">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-135">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="b335b-136">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-136">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="b335b-137">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-137">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="b335b-138">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-138">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="b335b-139">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-139">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="b335b-140">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-140">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="b335b-141">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-141">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="b335b-142">public int id()</span><span class="sxs-lookup"><span data-stu-id="b335b-142">public int id()</span></span>                                                                                             | <span data-ttu-id="b335b-143">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b335b-143">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="b335b-144">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="b335b-144">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="b335b-145">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b335b-145">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="b335b-146">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b335b-146">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="b335b-147">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-147">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="b335b-148">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-148">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="b335b-149">public int loops(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-149">public int loops(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="b335b-150">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-150">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="b335b-151">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-151">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="b335b-152">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-152">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="b335b-153">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-153">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="b335b-154">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-154">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="b335b-155">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b335b-155">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="b335b-156">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b335b-156">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b335b-157">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-157">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="b335b-158">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-158">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="b335b-159">public boolean transparent(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-159">public boolean transparent(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="b335b-160">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-160">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="b335b-161">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-161">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="b335b-162">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-162">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="b335b-163">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-163">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b335b-164">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b335b-164">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="b335b-165">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b335b-165">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="b335b-166">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-166">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="b335b-167">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-167">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="b335b-168">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b335b-168">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="b335b-169">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-169">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="b335b-170">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-170">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="b335b-171">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-171">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="b335b-172">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b335b-172">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="b335b-173">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-173">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="b335b-174">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="b335b-174">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="b335b-175">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="b335b-175">Method alignControl</span></span>

<span data-ttu-id="b335b-176">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-176">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="b335b-177">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="b335b-177">Parameters - alignControl</span></span>

<span data-ttu-id="b335b-178">値</span><span class="sxs-lookup"><span data-stu-id="b335b-178">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="b335b-179">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="b335b-179">Return Value - alignControl</span></span>

<span data-ttu-id="b335b-180">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="b335b-180">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="b335b-181">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="b335b-181">Remarks - alignControl</span></span>

<span data-ttu-id="b335b-182">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-182">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="b335b-183">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="b335b-183">Method allowEdit</span></span>

<span data-ttu-id="b335b-184">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-184">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="b335b-185">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b335b-185">Parameters - allowEdit</span></span>

<span data-ttu-id="b335b-186">値</span><span class="sxs-lookup"><span data-stu-id="b335b-186">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="b335b-187">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b335b-187">Return Value - allowEdit</span></span>

<span data-ttu-id="b335b-188">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b335b-188">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="b335b-189">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b335b-189">Remarks - allowEdit</span></span>

<span data-ttu-id="b335b-190">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="b335b-190">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-animatefile"></a><span data-ttu-id="b335b-191">メソッド animateFile</span><span class="sxs-lookup"><span data-stu-id="b335b-191">Method animateFile</span></span>

```xpp
public str animateFile([str value])
```

### <a name="parameters---animatefile"></a><span data-ttu-id="b335b-192">パラメーター - animateFile</span><span class="sxs-lookup"><span data-stu-id="b335b-192">Parameters - animateFile</span></span>

<span data-ttu-id="b335b-193">値</span><span class="sxs-lookup"><span data-stu-id="b335b-193">value</span></span>  

### <a name="return-value---animatefile"></a><span data-ttu-id="b335b-194">戻り値 - animateFile</span><span class="sxs-lookup"><span data-stu-id="b335b-194">Return Value - animateFile</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="b335b-195">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b335b-195">Method autoDeclaration</span></span>

<span data-ttu-id="b335b-196">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-196">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="b335b-197">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b335b-197">Parameters - autoDeclaration</span></span>

<span data-ttu-id="b335b-198">値</span><span class="sxs-lookup"><span data-stu-id="b335b-198">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="b335b-199">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b335b-199">Return Value - autoDeclaration</span></span>

<span data-ttu-id="b335b-200">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b335b-200">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="b335b-201">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b335b-201">Remarks - autoDeclaration</span></span>

<span data-ttu-id="b335b-202">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b335b-202">Controls cannot have identical names.</span></span>

## <a name="method-autoplay"></a><span data-ttu-id="b335b-203">メソッド autoPlay</span><span class="sxs-lookup"><span data-stu-id="b335b-203">Method autoPlay</span></span>

```xpp
public boolean autoPlay([boolean value])
```

### <a name="parameters---autoplay"></a><span data-ttu-id="b335b-204">パラメーター - autoPlay</span><span class="sxs-lookup"><span data-stu-id="b335b-204">Parameters - autoPlay</span></span>

<span data-ttu-id="b335b-205">値</span><span class="sxs-lookup"><span data-stu-id="b335b-205">value</span></span>  

### <a name="return-value---autoplay"></a><span data-ttu-id="b335b-206">戻り値 - autoPlay</span><span class="sxs-lookup"><span data-stu-id="b335b-206">Return Value - autoPlay</span></span>

## <a name="method-border"></a><span data-ttu-id="b335b-207">メソッド border</span><span class="sxs-lookup"><span data-stu-id="b335b-207">Method border</span></span>

<span data-ttu-id="b335b-208">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-208">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="b335b-209">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="b335b-209">Parameters - border</span></span>

<span data-ttu-id="b335b-210">値</span><span class="sxs-lookup"><span data-stu-id="b335b-210">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="b335b-211">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="b335b-211">Return Value - border</span></span>

<span data-ttu-id="b335b-212">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="b335b-212">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="b335b-213">備考 - border</span><span class="sxs-lookup"><span data-stu-id="b335b-213">Remarks - border</span></span>

<span data-ttu-id="b335b-214">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b335b-214">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="b335b-215">値です。</span><span class="sxs-lookup"><span data-stu-id="b335b-215">Value.</span></span> | <span data-ttu-id="b335b-216">説明。</span><span class="sxs-lookup"><span data-stu-id="b335b-216">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="b335b-217">0</span><span class="sxs-lookup"><span data-stu-id="b335b-217">0</span></span>      | <span data-ttu-id="b335b-218">自動。</span><span class="sxs-lookup"><span data-stu-id="b335b-218">Auto.</span></span>        |
| <span data-ttu-id="b335b-219">1</span><span class="sxs-lookup"><span data-stu-id="b335b-219">1</span></span>      | <span data-ttu-id="b335b-220">3D。</span><span class="sxs-lookup"><span data-stu-id="b335b-220">3D.</span></span>          |
| <span data-ttu-id="b335b-221">2</span><span class="sxs-lookup"><span data-stu-id="b335b-221">2</span></span>      | <span data-ttu-id="b335b-222">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="b335b-222">Single line.</span></span> |
| <span data-ttu-id="b335b-223">3</span><span class="sxs-lookup"><span data-stu-id="b335b-223">3</span></span>      | <span data-ttu-id="b335b-224">均一。</span><span class="sxs-lookup"><span data-stu-id="b335b-224">Flat.</span></span>        |
| <span data-ttu-id="b335b-225">4</span><span class="sxs-lookup"><span data-stu-id="b335b-225">4</span></span>      | <span data-ttu-id="b335b-226">なし。</span><span class="sxs-lookup"><span data-stu-id="b335b-226">None.</span></span>        |

## <a name="method-center"></a><span data-ttu-id="b335b-227">メソッド center</span><span class="sxs-lookup"><span data-stu-id="b335b-227">Method center</span></span>

```xpp
public boolean center([boolean value])
```

### <a name="parameters---center"></a><span data-ttu-id="b335b-228">パラメーター - center</span><span class="sxs-lookup"><span data-stu-id="b335b-228">Parameters - center</span></span>

<span data-ttu-id="b335b-229">値</span><span class="sxs-lookup"><span data-stu-id="b335b-229">value</span></span>  

### <a name="return-value---center"></a><span data-ttu-id="b335b-230">戻り値 - center</span><span class="sxs-lookup"><span data-stu-id="b335b-230">Return Value - center</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="b335b-231">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="b335b-231">Method configurationKey</span></span>

<span data-ttu-id="b335b-232">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-232">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="b335b-233">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b335b-233">Parameters - configurationKey</span></span>

<span data-ttu-id="b335b-234">値</span><span class="sxs-lookup"><span data-stu-id="b335b-234">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="b335b-235">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b335b-235">Return Value - configurationKey</span></span>

<span data-ttu-id="b335b-236">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="b335b-236">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="b335b-237">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b335b-237">Remarks - configurationKey</span></span>

<span data-ttu-id="b335b-238">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-238">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="b335b-239">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="b335b-239">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="b335b-240">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="b335b-240">Method containerId</span></span>

<span data-ttu-id="b335b-241">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b335b-241">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="b335b-242">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="b335b-242">Return Value - containerId</span></span>

<span data-ttu-id="b335b-243">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="b335b-243">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="b335b-244">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b335b-244">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="b335b-245">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b335b-245">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="b335b-246">値</span><span class="sxs-lookup"><span data-stu-id="b335b-246">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="b335b-247">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b335b-247">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="b335b-248">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b335b-248">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="b335b-249">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b335b-249">Parameters - dataRelationPath</span></span>

<span data-ttu-id="b335b-250">値</span><span class="sxs-lookup"><span data-stu-id="b335b-250">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="b335b-251">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b335b-251">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="b335b-252">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="b335b-252">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="b335b-253">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="b335b-253">Parameters - displayTarget</span></span>

<span data-ttu-id="b335b-254">値</span><span class="sxs-lookup"><span data-stu-id="b335b-254">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="b335b-255">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="b335b-255">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="b335b-256">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="b335b-256">Method dragDrop</span></span>

<span data-ttu-id="b335b-257">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-257">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="b335b-258">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b335b-258">Parameters - dragDrop</span></span>

<span data-ttu-id="b335b-259">値</span><span class="sxs-lookup"><span data-stu-id="b335b-259">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="b335b-260">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b335b-260">Return Value - dragDrop</span></span>

<span data-ttu-id="b335b-261">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="b335b-261">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="b335b-262">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="b335b-262">Method enabled</span></span>

<span data-ttu-id="b335b-263">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-263">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="b335b-264">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="b335b-264">Parameters - enabled</span></span>

<span data-ttu-id="b335b-265">値</span><span class="sxs-lookup"><span data-stu-id="b335b-265">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="b335b-266">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="b335b-266">Return Value - enabled</span></span>

<span data-ttu-id="b335b-267">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b335b-267">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="b335b-268">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="b335b-268">Remarks - enabled</span></span>

<span data-ttu-id="b335b-269">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="b335b-269">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="b335b-270">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b335b-270">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="b335b-271">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b335b-271">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="b335b-272">メソッド height</span><span class="sxs-lookup"><span data-stu-id="b335b-272">Method height</span></span>

<span data-ttu-id="b335b-273">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-273">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="b335b-274">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="b335b-274">Parameters - height</span></span>

<span data-ttu-id="b335b-275">値</span><span class="sxs-lookup"><span data-stu-id="b335b-275">value</span></span>  

<!-- -->

<span data-ttu-id="b335b-276">モード</span><span class="sxs-lookup"><span data-stu-id="b335b-276">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="b335b-277">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="b335b-277">Return Value - height</span></span>

<span data-ttu-id="b335b-278">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="b335b-278">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="b335b-279">備考 - height</span><span class="sxs-lookup"><span data-stu-id="b335b-279">Remarks - height</span></span>

<span data-ttu-id="b335b-280">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-280">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b335b-281">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b335b-281">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b335b-282">モード。</span><span class="sxs-lookup"><span data-stu-id="b335b-282">Mode.</span></span>            | <span data-ttu-id="b335b-283">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b335b-283">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b335b-284">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b335b-284">-1 Exact.</span></span>        | <span data-ttu-id="b335b-285">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-285">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b335b-286">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b335b-286">0 Auto.</span></span>          | <span data-ttu-id="b335b-287">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-287">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b335b-288">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="b335b-288">1 Column height.</span></span> | <span data-ttu-id="b335b-289">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b335b-289">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b335b-290">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b335b-290">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="b335b-291">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="b335b-291">Method heightMode</span></span>

<span data-ttu-id="b335b-292">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-292">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="b335b-293">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="b335b-293">Parameters - heightMode</span></span>

<span data-ttu-id="b335b-294">値</span><span class="sxs-lookup"><span data-stu-id="b335b-294">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="b335b-295">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b335b-295">Return Value - heightMode</span></span>

<span data-ttu-id="b335b-296">計算モード。</span><span class="sxs-lookup"><span data-stu-id="b335b-296">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="b335b-297">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b335b-297">Remarks - heightMode</span></span>

<span data-ttu-id="b335b-298">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b335b-298">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b335b-299">モード。</span><span class="sxs-lookup"><span data-stu-id="b335b-299">Mode.</span></span>          | <span data-ttu-id="b335b-300">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b335b-300">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b335b-301">正確。</span><span class="sxs-lookup"><span data-stu-id="b335b-301">Exact.</span></span>         | <span data-ttu-id="b335b-302">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-302">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b335b-303">自動。</span><span class="sxs-lookup"><span data-stu-id="b335b-303">Auto.</span></span>          | <span data-ttu-id="b335b-304">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-304">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b335b-305">列の高さ</span><span class="sxs-lookup"><span data-stu-id="b335b-305">Column height.</span></span> | <span data-ttu-id="b335b-306">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b335b-306">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b335b-307">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b335b-307">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="b335b-308">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="b335b-308">Method heightValue</span></span>

<span data-ttu-id="b335b-309">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-309">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="b335b-310">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="b335b-310">Parameters - heightValue</span></span>

<span data-ttu-id="b335b-311">値</span><span class="sxs-lookup"><span data-stu-id="b335b-311">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="b335b-312">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b335b-312">Return Value - heightValue</span></span>

<span data-ttu-id="b335b-313">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="b335b-313">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="b335b-314">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b335b-314">Remarks - heightValue</span></span>

<span data-ttu-id="b335b-315">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="b335b-315">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="b335b-316">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="b335b-316">Method helpText</span></span>

<span data-ttu-id="b335b-317">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-317">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="b335b-318">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="b335b-318">Parameters - helpText</span></span>

<span data-ttu-id="b335b-319">値</span><span class="sxs-lookup"><span data-stu-id="b335b-319">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="b335b-320">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="b335b-320">Return Value - helpText</span></span>

<span data-ttu-id="b335b-321">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="b335b-321">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="b335b-322">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="b335b-322">Remarks - helpText</span></span>

<span data-ttu-id="b335b-323">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-323">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="b335b-324">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="b335b-324">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="b335b-325">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b335b-325">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="b335b-326">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b335b-326">Parameters - hierarchyParent</span></span>

<span data-ttu-id="b335b-327">値</span><span class="sxs-lookup"><span data-stu-id="b335b-327">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="b335b-328">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b335b-328">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="b335b-329">メソッド id</span><span class="sxs-lookup"><span data-stu-id="b335b-329">Method id</span></span>

<span data-ttu-id="b335b-330">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b335b-330">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="b335b-331">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="b335b-331">Return Value - id</span></span>

<span data-ttu-id="b335b-332">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="b335b-332">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="b335b-333">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="b335b-333">Method isContainer</span></span>

<span data-ttu-id="b335b-334">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b335b-334">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="b335b-335">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="b335b-335">Return Value - isContainer</span></span>

<span data-ttu-id="b335b-336">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b335b-336">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="b335b-337">メソッド left</span><span class="sxs-lookup"><span data-stu-id="b335b-337">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="b335b-338">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="b335b-338">Parameters - left</span></span>

<span data-ttu-id="b335b-339">値</span><span class="sxs-lookup"><span data-stu-id="b335b-339">value</span></span>  

<!-- -->

<span data-ttu-id="b335b-340">モード</span><span class="sxs-lookup"><span data-stu-id="b335b-340">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="b335b-341">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="b335b-341">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="b335b-342">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="b335b-342">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="b335b-343">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="b335b-343">Parameters - leftMode</span></span>

<span data-ttu-id="b335b-344">値</span><span class="sxs-lookup"><span data-stu-id="b335b-344">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="b335b-345">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="b335b-345">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="b335b-346">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="b335b-346">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="b335b-347">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="b335b-347">Parameters - leftValue</span></span>

<span data-ttu-id="b335b-348">値</span><span class="sxs-lookup"><span data-stu-id="b335b-348">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="b335b-349">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="b335b-349">Return Value - leftValue</span></span>

## <a name="method-loops"></a><span data-ttu-id="b335b-350">メソッド loops</span><span class="sxs-lookup"><span data-stu-id="b335b-350">Method loops</span></span>

```xpp
public int loops([int value])
```

### <a name="parameters---loops"></a><span data-ttu-id="b335b-351">パラメーター - loops</span><span class="sxs-lookup"><span data-stu-id="b335b-351">Parameters - loops</span></span>

<span data-ttu-id="b335b-352">値</span><span class="sxs-lookup"><span data-stu-id="b335b-352">value</span></span>  

### <a name="return-value---loops"></a><span data-ttu-id="b335b-353">戻り値 - loops</span><span class="sxs-lookup"><span data-stu-id="b335b-353">Return Value - loops</span></span>

## <a name="method-name"></a><span data-ttu-id="b335b-354">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b335b-354">Method name</span></span>

<span data-ttu-id="b335b-355">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-355">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="b335b-356">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="b335b-356">Parameters - name</span></span>

<span data-ttu-id="b335b-357">値</span><span class="sxs-lookup"><span data-stu-id="b335b-357">value</span></span>  
<span data-ttu-id="b335b-358">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="b335b-358">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="b335b-359">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b335b-359">Return Value - name</span></span>

<span data-ttu-id="b335b-360">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="b335b-360">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="b335b-361">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="b335b-361">Remarks - name</span></span>

<span data-ttu-id="b335b-362">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b335b-362">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="b335b-363">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b335b-363">It must start with a letter.</span></span>
-   <span data-ttu-id="b335b-364">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="b335b-364">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="b335b-365">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b335b-365">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="b335b-366">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b335b-366">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="b335b-367">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="b335b-367">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="b335b-368">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="b335b-368">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="b335b-369">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="b335b-369">Parameters - neededPermission</span></span>

<span data-ttu-id="b335b-370">値</span><span class="sxs-lookup"><span data-stu-id="b335b-370">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="b335b-371">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="b335b-371">Return Value - neededPermission</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="b335b-372">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="b335b-372">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="b335b-373">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="b335b-373">Parameters - securityKey</span></span>

<span data-ttu-id="b335b-374">値</span><span class="sxs-lookup"><span data-stu-id="b335b-374">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="b335b-375">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="b335b-375">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="b335b-376">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="b335b-376">Method skip</span></span>

<span data-ttu-id="b335b-377">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b335b-377">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="b335b-378">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="b335b-378">Parameters - skip</span></span>

<span data-ttu-id="b335b-379">値</span><span class="sxs-lookup"><span data-stu-id="b335b-379">value</span></span>  
<span data-ttu-id="b335b-380">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="b335b-380">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="b335b-381">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="b335b-381">Return Value - skip</span></span>

<span data-ttu-id="b335b-382">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b335b-382">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-top"></a><span data-ttu-id="b335b-383">メソッド top</span><span class="sxs-lookup"><span data-stu-id="b335b-383">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="b335b-384">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="b335b-384">Parameters - top</span></span>

<span data-ttu-id="b335b-385">値</span><span class="sxs-lookup"><span data-stu-id="b335b-385">value</span></span>  

<!-- -->

<span data-ttu-id="b335b-386">モード</span><span class="sxs-lookup"><span data-stu-id="b335b-386">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="b335b-387">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="b335b-387">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="b335b-388">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="b335b-388">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="b335b-389">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="b335b-389">Parameters - topMode</span></span>

<span data-ttu-id="b335b-390">値</span><span class="sxs-lookup"><span data-stu-id="b335b-390">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="b335b-391">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="b335b-391">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="b335b-392">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="b335b-392">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="b335b-393">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="b335b-393">Parameters - topValue</span></span>

<span data-ttu-id="b335b-394">値</span><span class="sxs-lookup"><span data-stu-id="b335b-394">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="b335b-395">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="b335b-395">Return Value - topValue</span></span>

## <a name="method-transparent"></a><span data-ttu-id="b335b-396">メソッド transparent</span><span class="sxs-lookup"><span data-stu-id="b335b-396">Method transparent</span></span>

```xpp
public boolean transparent([boolean value])
```

### <a name="parameters---transparent"></a><span data-ttu-id="b335b-397">パラメーター - transparent</span><span class="sxs-lookup"><span data-stu-id="b335b-397">Parameters - transparent</span></span>

<span data-ttu-id="b335b-398">値</span><span class="sxs-lookup"><span data-stu-id="b335b-398">value</span></span>  

### <a name="return-value---transparent"></a><span data-ttu-id="b335b-399">戻り値 - transparent</span><span class="sxs-lookup"><span data-stu-id="b335b-399">Return Value - transparent</span></span>

## <a name="method-type"></a><span data-ttu-id="b335b-400">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="b335b-400">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="b335b-401">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="b335b-401">Parameters - type</span></span>

<span data-ttu-id="b335b-402">値</span><span class="sxs-lookup"><span data-stu-id="b335b-402">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="b335b-403">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="b335b-403">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="b335b-404">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="b335b-404">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="b335b-405">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="b335b-405">Parameters - userData</span></span>

<span data-ttu-id="b335b-406">値</span><span class="sxs-lookup"><span data-stu-id="b335b-406">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="b335b-407">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="b335b-407">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="b335b-408">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="b335b-408">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="b335b-409">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="b335b-409">Parameters - userDataItem</span></span>

<span data-ttu-id="b335b-410">値</span><span class="sxs-lookup"><span data-stu-id="b335b-410">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="b335b-411">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="b335b-411">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="b335b-412">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="b335b-412">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="b335b-413">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="b335b-413">Parameters - userDataItems</span></span>

<span data-ttu-id="b335b-414">値</span><span class="sxs-lookup"><span data-stu-id="b335b-414">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="b335b-415">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="b335b-415">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="b335b-416">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b335b-416">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="b335b-417">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b335b-417">Parameters - verticalSpacing</span></span>

<span data-ttu-id="b335b-418">値</span><span class="sxs-lookup"><span data-stu-id="b335b-418">value</span></span>  

<!-- -->

<span data-ttu-id="b335b-419">モード</span><span class="sxs-lookup"><span data-stu-id="b335b-419">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="b335b-420">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b335b-420">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="b335b-421">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b335b-421">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="b335b-422">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b335b-422">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="b335b-423">モード</span><span class="sxs-lookup"><span data-stu-id="b335b-423">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="b335b-424">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b335b-424">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="b335b-425">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b335b-425">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="b335b-426">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b335b-426">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="b335b-427">値</span><span class="sxs-lookup"><span data-stu-id="b335b-427">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="b335b-428">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b335b-428">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="b335b-429">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="b335b-429">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="b335b-430">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="b335b-430">Parameters - visible</span></span>

<span data-ttu-id="b335b-431">値</span><span class="sxs-lookup"><span data-stu-id="b335b-431">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="b335b-432">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="b335b-432">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="b335b-433">メソッド width</span><span class="sxs-lookup"><span data-stu-id="b335b-433">Method width</span></span>

<span data-ttu-id="b335b-434">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-434">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="b335b-435">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="b335b-435">Parameters - width</span></span>

<span data-ttu-id="b335b-436">値</span><span class="sxs-lookup"><span data-stu-id="b335b-436">value</span></span>  

<!-- -->

<span data-ttu-id="b335b-437">モード</span><span class="sxs-lookup"><span data-stu-id="b335b-437">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="b335b-438">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="b335b-438">Return Value - width</span></span>

<span data-ttu-id="b335b-439">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b335b-439">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="b335b-440">備考 - width</span><span class="sxs-lookup"><span data-stu-id="b335b-440">Remarks - width</span></span>

<span data-ttu-id="b335b-441">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-441">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b335b-442">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b335b-442">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b335b-443">モード。</span><span class="sxs-lookup"><span data-stu-id="b335b-443">Mode.</span></span>           | <span data-ttu-id="b335b-444">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b335b-444">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b335b-445">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b335b-445">-1 Exact.</span></span>       | <span data-ttu-id="b335b-446">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-446">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b335b-447">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b335b-447">0 Auto.</span></span>         | <span data-ttu-id="b335b-448">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-448">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b335b-449">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="b335b-449">1 Column width.</span></span> | <span data-ttu-id="b335b-450">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b335b-450">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b335b-451">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b335b-451">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="b335b-452">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="b335b-452">Method widthMode</span></span>

<span data-ttu-id="b335b-453">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-453">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="b335b-454">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b335b-454">Parameters - widthMode</span></span>

<span data-ttu-id="b335b-455">値</span><span class="sxs-lookup"><span data-stu-id="b335b-455">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="b335b-456">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b335b-456">Return Value - widthMode</span></span>

<span data-ttu-id="b335b-457">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b335b-457">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="b335b-458">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b335b-458">Remarks - widthMode</span></span>

<span data-ttu-id="b335b-459">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b335b-459">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b335b-460">モード。</span><span class="sxs-lookup"><span data-stu-id="b335b-460">Mode.</span></span>         | <span data-ttu-id="b335b-461">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b335b-461">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b335b-462">正確。</span><span class="sxs-lookup"><span data-stu-id="b335b-462">Exact.</span></span>        | <span data-ttu-id="b335b-463">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-463">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b335b-464">自動。</span><span class="sxs-lookup"><span data-stu-id="b335b-464">Auto.</span></span>         | <span data-ttu-id="b335b-465">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b335b-465">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b335b-466">列の幅。</span><span class="sxs-lookup"><span data-stu-id="b335b-466">Column width.</span></span> | <span data-ttu-id="b335b-467">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b335b-467">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b335b-468">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b335b-468">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="b335b-469">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="b335b-469">Method widthValue</span></span>

<span data-ttu-id="b335b-470">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b335b-470">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="b335b-471">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b335b-471">Parameters - widthValue</span></span>

<span data-ttu-id="b335b-472">値</span><span class="sxs-lookup"><span data-stu-id="b335b-472">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="b335b-473">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b335b-473">Return Value - widthValue</span></span>

<span data-ttu-id="b335b-474">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b335b-474">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="b335b-475">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b335b-475">Remarks - widthValue</span></span>

<span data-ttu-id="b335b-476">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b335b-476">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="b335b-477">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="b335b-477">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="b335b-478">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="b335b-478">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="b335b-479">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="b335b-479">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="b335b-480">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="b335b-480">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="b335b-481">overrideObject</span><span class="sxs-lookup"><span data-stu-id="b335b-481">overrideObject</span></span>  



