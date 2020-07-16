---
title: FormBuildProgressControl クラス
description: このトピックでは、FormBuildProgressControl クラスについて説明します。
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
ms.openlocfilehash: 174338dcbcfcfc6d6b0942e7b9d527668dfe1d3a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502959"
---
# <a name="class-formbuildprogresscontrol"></a><span data-ttu-id="652fa-103">クラス FormBuildProgressControl</span><span class="sxs-lookup"><span data-stu-id="652fa-103">Class FormBuildProgressControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildProgressControl extends FormBuildControl
```

<span data-ttu-id="652fa-104">FormBuildProgressControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="652fa-104">The FormBuildProgressControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="652fa-105">備考</span><span class="sxs-lookup"><span data-stu-id="652fa-105">Remarks</span></span>

<span data-ttu-id="652fa-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="652fa-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="652fa-107">例</span><span class="sxs-lookup"><span data-stu-id="652fa-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="652fa-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="652fa-108">Methods</span></span>

| <span data-ttu-id="652fa-109">方法</span><span class="sxs-lookup"><span data-stu-id="652fa-109">Method</span></span>                                                                                                      | <span data-ttu-id="652fa-110">説明</span><span class="sxs-lookup"><span data-stu-id="652fa-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="652fa-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="652fa-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="652fa-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="652fa-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="652fa-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="652fa-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="652fa-117">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-117">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="652fa-118">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-118">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="652fa-119">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="652fa-119">public int containerId()</span></span>                                                                                    | <span data-ttu-id="652fa-120">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="652fa-120">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="652fa-121">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-121">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="652fa-122">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-122">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="652fa-123">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-123">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="652fa-124">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-124">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="652fa-125">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-125">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="652fa-126">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-126">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="652fa-127">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-127">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="652fa-128">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-128">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="652fa-129">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="652fa-129">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="652fa-130">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-130">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="652fa-131">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-131">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="652fa-132">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-132">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="652fa-133">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-133">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="652fa-134">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-134">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="652fa-135">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-135">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="652fa-136">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-136">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="652fa-137">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-137">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="652fa-138">public int id()</span><span class="sxs-lookup"><span data-stu-id="652fa-138">public int id()</span></span>                                                                                             | <span data-ttu-id="652fa-139">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="652fa-139">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="652fa-140">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="652fa-140">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="652fa-141">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="652fa-141">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="652fa-142">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="652fa-142">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="652fa-143">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-143">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="652fa-144">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-144">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="652fa-145">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-145">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="652fa-146">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-146">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="652fa-147">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-147">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="652fa-148">public int pos(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-148">public int pos(\[int value\])</span></span>                                                                               |                                                                                                                                         |
| <span data-ttu-id="652fa-149">public int progressType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-149">public int progressType(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="652fa-150">public int rangeHi(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-150">public int rangeHi(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="652fa-151">public int rangeLo(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-151">public int rangeLo(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="652fa-152">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-152">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="652fa-153">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-153">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="652fa-154">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="652fa-154">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="652fa-155">public int step(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-155">public int step(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="652fa-156">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-156">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="652fa-157">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="652fa-157">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="652fa-158">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-158">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="652fa-159">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-159">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="652fa-160">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-160">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="652fa-161">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-161">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="652fa-162">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-162">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="652fa-163">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-163">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="652fa-164">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="652fa-164">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="652fa-165">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="652fa-165">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="652fa-166">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-166">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="652fa-167">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-167">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="652fa-168">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="652fa-168">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="652fa-169">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-169">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="652fa-170">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-170">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="652fa-171">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-171">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="652fa-172">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="652fa-172">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="652fa-173">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-173">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="652fa-174">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="652fa-174">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="652fa-175">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="652fa-175">Method alignControl</span></span>

<span data-ttu-id="652fa-176">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-176">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="652fa-177">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="652fa-177">Parameters - alignControl</span></span>

<span data-ttu-id="652fa-178">値</span><span class="sxs-lookup"><span data-stu-id="652fa-178">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="652fa-179">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="652fa-179">Return Value - alignControl</span></span>

<span data-ttu-id="652fa-180">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="652fa-180">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="652fa-181">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="652fa-181">Remarks - alignControl</span></span>

<span data-ttu-id="652fa-182">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-182">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="652fa-183">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="652fa-183">Method allowEdit</span></span>

<span data-ttu-id="652fa-184">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-184">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="652fa-185">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="652fa-185">Parameters - allowEdit</span></span>

<span data-ttu-id="652fa-186">値</span><span class="sxs-lookup"><span data-stu-id="652fa-186">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="652fa-187">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="652fa-187">Return Value - allowEdit</span></span>

<span data-ttu-id="652fa-188">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="652fa-188">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="652fa-189">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="652fa-189">Remarks - allowEdit</span></span>

<span data-ttu-id="652fa-190">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="652fa-190">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="652fa-191">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="652fa-191">Method autoDeclaration</span></span>

<span data-ttu-id="652fa-192">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-192">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="652fa-193">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="652fa-193">Parameters - autoDeclaration</span></span>

<span data-ttu-id="652fa-194">値</span><span class="sxs-lookup"><span data-stu-id="652fa-194">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="652fa-195">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="652fa-195">Return Value - autoDeclaration</span></span>

<span data-ttu-id="652fa-196">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="652fa-196">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="652fa-197">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="652fa-197">Remarks - autoDeclaration</span></span>

<span data-ttu-id="652fa-198">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="652fa-198">Controls cannot have identical names.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="652fa-199">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="652fa-199">Method configurationKey</span></span>

<span data-ttu-id="652fa-200">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-200">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="652fa-201">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="652fa-201">Parameters - configurationKey</span></span>

<span data-ttu-id="652fa-202">値</span><span class="sxs-lookup"><span data-stu-id="652fa-202">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="652fa-203">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="652fa-203">Return Value - configurationKey</span></span>

<span data-ttu-id="652fa-204">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="652fa-204">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="652fa-205">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="652fa-205">Remarks - configurationKey</span></span>

<span data-ttu-id="652fa-206">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-206">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="652fa-207">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="652fa-207">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="652fa-208">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="652fa-208">Method containerId</span></span>

<span data-ttu-id="652fa-209">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="652fa-209">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="652fa-210">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="652fa-210">Return Value - containerId</span></span>

<span data-ttu-id="652fa-211">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="652fa-211">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="652fa-212">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="652fa-212">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="652fa-213">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="652fa-213">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="652fa-214">値</span><span class="sxs-lookup"><span data-stu-id="652fa-214">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="652fa-215">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="652fa-215">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="652fa-216">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="652fa-216">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="652fa-217">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="652fa-217">Parameters - dataRelationPath</span></span>

<span data-ttu-id="652fa-218">値</span><span class="sxs-lookup"><span data-stu-id="652fa-218">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="652fa-219">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="652fa-219">Return Value - dataRelationPath</span></span>

## <a name="method-direction"></a><span data-ttu-id="652fa-220">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="652fa-220">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="652fa-221">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="652fa-221">Parameters - direction</span></span>

<span data-ttu-id="652fa-222">値</span><span class="sxs-lookup"><span data-stu-id="652fa-222">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="652fa-223">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="652fa-223">Return Value - direction</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="652fa-224">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="652fa-224">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="652fa-225">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="652fa-225">Parameters - displayTarget</span></span>

<span data-ttu-id="652fa-226">値</span><span class="sxs-lookup"><span data-stu-id="652fa-226">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="652fa-227">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="652fa-227">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="652fa-228">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="652fa-228">Method dragDrop</span></span>

<span data-ttu-id="652fa-229">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-229">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="652fa-230">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="652fa-230">Parameters - dragDrop</span></span>

<span data-ttu-id="652fa-231">値</span><span class="sxs-lookup"><span data-stu-id="652fa-231">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="652fa-232">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="652fa-232">Return Value - dragDrop</span></span>

<span data-ttu-id="652fa-233">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="652fa-233">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="652fa-234">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="652fa-234">Method enabled</span></span>

<span data-ttu-id="652fa-235">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-235">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="652fa-236">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="652fa-236">Parameters - enabled</span></span>

<span data-ttu-id="652fa-237">値</span><span class="sxs-lookup"><span data-stu-id="652fa-237">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="652fa-238">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="652fa-238">Return Value - enabled</span></span>

<span data-ttu-id="652fa-239">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="652fa-239">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="652fa-240">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="652fa-240">Remarks - enabled</span></span>

<span data-ttu-id="652fa-241">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="652fa-241">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="652fa-242">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="652fa-242">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="652fa-243">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="652fa-243">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="652fa-244">メソッド height</span><span class="sxs-lookup"><span data-stu-id="652fa-244">Method height</span></span>

<span data-ttu-id="652fa-245">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-245">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="652fa-246">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="652fa-246">Parameters - height</span></span>

<span data-ttu-id="652fa-247">値</span><span class="sxs-lookup"><span data-stu-id="652fa-247">value</span></span>  

<!-- -->

<span data-ttu-id="652fa-248">モード</span><span class="sxs-lookup"><span data-stu-id="652fa-248">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="652fa-249">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="652fa-249">Return Value - height</span></span>

<span data-ttu-id="652fa-250">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="652fa-250">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="652fa-251">備考 - height</span><span class="sxs-lookup"><span data-stu-id="652fa-251">Remarks - height</span></span>

<span data-ttu-id="652fa-252">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-252">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="652fa-253">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="652fa-253">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="652fa-254">モード。</span><span class="sxs-lookup"><span data-stu-id="652fa-254">Mode.</span></span>            | <span data-ttu-id="652fa-255">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="652fa-255">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="652fa-256">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="652fa-256">-1 Exact.</span></span>        | <span data-ttu-id="652fa-257">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-257">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="652fa-258">0 自動。</span><span class="sxs-lookup"><span data-stu-id="652fa-258">0 Auto.</span></span>          | <span data-ttu-id="652fa-259">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-259">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="652fa-260">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="652fa-260">1 Column height.</span></span> | <span data-ttu-id="652fa-261">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="652fa-261">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="652fa-262">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="652fa-262">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="652fa-263">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="652fa-263">Method heightMode</span></span>

<span data-ttu-id="652fa-264">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-264">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="652fa-265">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="652fa-265">Parameters - heightMode</span></span>

<span data-ttu-id="652fa-266">値</span><span class="sxs-lookup"><span data-stu-id="652fa-266">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="652fa-267">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="652fa-267">Return Value - heightMode</span></span>

<span data-ttu-id="652fa-268">計算モード。</span><span class="sxs-lookup"><span data-stu-id="652fa-268">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="652fa-269">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="652fa-269">Remarks - heightMode</span></span>

<span data-ttu-id="652fa-270">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="652fa-270">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="652fa-271">モード。</span><span class="sxs-lookup"><span data-stu-id="652fa-271">Mode.</span></span>          | <span data-ttu-id="652fa-272">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="652fa-272">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="652fa-273">正確。</span><span class="sxs-lookup"><span data-stu-id="652fa-273">Exact.</span></span>         | <span data-ttu-id="652fa-274">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-274">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="652fa-275">自動。</span><span class="sxs-lookup"><span data-stu-id="652fa-275">Auto.</span></span>          | <span data-ttu-id="652fa-276">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-276">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="652fa-277">列の高さ</span><span class="sxs-lookup"><span data-stu-id="652fa-277">Column height.</span></span> | <span data-ttu-id="652fa-278">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="652fa-278">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="652fa-279">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="652fa-279">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="652fa-280">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="652fa-280">Method heightValue</span></span>

<span data-ttu-id="652fa-281">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-281">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="652fa-282">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="652fa-282">Parameters - heightValue</span></span>

<span data-ttu-id="652fa-283">値</span><span class="sxs-lookup"><span data-stu-id="652fa-283">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="652fa-284">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="652fa-284">Return Value - heightValue</span></span>

<span data-ttu-id="652fa-285">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="652fa-285">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="652fa-286">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="652fa-286">Remarks - heightValue</span></span>

<span data-ttu-id="652fa-287">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="652fa-287">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="652fa-288">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="652fa-288">Method helpText</span></span>

<span data-ttu-id="652fa-289">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-289">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="652fa-290">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="652fa-290">Parameters - helpText</span></span>

<span data-ttu-id="652fa-291">値</span><span class="sxs-lookup"><span data-stu-id="652fa-291">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="652fa-292">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="652fa-292">Return Value - helpText</span></span>

<span data-ttu-id="652fa-293">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="652fa-293">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="652fa-294">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="652fa-294">Remarks - helpText</span></span>

<span data-ttu-id="652fa-295">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-295">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="652fa-296">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="652fa-296">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="652fa-297">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="652fa-297">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="652fa-298">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="652fa-298">Parameters - hierarchyParent</span></span>

<span data-ttu-id="652fa-299">値</span><span class="sxs-lookup"><span data-stu-id="652fa-299">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="652fa-300">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="652fa-300">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="652fa-301">メソッド id</span><span class="sxs-lookup"><span data-stu-id="652fa-301">Method id</span></span>

<span data-ttu-id="652fa-302">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="652fa-302">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="652fa-303">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="652fa-303">Return Value - id</span></span>

<span data-ttu-id="652fa-304">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="652fa-304">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="652fa-305">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="652fa-305">Method isContainer</span></span>

<span data-ttu-id="652fa-306">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="652fa-306">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="652fa-307">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="652fa-307">Return Value - isContainer</span></span>

<span data-ttu-id="652fa-308">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="652fa-308">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="652fa-309">メソッド left</span><span class="sxs-lookup"><span data-stu-id="652fa-309">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="652fa-310">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="652fa-310">Parameters - left</span></span>

<span data-ttu-id="652fa-311">値</span><span class="sxs-lookup"><span data-stu-id="652fa-311">value</span></span>  

<!-- -->

<span data-ttu-id="652fa-312">モード</span><span class="sxs-lookup"><span data-stu-id="652fa-312">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="652fa-313">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="652fa-313">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="652fa-314">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="652fa-314">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="652fa-315">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="652fa-315">Parameters - leftMode</span></span>

<span data-ttu-id="652fa-316">値</span><span class="sxs-lookup"><span data-stu-id="652fa-316">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="652fa-317">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="652fa-317">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="652fa-318">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="652fa-318">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="652fa-319">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="652fa-319">Parameters - leftValue</span></span>

<span data-ttu-id="652fa-320">値</span><span class="sxs-lookup"><span data-stu-id="652fa-320">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="652fa-321">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="652fa-321">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="652fa-322">メソッド名</span><span class="sxs-lookup"><span data-stu-id="652fa-322">Method name</span></span>

<span data-ttu-id="652fa-323">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-323">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="652fa-324">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="652fa-324">Parameters - name</span></span>

<span data-ttu-id="652fa-325">値</span><span class="sxs-lookup"><span data-stu-id="652fa-325">value</span></span>  
<span data-ttu-id="652fa-326">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="652fa-326">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="652fa-327">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="652fa-327">Return Value - name</span></span>

<span data-ttu-id="652fa-328">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="652fa-328">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="652fa-329">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="652fa-329">Remarks - name</span></span>

<span data-ttu-id="652fa-330">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="652fa-330">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="652fa-331">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="652fa-331">It must start with a letter.</span></span>
-   <span data-ttu-id="652fa-332">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="652fa-332">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="652fa-333">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="652fa-333">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="652fa-334">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="652fa-334">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="652fa-335">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="652fa-335">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="652fa-336">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="652fa-336">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="652fa-337">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="652fa-337">Parameters - neededPermission</span></span>

<span data-ttu-id="652fa-338">値</span><span class="sxs-lookup"><span data-stu-id="652fa-338">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="652fa-339">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="652fa-339">Return Value - neededPermission</span></span>

## <a name="method-pos"></a><span data-ttu-id="652fa-340">メソッド pos</span><span class="sxs-lookup"><span data-stu-id="652fa-340">Method pos</span></span>

```xpp
public int pos([int value])
```

### <a name="parameters---pos"></a><span data-ttu-id="652fa-341">パラメーター - pos</span><span class="sxs-lookup"><span data-stu-id="652fa-341">Parameters - pos</span></span>

<span data-ttu-id="652fa-342">値</span><span class="sxs-lookup"><span data-stu-id="652fa-342">value</span></span>  

### <a name="return-value---pos"></a><span data-ttu-id="652fa-343">戻り値 - pos</span><span class="sxs-lookup"><span data-stu-id="652fa-343">Return Value - pos</span></span>

## <a name="method-progresstype"></a><span data-ttu-id="652fa-344">メソッド progressType</span><span class="sxs-lookup"><span data-stu-id="652fa-344">Method progressType</span></span>

```xpp
public int progressType([int value])
```

### <a name="parameters---progresstype"></a><span data-ttu-id="652fa-345">パラメーター - progressType</span><span class="sxs-lookup"><span data-stu-id="652fa-345">Parameters - progressType</span></span>

<span data-ttu-id="652fa-346">値</span><span class="sxs-lookup"><span data-stu-id="652fa-346">value</span></span>  

### <a name="return-value---progresstype"></a><span data-ttu-id="652fa-347">戻り値 - progressType</span><span class="sxs-lookup"><span data-stu-id="652fa-347">Return Value - progressType</span></span>

## <a name="method-rangehi"></a><span data-ttu-id="652fa-348">メソッド rangeHi</span><span class="sxs-lookup"><span data-stu-id="652fa-348">Method rangeHi</span></span>

```xpp
public int rangeHi([int value])
```

### <a name="parameters---rangehi"></a><span data-ttu-id="652fa-349">パラメーター - rangeHi</span><span class="sxs-lookup"><span data-stu-id="652fa-349">Parameters - rangeHi</span></span>

<span data-ttu-id="652fa-350">値</span><span class="sxs-lookup"><span data-stu-id="652fa-350">value</span></span>  

### <a name="return-value---rangehi"></a><span data-ttu-id="652fa-351">戻り値 - rangeHi</span><span class="sxs-lookup"><span data-stu-id="652fa-351">Return Value - rangeHi</span></span>

## <a name="method-rangelo"></a><span data-ttu-id="652fa-352">メソッド rangeLo</span><span class="sxs-lookup"><span data-stu-id="652fa-352">Method rangeLo</span></span>

```xpp
public int rangeLo([int value])
```

### <a name="parameters---rangelo"></a><span data-ttu-id="652fa-353">パラメーター - rangeLo</span><span class="sxs-lookup"><span data-stu-id="652fa-353">Parameters - rangeLo</span></span>

<span data-ttu-id="652fa-354">値</span><span class="sxs-lookup"><span data-stu-id="652fa-354">value</span></span>  

### <a name="return-value---rangelo"></a><span data-ttu-id="652fa-355">戻り値 - rangeLo</span><span class="sxs-lookup"><span data-stu-id="652fa-355">Return Value - rangeLo</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="652fa-356">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="652fa-356">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="652fa-357">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="652fa-357">Parameters - securityKey</span></span>

<span data-ttu-id="652fa-358">値</span><span class="sxs-lookup"><span data-stu-id="652fa-358">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="652fa-359">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="652fa-359">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="652fa-360">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="652fa-360">Method skip</span></span>

<span data-ttu-id="652fa-361">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="652fa-361">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="652fa-362">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="652fa-362">Parameters - skip</span></span>

<span data-ttu-id="652fa-363">値</span><span class="sxs-lookup"><span data-stu-id="652fa-363">value</span></span>  
<span data-ttu-id="652fa-364">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="652fa-364">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="652fa-365">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="652fa-365">Return Value - skip</span></span>

<span data-ttu-id="652fa-366">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="652fa-366">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-step"></a><span data-ttu-id="652fa-367">メソッド step</span><span class="sxs-lookup"><span data-stu-id="652fa-367">Method step</span></span>

```xpp
public int step([int value])
```

### <a name="parameters---step"></a><span data-ttu-id="652fa-368">パラメーター - step</span><span class="sxs-lookup"><span data-stu-id="652fa-368">Parameters - step</span></span>

<span data-ttu-id="652fa-369">値</span><span class="sxs-lookup"><span data-stu-id="652fa-369">value</span></span>  

### <a name="return-value---step"></a><span data-ttu-id="652fa-370">戻り値 - step</span><span class="sxs-lookup"><span data-stu-id="652fa-370">Return Value - step</span></span>

## <a name="method-style"></a><span data-ttu-id="652fa-371">メソッド style</span><span class="sxs-lookup"><span data-stu-id="652fa-371">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="652fa-372">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="652fa-372">Parameters - style</span></span>

<span data-ttu-id="652fa-373">値</span><span class="sxs-lookup"><span data-stu-id="652fa-373">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="652fa-374">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="652fa-374">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="652fa-375">メソッド top</span><span class="sxs-lookup"><span data-stu-id="652fa-375">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="652fa-376">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="652fa-376">Parameters - top</span></span>

<span data-ttu-id="652fa-377">値</span><span class="sxs-lookup"><span data-stu-id="652fa-377">value</span></span>  

<!-- -->

<span data-ttu-id="652fa-378">モード</span><span class="sxs-lookup"><span data-stu-id="652fa-378">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="652fa-379">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="652fa-379">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="652fa-380">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="652fa-380">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="652fa-381">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="652fa-381">Parameters - topMode</span></span>

<span data-ttu-id="652fa-382">値</span><span class="sxs-lookup"><span data-stu-id="652fa-382">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="652fa-383">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="652fa-383">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="652fa-384">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="652fa-384">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="652fa-385">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="652fa-385">Parameters - topValue</span></span>

<span data-ttu-id="652fa-386">値</span><span class="sxs-lookup"><span data-stu-id="652fa-386">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="652fa-387">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="652fa-387">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="652fa-388">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="652fa-388">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="652fa-389">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="652fa-389">Parameters - type</span></span>

<span data-ttu-id="652fa-390">値</span><span class="sxs-lookup"><span data-stu-id="652fa-390">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="652fa-391">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="652fa-391">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="652fa-392">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="652fa-392">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="652fa-393">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="652fa-393">Parameters - userData</span></span>

<span data-ttu-id="652fa-394">値</span><span class="sxs-lookup"><span data-stu-id="652fa-394">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="652fa-395">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="652fa-395">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="652fa-396">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="652fa-396">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="652fa-397">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="652fa-397">Parameters - userDataItem</span></span>

<span data-ttu-id="652fa-398">値</span><span class="sxs-lookup"><span data-stu-id="652fa-398">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="652fa-399">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="652fa-399">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="652fa-400">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="652fa-400">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="652fa-401">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="652fa-401">Parameters - userDataItems</span></span>

<span data-ttu-id="652fa-402">値</span><span class="sxs-lookup"><span data-stu-id="652fa-402">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="652fa-403">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="652fa-403">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="652fa-404">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="652fa-404">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="652fa-405">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="652fa-405">Parameters - verticalSpacing</span></span>

<span data-ttu-id="652fa-406">値</span><span class="sxs-lookup"><span data-stu-id="652fa-406">value</span></span>  

<!-- -->

<span data-ttu-id="652fa-407">モード</span><span class="sxs-lookup"><span data-stu-id="652fa-407">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="652fa-408">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="652fa-408">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="652fa-409">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="652fa-409">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="652fa-410">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="652fa-410">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="652fa-411">モード</span><span class="sxs-lookup"><span data-stu-id="652fa-411">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="652fa-412">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="652fa-412">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="652fa-413">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="652fa-413">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="652fa-414">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="652fa-414">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="652fa-415">値</span><span class="sxs-lookup"><span data-stu-id="652fa-415">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="652fa-416">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="652fa-416">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="652fa-417">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="652fa-417">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="652fa-418">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="652fa-418">Parameters - visible</span></span>

<span data-ttu-id="652fa-419">値</span><span class="sxs-lookup"><span data-stu-id="652fa-419">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="652fa-420">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="652fa-420">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="652fa-421">メソッド width</span><span class="sxs-lookup"><span data-stu-id="652fa-421">Method width</span></span>

<span data-ttu-id="652fa-422">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-422">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="652fa-423">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="652fa-423">Parameters - width</span></span>

<span data-ttu-id="652fa-424">値</span><span class="sxs-lookup"><span data-stu-id="652fa-424">value</span></span>  

<!-- -->

<span data-ttu-id="652fa-425">モード</span><span class="sxs-lookup"><span data-stu-id="652fa-425">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="652fa-426">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="652fa-426">Return Value - width</span></span>

<span data-ttu-id="652fa-427">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="652fa-427">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="652fa-428">備考 - width</span><span class="sxs-lookup"><span data-stu-id="652fa-428">Remarks - width</span></span>

<span data-ttu-id="652fa-429">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-429">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="652fa-430">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="652fa-430">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="652fa-431">モード。</span><span class="sxs-lookup"><span data-stu-id="652fa-431">Mode.</span></span>           | <span data-ttu-id="652fa-432">幅計算。</span><span class="sxs-lookup"><span data-stu-id="652fa-432">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="652fa-433">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="652fa-433">-1 Exact.</span></span>       | <span data-ttu-id="652fa-434">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-434">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="652fa-435">0 自動。</span><span class="sxs-lookup"><span data-stu-id="652fa-435">0 Auto.</span></span>         | <span data-ttu-id="652fa-436">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-436">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="652fa-437">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="652fa-437">1 Column width.</span></span> | <span data-ttu-id="652fa-438">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="652fa-438">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="652fa-439">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="652fa-439">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="652fa-440">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="652fa-440">Method widthMode</span></span>

<span data-ttu-id="652fa-441">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-441">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="652fa-442">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="652fa-442">Parameters - widthMode</span></span>

<span data-ttu-id="652fa-443">値</span><span class="sxs-lookup"><span data-stu-id="652fa-443">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="652fa-444">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="652fa-444">Return Value - widthMode</span></span>

<span data-ttu-id="652fa-445">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="652fa-445">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="652fa-446">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="652fa-446">Remarks - widthMode</span></span>

<span data-ttu-id="652fa-447">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="652fa-447">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="652fa-448">モード。</span><span class="sxs-lookup"><span data-stu-id="652fa-448">Mode.</span></span>         | <span data-ttu-id="652fa-449">幅計算。</span><span class="sxs-lookup"><span data-stu-id="652fa-449">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="652fa-450">正確。</span><span class="sxs-lookup"><span data-stu-id="652fa-450">Exact.</span></span>        | <span data-ttu-id="652fa-451">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-451">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="652fa-452">自動。</span><span class="sxs-lookup"><span data-stu-id="652fa-452">Auto.</span></span>         | <span data-ttu-id="652fa-453">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="652fa-453">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="652fa-454">列の幅。</span><span class="sxs-lookup"><span data-stu-id="652fa-454">Column width.</span></span> | <span data-ttu-id="652fa-455">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="652fa-455">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="652fa-456">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="652fa-456">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="652fa-457">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="652fa-457">Method widthValue</span></span>

<span data-ttu-id="652fa-458">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="652fa-458">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="652fa-459">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="652fa-459">Parameters - widthValue</span></span>

<span data-ttu-id="652fa-460">値</span><span class="sxs-lookup"><span data-stu-id="652fa-460">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="652fa-461">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="652fa-461">Return Value - widthValue</span></span>

<span data-ttu-id="652fa-462">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="652fa-462">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="652fa-463">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="652fa-463">Remarks - widthValue</span></span>

<span data-ttu-id="652fa-464">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="652fa-464">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="652fa-465">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="652fa-465">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="652fa-466">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="652fa-466">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="652fa-467">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="652fa-467">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="652fa-468">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="652fa-468">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="652fa-469">overrideObject</span><span class="sxs-lookup"><span data-stu-id="652fa-469">overrideObject</span></span>  

