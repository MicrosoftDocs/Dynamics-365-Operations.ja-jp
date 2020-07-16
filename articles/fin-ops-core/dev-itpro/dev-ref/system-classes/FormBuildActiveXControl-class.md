---
title: FormBuildActiveXControl クラス
description: このトピックでは、FormBuildActiveXControl クラスについて説明します。
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
ms.openlocfilehash: 8ba1b1e82ecabae23896c38e1cdd7d0a3f775d2a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502657"
---
# <a name="class-formbuildactivexcontrol"></a><span data-ttu-id="12430-103">クラス FormBuildActiveXControl</span><span class="sxs-lookup"><span data-stu-id="12430-103">Class FormBuildActiveXControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildActiveXControl extends FormBuildControl
```

<span data-ttu-id="12430-104">FormBuildActiveXControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="12430-104">The FormBuildActiveXControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="12430-105">備考</span><span class="sxs-lookup"><span data-stu-id="12430-105">Remarks</span></span>

<span data-ttu-id="12430-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12430-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="12430-107">例</span><span class="sxs-lookup"><span data-stu-id="12430-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="12430-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="12430-108">Methods</span></span>

| <span data-ttu-id="12430-109">方法</span><span class="sxs-lookup"><span data-stu-id="12430-109">Method</span></span>                                                                                                      | <span data-ttu-id="12430-110">説明</span><span class="sxs-lookup"><span data-stu-id="12430-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12430-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="12430-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="12430-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="12430-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="12430-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="12430-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="12430-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="12430-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="12430-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="12430-117">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="12430-117">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="12430-118">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-118">Gets or set the caption of the control.</span></span>                                                                                                 |
| <span data-ttu-id="12430-119">public str className(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="12430-119">public str className(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="12430-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="12430-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="12430-121">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-121">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="12430-122">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="12430-122">public int containerId()</span></span>                                                                                    | <span data-ttu-id="12430-123">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="12430-123">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="12430-124">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="12430-124">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="12430-125">public str custom(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="12430-125">public str custom(\[str value\])</span></span>                                                                            |                                                                                                                                         |
| <span data-ttu-id="12430-126">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="12430-126">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="12430-127">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-127">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="12430-128">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-128">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="12430-129">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-129">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="12430-130">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="12430-130">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="12430-131">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-131">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="12430-132">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="12430-132">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="12430-133">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-133">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="12430-134">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-134">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="12430-135">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-135">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="12430-136">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-136">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="12430-137">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-137">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="12430-138">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="12430-138">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="12430-139">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-139">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="12430-140">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="12430-140">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="12430-141">public int id()</span><span class="sxs-lookup"><span data-stu-id="12430-141">public int id()</span></span>                                                                                             | <span data-ttu-id="12430-142">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="12430-142">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="12430-143">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="12430-143">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="12430-144">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="12430-144">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="12430-145">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="12430-145">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="12430-146">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-146">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="12430-147">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-147">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="12430-148">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="12430-148">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="12430-149">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-149">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="12430-150">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-150">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="12430-151">public boolean rTLCapable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="12430-151">public boolean rTLCapable(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="12430-152">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="12430-152">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="12430-153">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="12430-153">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="12430-154">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="12430-154">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="12430-155">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="12430-155">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="12430-156">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-156">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="12430-157">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-157">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="12430-158">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-158">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="12430-159">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-159">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="12430-160">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-160">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="12430-161">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-161">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="12430-162">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="12430-162">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="12430-163">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="12430-163">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="12430-164">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-164">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="12430-165">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="12430-165">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="12430-166">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="12430-166">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="12430-167">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-167">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="12430-168">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-168">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="12430-169">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-169">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="12430-170">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="12430-170">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="12430-171">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-171">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="12430-172">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="12430-172">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="12430-173">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="12430-173">Method alignControl</span></span>

<span data-ttu-id="12430-174">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-174">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="12430-175">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="12430-175">Parameters - alignControl</span></span>

<span data-ttu-id="12430-176">値</span><span class="sxs-lookup"><span data-stu-id="12430-176">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="12430-177">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="12430-177">Return Value - alignControl</span></span>

<span data-ttu-id="12430-178">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="12430-178">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="12430-179">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="12430-179">Remarks - alignControl</span></span>

<span data-ttu-id="12430-180">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="12430-180">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="12430-181">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="12430-181">Method allowEdit</span></span>

<span data-ttu-id="12430-182">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-182">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="12430-183">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="12430-183">Parameters - allowEdit</span></span>

<span data-ttu-id="12430-184">値</span><span class="sxs-lookup"><span data-stu-id="12430-184">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="12430-185">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="12430-185">Return Value - allowEdit</span></span>

<span data-ttu-id="12430-186">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="12430-186">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="12430-187">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="12430-187">Remarks - allowEdit</span></span>

<span data-ttu-id="12430-188">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="12430-188">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="12430-189">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="12430-189">Method autoDeclaration</span></span>

<span data-ttu-id="12430-190">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-190">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="12430-191">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="12430-191">Parameters - autoDeclaration</span></span>

<span data-ttu-id="12430-192">値</span><span class="sxs-lookup"><span data-stu-id="12430-192">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="12430-193">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="12430-193">Return Value - autoDeclaration</span></span>

<span data-ttu-id="12430-194">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="12430-194">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="12430-195">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="12430-195">Remarks - autoDeclaration</span></span>

<span data-ttu-id="12430-196">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="12430-196">Controls cannot have identical names.</span></span>

## <a name="method-caption"></a><span data-ttu-id="12430-197">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="12430-197">Method caption</span></span>

<span data-ttu-id="12430-198">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-198">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="12430-199">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="12430-199">Parameters - caption</span></span>

<span data-ttu-id="12430-200">値</span><span class="sxs-lookup"><span data-stu-id="12430-200">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="12430-201">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="12430-201">Return Value - caption</span></span>

<span data-ttu-id="12430-202">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="12430-202">The string that is used as the caption of the control.</span></span>

## <a name="method-classname"></a><span data-ttu-id="12430-203">メソッド className</span><span class="sxs-lookup"><span data-stu-id="12430-203">Method className</span></span>

```xpp
public str className([str value])
```

### <a name="parameters---classname"></a><span data-ttu-id="12430-204">パラメーター - className</span><span class="sxs-lookup"><span data-stu-id="12430-204">Parameters - className</span></span>

<span data-ttu-id="12430-205">値</span><span class="sxs-lookup"><span data-stu-id="12430-205">value</span></span>  

### <a name="return-value---classname"></a><span data-ttu-id="12430-206">戻り値 - className</span><span class="sxs-lookup"><span data-stu-id="12430-206">Return Value - className</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="12430-207">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="12430-207">Method configurationKey</span></span>

<span data-ttu-id="12430-208">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-208">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="12430-209">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="12430-209">Parameters - configurationKey</span></span>

<span data-ttu-id="12430-210">値</span><span class="sxs-lookup"><span data-stu-id="12430-210">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="12430-211">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="12430-211">Return Value - configurationKey</span></span>

<span data-ttu-id="12430-212">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="12430-212">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="12430-213">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="12430-213">Remarks - configurationKey</span></span>

<span data-ttu-id="12430-214">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="12430-214">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="12430-215">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="12430-215">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="12430-216">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="12430-216">Method containerId</span></span>

<span data-ttu-id="12430-217">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="12430-217">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="12430-218">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="12430-218">Return Value - containerId</span></span>

<span data-ttu-id="12430-219">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="12430-219">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="12430-220">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="12430-220">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="12430-221">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="12430-221">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="12430-222">値</span><span class="sxs-lookup"><span data-stu-id="12430-222">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="12430-223">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="12430-223">Return Value - countryRegionCodes</span></span>

## <a name="method-custom"></a><span data-ttu-id="12430-224">メソッド custom</span><span class="sxs-lookup"><span data-stu-id="12430-224">Method custom</span></span>

```xpp
public str custom([str value])
```

### <a name="parameters---custom"></a><span data-ttu-id="12430-225">パラメーター - custom</span><span class="sxs-lookup"><span data-stu-id="12430-225">Parameters - custom</span></span>

<span data-ttu-id="12430-226">値</span><span class="sxs-lookup"><span data-stu-id="12430-226">value</span></span>  

### <a name="return-value---custom"></a><span data-ttu-id="12430-227">戻り値 - custom</span><span class="sxs-lookup"><span data-stu-id="12430-227">Return Value - custom</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="12430-228">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="12430-228">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="12430-229">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="12430-229">Parameters - dataRelationPath</span></span>

<span data-ttu-id="12430-230">値</span><span class="sxs-lookup"><span data-stu-id="12430-230">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="12430-231">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="12430-231">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="12430-232">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="12430-232">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="12430-233">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="12430-233">Parameters - displayTarget</span></span>

<span data-ttu-id="12430-234">値</span><span class="sxs-lookup"><span data-stu-id="12430-234">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="12430-235">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="12430-235">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="12430-236">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="12430-236">Method dragDrop</span></span>

<span data-ttu-id="12430-237">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-237">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="12430-238">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="12430-238">Parameters - dragDrop</span></span>

<span data-ttu-id="12430-239">値</span><span class="sxs-lookup"><span data-stu-id="12430-239">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="12430-240">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="12430-240">Return Value - dragDrop</span></span>

<span data-ttu-id="12430-241">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="12430-241">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="12430-242">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="12430-242">Method enabled</span></span>

<span data-ttu-id="12430-243">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="12430-243">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="12430-244">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="12430-244">Parameters - enabled</span></span>

<span data-ttu-id="12430-245">値</span><span class="sxs-lookup"><span data-stu-id="12430-245">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="12430-246">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="12430-246">Return Value - enabled</span></span>

<span data-ttu-id="12430-247">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="12430-247">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="12430-248">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="12430-248">Remarks - enabled</span></span>

<span data-ttu-id="12430-249">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="12430-249">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="12430-250">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="12430-250">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="12430-251">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="12430-251">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="12430-252">メソッド height</span><span class="sxs-lookup"><span data-stu-id="12430-252">Method height</span></span>

<span data-ttu-id="12430-253">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-253">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="12430-254">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="12430-254">Parameters - height</span></span>

<span data-ttu-id="12430-255">値</span><span class="sxs-lookup"><span data-stu-id="12430-255">value</span></span>  

<!-- -->

<span data-ttu-id="12430-256">モード</span><span class="sxs-lookup"><span data-stu-id="12430-256">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="12430-257">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="12430-257">Return Value - height</span></span>

<span data-ttu-id="12430-258">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="12430-258">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="12430-259">備考 - height</span><span class="sxs-lookup"><span data-stu-id="12430-259">Remarks - height</span></span>

<span data-ttu-id="12430-260">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="12430-260">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="12430-261">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="12430-261">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="12430-262">モード。</span><span class="sxs-lookup"><span data-stu-id="12430-262">Mode.</span></span>            | <span data-ttu-id="12430-263">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="12430-263">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="12430-264">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="12430-264">-1 Exact.</span></span>        | <span data-ttu-id="12430-265">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="12430-265">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="12430-266">0 自動。</span><span class="sxs-lookup"><span data-stu-id="12430-266">0 Auto.</span></span>          | <span data-ttu-id="12430-267">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="12430-267">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="12430-268">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="12430-268">1 Column height.</span></span> | <span data-ttu-id="12430-269">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="12430-269">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="12430-270">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="12430-270">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="12430-271">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="12430-271">Method heightMode</span></span>

<span data-ttu-id="12430-272">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-272">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="12430-273">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="12430-273">Parameters - heightMode</span></span>

<span data-ttu-id="12430-274">値</span><span class="sxs-lookup"><span data-stu-id="12430-274">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="12430-275">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="12430-275">Return Value - heightMode</span></span>

<span data-ttu-id="12430-276">計算モード。</span><span class="sxs-lookup"><span data-stu-id="12430-276">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="12430-277">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="12430-277">Remarks - heightMode</span></span>

<span data-ttu-id="12430-278">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="12430-278">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="12430-279">モード。</span><span class="sxs-lookup"><span data-stu-id="12430-279">Mode.</span></span>          | <span data-ttu-id="12430-280">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="12430-280">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="12430-281">正確。</span><span class="sxs-lookup"><span data-stu-id="12430-281">Exact.</span></span>         | <span data-ttu-id="12430-282">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="12430-282">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="12430-283">自動。</span><span class="sxs-lookup"><span data-stu-id="12430-283">Auto.</span></span>          | <span data-ttu-id="12430-284">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="12430-284">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="12430-285">列の高さ</span><span class="sxs-lookup"><span data-stu-id="12430-285">Column height.</span></span> | <span data-ttu-id="12430-286">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="12430-286">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="12430-287">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="12430-287">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="12430-288">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="12430-288">Method heightValue</span></span>

<span data-ttu-id="12430-289">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-289">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="12430-290">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="12430-290">Parameters - heightValue</span></span>

<span data-ttu-id="12430-291">値</span><span class="sxs-lookup"><span data-stu-id="12430-291">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="12430-292">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="12430-292">Return Value - heightValue</span></span>

<span data-ttu-id="12430-293">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="12430-293">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="12430-294">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="12430-294">Remarks - heightValue</span></span>

<span data-ttu-id="12430-295">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="12430-295">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="12430-296">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="12430-296">Method helpText</span></span>

<span data-ttu-id="12430-297">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-297">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="12430-298">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="12430-298">Parameters - helpText</span></span>

<span data-ttu-id="12430-299">値</span><span class="sxs-lookup"><span data-stu-id="12430-299">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="12430-300">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="12430-300">Return Value - helpText</span></span>

<span data-ttu-id="12430-301">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="12430-301">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="12430-302">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="12430-302">Remarks - helpText</span></span>

<span data-ttu-id="12430-303">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-303">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="12430-304">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="12430-304">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="12430-305">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="12430-305">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="12430-306">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="12430-306">Parameters - hierarchyParent</span></span>

<span data-ttu-id="12430-307">値</span><span class="sxs-lookup"><span data-stu-id="12430-307">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="12430-308">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="12430-308">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="12430-309">メソッド id</span><span class="sxs-lookup"><span data-stu-id="12430-309">Method id</span></span>

<span data-ttu-id="12430-310">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="12430-310">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="12430-311">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="12430-311">Return Value - id</span></span>

<span data-ttu-id="12430-312">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="12430-312">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="12430-313">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="12430-313">Method isContainer</span></span>

<span data-ttu-id="12430-314">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="12430-314">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="12430-315">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="12430-315">Return Value - isContainer</span></span>

<span data-ttu-id="12430-316">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="12430-316">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="12430-317">メソッド left</span><span class="sxs-lookup"><span data-stu-id="12430-317">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="12430-318">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="12430-318">Parameters - left</span></span>

<span data-ttu-id="12430-319">値</span><span class="sxs-lookup"><span data-stu-id="12430-319">value</span></span>  

<!-- -->

<span data-ttu-id="12430-320">モード</span><span class="sxs-lookup"><span data-stu-id="12430-320">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="12430-321">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="12430-321">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="12430-322">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="12430-322">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="12430-323">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="12430-323">Parameters - leftMode</span></span>

<span data-ttu-id="12430-324">値</span><span class="sxs-lookup"><span data-stu-id="12430-324">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="12430-325">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="12430-325">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="12430-326">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="12430-326">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="12430-327">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="12430-327">Parameters - leftValue</span></span>

<span data-ttu-id="12430-328">値</span><span class="sxs-lookup"><span data-stu-id="12430-328">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="12430-329">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="12430-329">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="12430-330">メソッド名</span><span class="sxs-lookup"><span data-stu-id="12430-330">Method name</span></span>

<span data-ttu-id="12430-331">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-331">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="12430-332">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="12430-332">Parameters - name</span></span>

<span data-ttu-id="12430-333">値</span><span class="sxs-lookup"><span data-stu-id="12430-333">value</span></span>  
<span data-ttu-id="12430-334">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="12430-334">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="12430-335">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="12430-335">Return Value - name</span></span>

<span data-ttu-id="12430-336">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="12430-336">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="12430-337">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="12430-337">Remarks - name</span></span>

<span data-ttu-id="12430-338">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="12430-338">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="12430-339">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="12430-339">It must start with a letter.</span></span>
-   <span data-ttu-id="12430-340">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="12430-340">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="12430-341">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="12430-341">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="12430-342">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="12430-342">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="12430-343">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="12430-343">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="12430-344">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="12430-344">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="12430-345">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="12430-345">Parameters - neededPermission</span></span>

<span data-ttu-id="12430-346">値</span><span class="sxs-lookup"><span data-stu-id="12430-346">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="12430-347">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="12430-347">Return Value - neededPermission</span></span>

## <a name="method-rtlcapable"></a><span data-ttu-id="12430-348">メソッド rTLCapable</span><span class="sxs-lookup"><span data-stu-id="12430-348">Method rTLCapable</span></span>

```xpp
public boolean rTLCapable([boolean value])
```

### <a name="parameters---rtlcapable"></a><span data-ttu-id="12430-349">パラメーター - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="12430-349">Parameters - rTLCapable</span></span>

<span data-ttu-id="12430-350">値</span><span class="sxs-lookup"><span data-stu-id="12430-350">value</span></span>  

### <a name="return-value---rtlcapable"></a><span data-ttu-id="12430-351">戻り値 - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="12430-351">Return Value - rTLCapable</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="12430-352">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="12430-352">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="12430-353">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="12430-353">Parameters - securityKey</span></span>

<span data-ttu-id="12430-354">値</span><span class="sxs-lookup"><span data-stu-id="12430-354">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="12430-355">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="12430-355">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="12430-356">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="12430-356">Method skip</span></span>

<span data-ttu-id="12430-357">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="12430-357">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="12430-358">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="12430-358">Parameters - skip</span></span>

<span data-ttu-id="12430-359">値</span><span class="sxs-lookup"><span data-stu-id="12430-359">value</span></span>  
<span data-ttu-id="12430-360">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="12430-360">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="12430-361">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="12430-361">Return Value - skip</span></span>

<span data-ttu-id="12430-362">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="12430-362">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-top"></a><span data-ttu-id="12430-363">メソッド top</span><span class="sxs-lookup"><span data-stu-id="12430-363">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="12430-364">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="12430-364">Parameters - top</span></span>

<span data-ttu-id="12430-365">値</span><span class="sxs-lookup"><span data-stu-id="12430-365">value</span></span>  

<!-- -->

<span data-ttu-id="12430-366">モード</span><span class="sxs-lookup"><span data-stu-id="12430-366">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="12430-367">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="12430-367">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="12430-368">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="12430-368">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="12430-369">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="12430-369">Parameters - topMode</span></span>

<span data-ttu-id="12430-370">値</span><span class="sxs-lookup"><span data-stu-id="12430-370">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="12430-371">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="12430-371">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="12430-372">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="12430-372">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="12430-373">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="12430-373">Parameters - topValue</span></span>

<span data-ttu-id="12430-374">値</span><span class="sxs-lookup"><span data-stu-id="12430-374">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="12430-375">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="12430-375">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="12430-376">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="12430-376">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="12430-377">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="12430-377">Parameters - type</span></span>

<span data-ttu-id="12430-378">値</span><span class="sxs-lookup"><span data-stu-id="12430-378">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="12430-379">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="12430-379">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="12430-380">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="12430-380">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="12430-381">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="12430-381">Parameters - userData</span></span>

<span data-ttu-id="12430-382">値</span><span class="sxs-lookup"><span data-stu-id="12430-382">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="12430-383">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="12430-383">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="12430-384">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="12430-384">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="12430-385">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="12430-385">Parameters - userDataItem</span></span>

<span data-ttu-id="12430-386">値</span><span class="sxs-lookup"><span data-stu-id="12430-386">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="12430-387">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="12430-387">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="12430-388">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="12430-388">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="12430-389">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="12430-389">Parameters - userDataItems</span></span>

<span data-ttu-id="12430-390">値</span><span class="sxs-lookup"><span data-stu-id="12430-390">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="12430-391">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="12430-391">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="12430-392">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="12430-392">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="12430-393">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="12430-393">Parameters - verticalSpacing</span></span>

<span data-ttu-id="12430-394">値</span><span class="sxs-lookup"><span data-stu-id="12430-394">value</span></span>  

<!-- -->

<span data-ttu-id="12430-395">モード</span><span class="sxs-lookup"><span data-stu-id="12430-395">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="12430-396">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="12430-396">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="12430-397">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="12430-397">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="12430-398">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="12430-398">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="12430-399">モード</span><span class="sxs-lookup"><span data-stu-id="12430-399">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="12430-400">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="12430-400">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="12430-401">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="12430-401">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="12430-402">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="12430-402">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="12430-403">値</span><span class="sxs-lookup"><span data-stu-id="12430-403">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="12430-404">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="12430-404">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="12430-405">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="12430-405">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="12430-406">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="12430-406">Parameters - visible</span></span>

<span data-ttu-id="12430-407">値</span><span class="sxs-lookup"><span data-stu-id="12430-407">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="12430-408">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="12430-408">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="12430-409">メソッド width</span><span class="sxs-lookup"><span data-stu-id="12430-409">Method width</span></span>

<span data-ttu-id="12430-410">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-410">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="12430-411">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="12430-411">Parameters - width</span></span>

<span data-ttu-id="12430-412">値</span><span class="sxs-lookup"><span data-stu-id="12430-412">value</span></span>  

<!-- -->

<span data-ttu-id="12430-413">モード</span><span class="sxs-lookup"><span data-stu-id="12430-413">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="12430-414">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="12430-414">Return Value - width</span></span>

<span data-ttu-id="12430-415">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="12430-415">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="12430-416">備考 - width</span><span class="sxs-lookup"><span data-stu-id="12430-416">Remarks - width</span></span>

<span data-ttu-id="12430-417">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="12430-417">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="12430-418">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="12430-418">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="12430-419">モード。</span><span class="sxs-lookup"><span data-stu-id="12430-419">Mode.</span></span>           | <span data-ttu-id="12430-420">幅計算。</span><span class="sxs-lookup"><span data-stu-id="12430-420">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12430-421">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="12430-421">-1 Exact.</span></span>       | <span data-ttu-id="12430-422">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="12430-422">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="12430-423">0 自動。</span><span class="sxs-lookup"><span data-stu-id="12430-423">0 Auto.</span></span>         | <span data-ttu-id="12430-424">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="12430-424">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="12430-425">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="12430-425">1 Column width.</span></span> | <span data-ttu-id="12430-426">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="12430-426">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="12430-427">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="12430-427">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="12430-428">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="12430-428">Method widthMode</span></span>

<span data-ttu-id="12430-429">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-429">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="12430-430">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="12430-430">Parameters - widthMode</span></span>

<span data-ttu-id="12430-431">値</span><span class="sxs-lookup"><span data-stu-id="12430-431">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="12430-432">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="12430-432">Return Value - widthMode</span></span>

<span data-ttu-id="12430-433">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="12430-433">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="12430-434">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="12430-434">Remarks - widthMode</span></span>

<span data-ttu-id="12430-435">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="12430-435">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="12430-436">モード。</span><span class="sxs-lookup"><span data-stu-id="12430-436">Mode.</span></span>         | <span data-ttu-id="12430-437">幅計算。</span><span class="sxs-lookup"><span data-stu-id="12430-437">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12430-438">正確。</span><span class="sxs-lookup"><span data-stu-id="12430-438">Exact.</span></span>        | <span data-ttu-id="12430-439">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="12430-439">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="12430-440">自動。</span><span class="sxs-lookup"><span data-stu-id="12430-440">Auto.</span></span>         | <span data-ttu-id="12430-441">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="12430-441">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="12430-442">列の幅。</span><span class="sxs-lookup"><span data-stu-id="12430-442">Column width.</span></span> | <span data-ttu-id="12430-443">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="12430-443">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="12430-444">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="12430-444">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="12430-445">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="12430-445">Method widthValue</span></span>

<span data-ttu-id="12430-446">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="12430-446">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="12430-447">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="12430-447">Parameters - widthValue</span></span>

<span data-ttu-id="12430-448">値</span><span class="sxs-lookup"><span data-stu-id="12430-448">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="12430-449">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="12430-449">Return Value - widthValue</span></span>

<span data-ttu-id="12430-450">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="12430-450">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="12430-451">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="12430-451">Remarks - widthValue</span></span>

<span data-ttu-id="12430-452">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="12430-452">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="12430-453">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="12430-453">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="12430-454">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="12430-454">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="12430-455">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="12430-455">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="12430-456">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="12430-456">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="12430-457">overrideObject</span><span class="sxs-lookup"><span data-stu-id="12430-457">overrideObject</span></span>  

