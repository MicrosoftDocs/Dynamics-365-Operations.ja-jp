---
title: FormBuildButtonSeparatorControl クラス
description: このトピックでは、FormBuildButtonSeparatorControl クラスについて説明します。
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
ms.openlocfilehash: 8019c439d03c9d5ad6fc18127ab42458bc589330
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502975"
---
# <a name="class-formbuildbuttonseparatorcontrol"></a><span data-ttu-id="ee4f7-103">クラス FormBuildButtonSeparatorControl</span><span class="sxs-lookup"><span data-stu-id="ee4f7-103">Class FormBuildButtonSeparatorControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildButtonSeparatorControl extends FormBuildControl
```

<span data-ttu-id="ee4f7-104">FormBuildButtonSeparatorControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-104">The FormBuildButtonSeparatorControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee4f7-105">備考</span><span class="sxs-lookup"><span data-stu-id="ee4f7-105">Remarks</span></span>

<span data-ttu-id="ee4f7-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="ee4f7-107">例</span><span class="sxs-lookup"><span data-stu-id="ee4f7-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ee4f7-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="ee4f7-108">Methods</span></span>

| <span data-ttu-id="ee4f7-109">方法</span><span class="sxs-lookup"><span data-stu-id="ee4f7-109">Method</span></span>                                                                                                      | <span data-ttu-id="ee4f7-110">説明</span><span class="sxs-lookup"><span data-stu-id="ee4f7-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f7-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="ee4f7-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-112">Determines whether to align the control.</span></span>                                                                                                      |
| <span data-ttu-id="ee4f7-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="ee4f7-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-114">Determines whether the user can change the contents of the control.</span></span>                                                                           |
| <span data-ttu-id="ee4f7-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="ee4f7-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="ee4f7-117">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-117">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="ee4f7-118">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-118">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="ee4f7-119">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="ee4f7-119">public int containerId()</span></span>                                                                                    | <span data-ttu-id="ee4f7-120">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-120">Retrieves the ID of the parent container for the control.</span></span>                                                                                     |
| <span data-ttu-id="ee4f7-121">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-121">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="ee4f7-122">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-122">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="ee4f7-123">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-123">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="ee4f7-124">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-124">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="ee4f7-125">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-125">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                             |
| <span data-ttu-id="ee4f7-126">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-126">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="ee4f7-127">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-127">Determines whether to enable or disable the object.</span></span>                                                                                           |
| <span data-ttu-id="ee4f7-128">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-128">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="ee4f7-129">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-129">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="ee4f7-130">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-130">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="ee4f7-131">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-131">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="ee4f7-132">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-132">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="ee4f7-133">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-133">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="ee4f7-134">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-134">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="ee4f7-135">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-135">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="ee4f7-136">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-136">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="ee4f7-137">public int id()</span><span class="sxs-lookup"><span data-stu-id="ee4f7-137">public int id()</span></span>                                                                                             | <span data-ttu-id="ee4f7-138">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-138">Retrieves the ID of the control.</span></span>                                                                                                              |
| <span data-ttu-id="ee4f7-139">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="ee4f7-139">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="ee4f7-140">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-140">Retrieves a value that indicates whether the control is a container control.</span></span>                                                                  |
| <span data-ttu-id="ee4f7-141">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-141">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="ee4f7-142">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-142">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="ee4f7-143">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-143">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="ee4f7-144">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-144">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="ee4f7-145">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-145">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="ee4f7-146">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-146">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="ee4f7-147">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-147">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="ee4f7-148">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-148">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="ee4f7-149">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-149">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="ee4f7-150">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-150">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="ee4f7-151">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-151">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="ee4f7-152">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-152">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="ee4f7-153">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-153">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="ee4f7-154">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-154">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="ee4f7-155">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-155">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="ee4f7-156">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-156">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="ee4f7-157">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-157">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                               |
| <span data-ttu-id="ee4f7-158">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-158">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="ee4f7-159">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-159">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="ee4f7-160">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-160">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="ee4f7-161">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-161">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="ee4f7-162">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-162">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="ee4f7-163">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-163">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="ee4f7-164">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-164">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="ee4f7-165">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-165">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="ee4f7-166">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-166">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="ee4f7-167">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="ee4f7-167">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                               |

## <a name="method-aligncontrol"></a><span data-ttu-id="ee4f7-168">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="ee4f7-168">Method alignControl</span></span>

<span data-ttu-id="ee4f7-169">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-169">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="ee4f7-170">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="ee4f7-170">Parameters - alignControl</span></span>

<span data-ttu-id="ee4f7-171">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-171">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="ee4f7-172">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="ee4f7-172">Return Value - alignControl</span></span>

<span data-ttu-id="ee4f7-173">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-173">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="ee4f7-174">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="ee4f7-174">Remarks - alignControl</span></span>

<span data-ttu-id="ee4f7-175">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-175">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="ee4f7-176">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="ee4f7-176">Method allowEdit</span></span>

<span data-ttu-id="ee4f7-177">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-177">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="ee4f7-178">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ee4f7-178">Parameters - allowEdit</span></span>

<span data-ttu-id="ee4f7-179">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-179">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="ee4f7-180">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ee4f7-180">Return Value - allowEdit</span></span>

<span data-ttu-id="ee4f7-181">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-181">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="ee4f7-182">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ee4f7-182">Remarks - allowEdit</span></span>

<span data-ttu-id="ee4f7-183">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-183">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="ee4f7-184">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee4f7-184">Method autoDeclaration</span></span>

<span data-ttu-id="ee4f7-185">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-185">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="ee4f7-186">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee4f7-186">Parameters - autoDeclaration</span></span>

<span data-ttu-id="ee4f7-187">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-187">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="ee4f7-188">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee4f7-188">Return Value - autoDeclaration</span></span>

<span data-ttu-id="ee4f7-189">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-189">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="ee4f7-190">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee4f7-190">Remarks - autoDeclaration</span></span>

<span data-ttu-id="ee4f7-191">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-191">Controls cannot have identical names.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="ee4f7-192">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="ee4f7-192">Method configurationKey</span></span>

<span data-ttu-id="ee4f7-193">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-193">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="ee4f7-194">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ee4f7-194">Parameters - configurationKey</span></span>

<span data-ttu-id="ee4f7-195">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-195">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="ee4f7-196">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ee4f7-196">Return Value - configurationKey</span></span>

<span data-ttu-id="ee4f7-197">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-197">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="ee4f7-198">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ee4f7-198">Remarks - configurationKey</span></span>

<span data-ttu-id="ee4f7-199">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-199">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="ee4f7-200">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-200">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="ee4f7-201">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="ee4f7-201">Method containerId</span></span>

<span data-ttu-id="ee4f7-202">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-202">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="ee4f7-203">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="ee4f7-203">Return Value - containerId</span></span>

<span data-ttu-id="ee4f7-204">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-204">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="ee4f7-205">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ee4f7-205">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="ee4f7-206">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ee4f7-206">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="ee4f7-207">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-207">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="ee4f7-208">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ee4f7-208">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="ee4f7-209">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ee4f7-209">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="ee4f7-210">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ee4f7-210">Parameters - dataRelationPath</span></span>

<span data-ttu-id="ee4f7-211">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-211">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="ee4f7-212">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ee4f7-212">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="ee4f7-213">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="ee4f7-213">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="ee4f7-214">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="ee4f7-214">Parameters - displayTarget</span></span>

<span data-ttu-id="ee4f7-215">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-215">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="ee4f7-216">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="ee4f7-216">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="ee4f7-217">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="ee4f7-217">Method dragDrop</span></span>

<span data-ttu-id="ee4f7-218">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-218">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="ee4f7-219">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ee4f7-219">Parameters - dragDrop</span></span>

<span data-ttu-id="ee4f7-220">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-220">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="ee4f7-221">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ee4f7-221">Return Value - dragDrop</span></span>

<span data-ttu-id="ee4f7-222">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-222">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="ee4f7-223">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="ee4f7-223">Method enabled</span></span>

<span data-ttu-id="ee4f7-224">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-224">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="ee4f7-225">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="ee4f7-225">Parameters - enabled</span></span>

<span data-ttu-id="ee4f7-226">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-226">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="ee4f7-227">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="ee4f7-227">Return Value - enabled</span></span>

<span data-ttu-id="ee4f7-228">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-228">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="ee4f7-229">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="ee4f7-229">Remarks - enabled</span></span>

<span data-ttu-id="ee4f7-230">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-230">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="ee4f7-231">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-231">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="ee4f7-232">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-232">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="ee4f7-233">メソッド height</span><span class="sxs-lookup"><span data-stu-id="ee4f7-233">Method height</span></span>

<span data-ttu-id="ee4f7-234">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-234">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="ee4f7-235">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="ee4f7-235">Parameters - height</span></span>

<span data-ttu-id="ee4f7-236">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-236">value</span></span>  

<!-- -->

<span data-ttu-id="ee4f7-237">モード</span><span class="sxs-lookup"><span data-stu-id="ee4f7-237">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="ee4f7-238">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="ee4f7-238">Return Value - height</span></span>

<span data-ttu-id="ee4f7-239">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-239">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="ee4f7-240">備考 - height</span><span class="sxs-lookup"><span data-stu-id="ee4f7-240">Remarks - height</span></span>

<span data-ttu-id="ee4f7-241">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-241">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="ee4f7-242">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="ee4f7-242">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="ee4f7-243">モード。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-243">Mode.</span></span>            | <span data-ttu-id="ee4f7-244">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-244">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f7-245">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-245">-1 Exact.</span></span>        | <span data-ttu-id="ee4f7-246">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-246">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ee4f7-247">0 自動。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-247">0 Auto.</span></span>          | <span data-ttu-id="ee4f7-248">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-248">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ee4f7-249">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-249">1 Column height.</span></span> | <span data-ttu-id="ee4f7-250">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-250">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="ee4f7-251">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-251">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="ee4f7-252">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-252">Method heightMode</span></span>

<span data-ttu-id="ee4f7-253">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-253">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="ee4f7-254">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-254">Parameters - heightMode</span></span>

<span data-ttu-id="ee4f7-255">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-255">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="ee4f7-256">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-256">Return Value - heightMode</span></span>

<span data-ttu-id="ee4f7-257">計算モード。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-257">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="ee4f7-258">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-258">Remarks - heightMode</span></span>

<span data-ttu-id="ee4f7-259">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="ee4f7-259">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="ee4f7-260">モード。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-260">Mode.</span></span>          | <span data-ttu-id="ee4f7-261">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-261">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f7-262">正確。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-262">Exact.</span></span>         | <span data-ttu-id="ee4f7-263">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-263">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ee4f7-264">自動。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-264">Auto.</span></span>          | <span data-ttu-id="ee4f7-265">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-265">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ee4f7-266">列の高さ</span><span class="sxs-lookup"><span data-stu-id="ee4f7-266">Column height.</span></span> | <span data-ttu-id="ee4f7-267">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-267">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="ee4f7-268">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-268">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="ee4f7-269">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-269">Method heightValue</span></span>

<span data-ttu-id="ee4f7-270">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-270">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="ee4f7-271">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-271">Parameters - heightValue</span></span>

<span data-ttu-id="ee4f7-272">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-272">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="ee4f7-273">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-273">Return Value - heightValue</span></span>

<span data-ttu-id="ee4f7-274">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-274">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="ee4f7-275">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-275">Remarks - heightValue</span></span>

<span data-ttu-id="ee4f7-276">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-276">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="ee4f7-277">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="ee4f7-277">Method helpText</span></span>

<span data-ttu-id="ee4f7-278">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-278">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="ee4f7-279">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="ee4f7-279">Parameters - helpText</span></span>

<span data-ttu-id="ee4f7-280">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-280">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="ee4f7-281">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="ee4f7-281">Return Value - helpText</span></span>

<span data-ttu-id="ee4f7-282">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-282">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="ee4f7-283">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="ee4f7-283">Remarks - helpText</span></span>

<span data-ttu-id="ee4f7-284">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-284">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="ee4f7-285">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-285">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="ee4f7-286">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ee4f7-286">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="ee4f7-287">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ee4f7-287">Parameters - hierarchyParent</span></span>

<span data-ttu-id="ee4f7-288">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-288">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="ee4f7-289">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ee4f7-289">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="ee4f7-290">メソッド id</span><span class="sxs-lookup"><span data-stu-id="ee4f7-290">Method id</span></span>

<span data-ttu-id="ee4f7-291">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-291">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="ee4f7-292">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="ee4f7-292">Return Value - id</span></span>

<span data-ttu-id="ee4f7-293">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-293">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="ee4f7-294">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="ee4f7-294">Method isContainer</span></span>

<span data-ttu-id="ee4f7-295">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-295">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="ee4f7-296">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="ee4f7-296">Return Value - isContainer</span></span>

<span data-ttu-id="ee4f7-297">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-297">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="ee4f7-298">メソッド left</span><span class="sxs-lookup"><span data-stu-id="ee4f7-298">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="ee4f7-299">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="ee4f7-299">Parameters - left</span></span>

<span data-ttu-id="ee4f7-300">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-300">value</span></span>  

<!-- -->

<span data-ttu-id="ee4f7-301">モード</span><span class="sxs-lookup"><span data-stu-id="ee4f7-301">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="ee4f7-302">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="ee4f7-302">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="ee4f7-303">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-303">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="ee4f7-304">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-304">Parameters - leftMode</span></span>

<span data-ttu-id="ee4f7-305">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-305">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="ee4f7-306">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-306">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="ee4f7-307">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-307">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="ee4f7-308">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-308">Parameters - leftValue</span></span>

<span data-ttu-id="ee4f7-309">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-309">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="ee4f7-310">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-310">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="ee4f7-311">メソッド名</span><span class="sxs-lookup"><span data-stu-id="ee4f7-311">Method name</span></span>

<span data-ttu-id="ee4f7-312">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-312">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="ee4f7-313">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="ee4f7-313">Parameters - name</span></span>

<span data-ttu-id="ee4f7-314">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-314">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="ee4f7-315">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="ee4f7-315">Return Value - name</span></span>

<span data-ttu-id="ee4f7-316">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-316">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="ee4f7-317">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="ee4f7-317">Remarks - name</span></span>

<span data-ttu-id="ee4f7-318">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-318">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="ee4f7-319">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-319">Begins with a letter.</span></span>
-   <span data-ttu-id="ee4f7-320">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-320">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="ee4f7-321">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-321">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="ee4f7-322">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-322">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="ee4f7-323">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-323">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="ee4f7-324">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="ee4f7-324">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="ee4f7-325">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="ee4f7-325">Parameters - neededPermission</span></span>

<span data-ttu-id="ee4f7-326">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-326">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="ee4f7-327">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="ee4f7-327">Return Value - neededPermission</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="ee4f7-328">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="ee4f7-328">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="ee4f7-329">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="ee4f7-329">Parameters - securityKey</span></span>

<span data-ttu-id="ee4f7-330">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-330">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="ee4f7-331">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="ee4f7-331">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="ee4f7-332">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="ee4f7-332">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="ee4f7-333">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="ee4f7-333">Parameters - skip</span></span>

<span data-ttu-id="ee4f7-334">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-334">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="ee4f7-335">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="ee4f7-335">Return Value - skip</span></span>

## <a name="method-text"></a><span data-ttu-id="ee4f7-336">メソッド text</span><span class="sxs-lookup"><span data-stu-id="ee4f7-336">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="ee4f7-337">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="ee4f7-337">Parameters - text</span></span>

<span data-ttu-id="ee4f7-338">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-338">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="ee4f7-339">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="ee4f7-339">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="ee4f7-340">メソッド top</span><span class="sxs-lookup"><span data-stu-id="ee4f7-340">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="ee4f7-341">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="ee4f7-341">Parameters - top</span></span>

<span data-ttu-id="ee4f7-342">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-342">value</span></span>  

<!-- -->

<span data-ttu-id="ee4f7-343">モード</span><span class="sxs-lookup"><span data-stu-id="ee4f7-343">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="ee4f7-344">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="ee4f7-344">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="ee4f7-345">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-345">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="ee4f7-346">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-346">Parameters - topMode</span></span>

<span data-ttu-id="ee4f7-347">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-347">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="ee4f7-348">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-348">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="ee4f7-349">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-349">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="ee4f7-350">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-350">Parameters - topValue</span></span>

<span data-ttu-id="ee4f7-351">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-351">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="ee4f7-352">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-352">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="ee4f7-353">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="ee4f7-353">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="ee4f7-354">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="ee4f7-354">Parameters - type</span></span>

<span data-ttu-id="ee4f7-355">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-355">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="ee4f7-356">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="ee4f7-356">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="ee4f7-357">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="ee4f7-357">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="ee4f7-358">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="ee4f7-358">Parameters - userData</span></span>

<span data-ttu-id="ee4f7-359">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-359">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="ee4f7-360">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="ee4f7-360">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="ee4f7-361">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="ee4f7-361">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="ee4f7-362">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="ee4f7-362">Parameters - userDataItem</span></span>

<span data-ttu-id="ee4f7-363">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-363">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="ee4f7-364">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="ee4f7-364">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="ee4f7-365">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="ee4f7-365">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="ee4f7-366">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="ee4f7-366">Parameters - userDataItems</span></span>

<span data-ttu-id="ee4f7-367">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-367">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="ee4f7-368">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="ee4f7-368">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="ee4f7-369">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ee4f7-369">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="ee4f7-370">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ee4f7-370">Parameters - verticalSpacing</span></span>

<span data-ttu-id="ee4f7-371">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-371">value</span></span>  

<!-- -->

<span data-ttu-id="ee4f7-372">モード</span><span class="sxs-lookup"><span data-stu-id="ee4f7-372">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="ee4f7-373">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ee4f7-373">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="ee4f7-374">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-374">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="ee4f7-375">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-375">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="ee4f7-376">モード</span><span class="sxs-lookup"><span data-stu-id="ee4f7-376">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="ee4f7-377">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-377">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="ee4f7-378">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-378">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="ee4f7-379">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-379">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="ee4f7-380">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-380">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="ee4f7-381">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-381">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="ee4f7-382">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="ee4f7-382">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="ee4f7-383">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="ee4f7-383">Parameters - visible</span></span>

<span data-ttu-id="ee4f7-384">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-384">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="ee4f7-385">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="ee4f7-385">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="ee4f7-386">メソッド width</span><span class="sxs-lookup"><span data-stu-id="ee4f7-386">Method width</span></span>

<span data-ttu-id="ee4f7-387">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-387">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="ee4f7-388">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="ee4f7-388">Parameters - width</span></span>

<span data-ttu-id="ee4f7-389">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-389">value</span></span>  

<!-- -->

<span data-ttu-id="ee4f7-390">モード</span><span class="sxs-lookup"><span data-stu-id="ee4f7-390">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="ee4f7-391">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="ee4f7-391">Return Value - width</span></span>

<span data-ttu-id="ee4f7-392">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-392">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="ee4f7-393">備考 - width</span><span class="sxs-lookup"><span data-stu-id="ee4f7-393">Remarks - width</span></span>

<span data-ttu-id="ee4f7-394">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-394">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="ee4f7-395">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="ee4f7-395">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="ee4f7-396">モード。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-396">Mode.</span></span>           | <span data-ttu-id="ee4f7-397">幅計算。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-397">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f7-398">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-398">-1 Exact.</span></span>       | <span data-ttu-id="ee4f7-399">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-399">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ee4f7-400">0 自動。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-400">0 Auto.</span></span>         | <span data-ttu-id="ee4f7-401">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-401">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ee4f7-402">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-402">1 Column width.</span></span> | <span data-ttu-id="ee4f7-403">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-403">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="ee4f7-404">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-404">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="ee4f7-405">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-405">Method widthMode</span></span>

<span data-ttu-id="ee4f7-406">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-406">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="ee4f7-407">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-407">Parameters - widthMode</span></span>

<span data-ttu-id="ee4f7-408">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-408">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="ee4f7-409">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-409">Return Value - widthMode</span></span>

<span data-ttu-id="ee4f7-410">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-410">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="ee4f7-411">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="ee4f7-411">Remarks - widthMode</span></span>

<span data-ttu-id="ee4f7-412">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="ee4f7-412">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="ee4f7-413">モード。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-413">Mode.</span></span>         | <span data-ttu-id="ee4f7-414">幅計算。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-414">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f7-415">正確。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-415">Exact.</span></span>        | <span data-ttu-id="ee4f7-416">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-416">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ee4f7-417">自動。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-417">Auto.</span></span>         | <span data-ttu-id="ee4f7-418">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-418">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ee4f7-419">列の幅。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-419">Column width.</span></span> | <span data-ttu-id="ee4f7-420">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-420">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="ee4f7-421">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-421">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="ee4f7-422">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-422">Method widthValue</span></span>

<span data-ttu-id="ee4f7-423">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-423">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="ee4f7-424">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-424">Parameters - widthValue</span></span>

<span data-ttu-id="ee4f7-425">値</span><span class="sxs-lookup"><span data-stu-id="ee4f7-425">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="ee4f7-426">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-426">Return Value - widthValue</span></span>

<span data-ttu-id="ee4f7-427">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-427">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="ee4f7-428">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="ee4f7-428">Remarks - widthValue</span></span>

<span data-ttu-id="ee4f7-429">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee4f7-429">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="ee4f7-430">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="ee4f7-430">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="ee4f7-431">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="ee4f7-431">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="ee4f7-432">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="ee4f7-432">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="ee4f7-433">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="ee4f7-433">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="ee4f7-434">overrideObject</span><span class="sxs-lookup"><span data-stu-id="ee4f7-434">overrideObject</span></span>  

