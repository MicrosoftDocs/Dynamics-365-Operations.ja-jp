---
title: FormBuildFastTabSummarySeparator クラス
description: このトピックでは、FormBuildFastTabSummarySeparator クラスについて説明します。
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
ms.openlocfilehash: 22b16d5ae65dec719496d2148aeaff035168cb85
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502651"
---
# <a name="class-formbuildfasttabsummaryseparator"></a><span data-ttu-id="cdb01-103">クラス FormBuildFastTabSummarySeparator</span><span class="sxs-lookup"><span data-stu-id="cdb01-103">Class FormBuildFastTabSummarySeparator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildFastTabSummarySeparator extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="cdb01-104">備考</span><span class="sxs-lookup"><span data-stu-id="cdb01-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="cdb01-105">例</span><span class="sxs-lookup"><span data-stu-id="cdb01-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="cdb01-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="cdb01-106">Methods</span></span>

| <span data-ttu-id="cdb01-107">方法</span><span class="sxs-lookup"><span data-stu-id="cdb01-107">Method</span></span>                                                                                                      | <span data-ttu-id="cdb01-108">説明</span><span class="sxs-lookup"><span data-stu-id="cdb01-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb01-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="cdb01-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-110">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="cdb01-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="cdb01-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-112">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="cdb01-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-113">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="cdb01-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="cdb01-115">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-115">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="cdb01-116">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-116">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="cdb01-117">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-117">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="cdb01-118">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-118">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="cdb01-119">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-119">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="cdb01-120">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-120">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="cdb01-121">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-121">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="cdb01-122">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-122">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="cdb01-123">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-123">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="cdb01-124">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-124">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="cdb01-125">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-125">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="cdb01-126">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-126">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="cdb01-127">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="cdb01-127">public int containerId()</span></span>                                                                                    | <span data-ttu-id="cdb01-128">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-128">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="cdb01-129">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-129">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="cdb01-130">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-130">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="cdb01-131">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-131">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="cdb01-132">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-132">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="cdb01-133">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-133">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="cdb01-134">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-134">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="cdb01-135">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-135">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="cdb01-136">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-136">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="cdb01-137">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-137">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="cdb01-138">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-138">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="cdb01-139">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-139">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="cdb01-140">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-140">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="cdb01-141">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-141">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="cdb01-142">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-142">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="cdb01-143">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-143">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="cdb01-144">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-144">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="cdb01-145">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-145">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="cdb01-146">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-146">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="cdb01-147">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-147">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="cdb01-148">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-148">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="cdb01-149">public int id()</span><span class="sxs-lookup"><span data-stu-id="cdb01-149">public int id()</span></span>                                                                                             | <span data-ttu-id="cdb01-150">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-150">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="cdb01-151">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="cdb01-151">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="cdb01-152">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-152">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="cdb01-153">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-153">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="cdb01-154">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-154">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="cdb01-155">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-155">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="cdb01-156">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-156">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="cdb01-157">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-157">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="cdb01-158">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-158">Gets or sets the name that is used in code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="cdb01-159">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-159">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="cdb01-160">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-160">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="cdb01-161">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-161">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="cdb01-162">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-162">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="cdb01-163">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-163">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="cdb01-164">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-164">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="cdb01-165">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-165">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="cdb01-166">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-166">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="cdb01-167">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-167">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="cdb01-168">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-168">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="cdb01-169">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-169">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="cdb01-170">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-170">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="cdb01-171">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-171">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="cdb01-172">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-172">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="cdb01-173">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-173">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="cdb01-174">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-174">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="cdb01-175">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-175">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="cdb01-176">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-176">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="cdb01-177">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-177">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="cdb01-178">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-178">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="cdb01-179">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-179">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="cdb01-180">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="cdb01-180">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="cdb01-181">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="cdb01-181">Method alignControl</span></span>

<span data-ttu-id="cdb01-182">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-182">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="cdb01-183">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="cdb01-183">Parameters - alignControl</span></span>

<span data-ttu-id="cdb01-184">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-184">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="cdb01-185">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="cdb01-185">Return Value - alignControl</span></span>

<span data-ttu-id="cdb01-186">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="cdb01-186">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="cdb01-187">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="cdb01-187">Remarks - alignControl</span></span>

<span data-ttu-id="cdb01-188">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-188">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="cdb01-189">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="cdb01-189">Method allowEdit</span></span>

<span data-ttu-id="cdb01-190">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-190">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="cdb01-191">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="cdb01-191">Parameters - allowEdit</span></span>

<span data-ttu-id="cdb01-192">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-192">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="cdb01-193">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="cdb01-193">Return Value - allowEdit</span></span>

<span data-ttu-id="cdb01-194">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cdb01-194">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="cdb01-195">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="cdb01-195">Remarks - allowEdit</span></span>

<span data-ttu-id="cdb01-196">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-196">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="cdb01-197">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="cdb01-197">Method autoDeclaration</span></span>

<span data-ttu-id="cdb01-198">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-198">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="cdb01-199">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="cdb01-199">Parameters - autoDeclaration</span></span>

<span data-ttu-id="cdb01-200">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-200">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="cdb01-201">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="cdb01-201">Return Value - autoDeclaration</span></span>

<span data-ttu-id="cdb01-202">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cdb01-202">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="cdb01-203">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="cdb01-203">Remarks - autoDeclaration</span></span>

<span data-ttu-id="cdb01-204">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="cdb01-204">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="cdb01-205">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cdb01-205">Method backgroundColor</span></span>

<span data-ttu-id="cdb01-206">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-206">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="cdb01-207">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cdb01-207">Parameters - backgroundColor</span></span>

<span data-ttu-id="cdb01-208">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-208">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="cdb01-209">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cdb01-209">Return Value - backgroundColor</span></span>

<span data-ttu-id="cdb01-210">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="cdb01-210">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="cdb01-211">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cdb01-211">Remarks - backgroundColor</span></span>

<span data-ttu-id="cdb01-212">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-212">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="cdb01-213">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cdb01-213">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="cdb01-214">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="cdb01-214">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="cdb01-215">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="cdb01-215">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="cdb01-216">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="cdb01-216">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="cdb01-217">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-217">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="cdb01-218">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="cdb01-218">Method backStyle</span></span>

<span data-ttu-id="cdb01-219">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-219">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="cdb01-220">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="cdb01-220">Parameters - backStyle</span></span>

<span data-ttu-id="cdb01-221">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-221">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="cdb01-222">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="cdb01-222">Return Value - backStyle</span></span>

<span data-ttu-id="cdb01-223">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-223">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="cdb01-224">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="cdb01-224">Method bold</span></span>

<span data-ttu-id="cdb01-225">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-225">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="cdb01-226">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="cdb01-226">Parameters - bold</span></span>

<span data-ttu-id="cdb01-227">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-227">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="cdb01-228">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="cdb01-228">Return Value - bold</span></span>

<span data-ttu-id="cdb01-229">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="cdb01-229">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="cdb01-230">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="cdb01-230">Remarks - bold</span></span>

<span data-ttu-id="cdb01-231">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-231">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="cdb01-232">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-232">0 Use the default font weight.</span></span>
-   <span data-ttu-id="cdb01-233">1 シン。</span><span class="sxs-lookup"><span data-stu-id="cdb01-233">1 Thin.</span></span>
-   <span data-ttu-id="cdb01-234">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="cdb01-234">2 Extra-light.</span></span>
-   <span data-ttu-id="cdb01-235">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="cdb01-235">3 Light.</span></span>
-   <span data-ttu-id="cdb01-236">4 標準。</span><span class="sxs-lookup"><span data-stu-id="cdb01-236">4 Normal.</span></span>
-   <span data-ttu-id="cdb01-237">5 中。</span><span class="sxs-lookup"><span data-stu-id="cdb01-237">5 Medium.</span></span>
-   <span data-ttu-id="cdb01-238">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="cdb01-238">6 Semibold.</span></span>
-   <span data-ttu-id="cdb01-239">7 太字。</span><span class="sxs-lookup"><span data-stu-id="cdb01-239">7 Bold.</span></span>
-   <span data-ttu-id="cdb01-240">8 極太。</span><span class="sxs-lookup"><span data-stu-id="cdb01-240">8 Extra-bold.</span></span>
-   <span data-ttu-id="cdb01-241">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="cdb01-241">9 Heavy.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="cdb01-242">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="cdb01-242">Method characterSet</span></span>

<span data-ttu-id="cdb01-243">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-243">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="cdb01-244">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="cdb01-244">Parameters - characterSet</span></span>

<span data-ttu-id="cdb01-245">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-245">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="cdb01-246">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="cdb01-246">Return Value - characterSet</span></span>

<span data-ttu-id="cdb01-247">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="cdb01-247">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="cdb01-248">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="cdb01-248">Remarks - characterSet</span></span>

<span data-ttu-id="cdb01-249">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-249">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="cdb01-250">値です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-250">Value.</span></span> | <span data-ttu-id="cdb01-251">説明。</span><span class="sxs-lookup"><span data-stu-id="cdb01-251">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="cdb01-252">0</span><span class="sxs-lookup"><span data-stu-id="cdb01-252">0</span></span>      | <span data-ttu-id="cdb01-253">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-253">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="cdb01-254">1</span><span class="sxs-lookup"><span data-stu-id="cdb01-254">1</span></span>      | <span data-ttu-id="cdb01-255">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-255">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="cdb01-256">2</span><span class="sxs-lookup"><span data-stu-id="cdb01-256">2</span></span>      | <span data-ttu-id="cdb01-257">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-257">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="cdb01-258">77</span><span class="sxs-lookup"><span data-stu-id="cdb01-258">77</span></span>     | <span data-ttu-id="cdb01-259">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-259">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="cdb01-260">128</span><span class="sxs-lookup"><span data-stu-id="cdb01-260">128</span></span>    | <span data-ttu-id="cdb01-261">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-261">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="cdb01-262">129</span><span class="sxs-lookup"><span data-stu-id="cdb01-262">129</span></span>    | <span data-ttu-id="cdb01-263">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-263">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="cdb01-264">134</span><span class="sxs-lookup"><span data-stu-id="cdb01-264">134</span></span>    | <span data-ttu-id="cdb01-265">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-265">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="cdb01-266">136</span><span class="sxs-lookup"><span data-stu-id="cdb01-266">136</span></span>    | <span data-ttu-id="cdb01-267">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-267">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="cdb01-268">161</span><span class="sxs-lookup"><span data-stu-id="cdb01-268">161</span></span>    | <span data-ttu-id="cdb01-269">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-269">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="cdb01-270">162</span><span class="sxs-lookup"><span data-stu-id="cdb01-270">162</span></span>    | <span data-ttu-id="cdb01-271">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-271">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="cdb01-272">163</span><span class="sxs-lookup"><span data-stu-id="cdb01-272">163</span></span>    | <span data-ttu-id="cdb01-273">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-273">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="cdb01-274">186</span><span class="sxs-lookup"><span data-stu-id="cdb01-274">186</span></span>    | <span data-ttu-id="cdb01-275">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-275">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="cdb01-276">204</span><span class="sxs-lookup"><span data-stu-id="cdb01-276">204</span></span>    | <span data-ttu-id="cdb01-277">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-277">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="cdb01-278">238</span><span class="sxs-lookup"><span data-stu-id="cdb01-278">238</span></span>    | <span data-ttu-id="cdb01-279">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-279">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="cdb01-280">255</span><span class="sxs-lookup"><span data-stu-id="cdb01-280">255</span></span>    | <span data-ttu-id="cdb01-281">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-281">OEM\_CHARSET</span></span>         |

<span data-ttu-id="cdb01-282">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-282">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="cdb01-283">値です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-283">Value.</span></span> | <span data-ttu-id="cdb01-284">説明。</span><span class="sxs-lookup"><span data-stu-id="cdb01-284">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="cdb01-285">130</span><span class="sxs-lookup"><span data-stu-id="cdb01-285">130</span></span>    | <span data-ttu-id="cdb01-286">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-286">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="cdb01-287">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-287">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="cdb01-288">値です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-288">Value.</span></span> | <span data-ttu-id="cdb01-289">説明。</span><span class="sxs-lookup"><span data-stu-id="cdb01-289">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="cdb01-290">177</span><span class="sxs-lookup"><span data-stu-id="cdb01-290">177</span></span>    | <span data-ttu-id="cdb01-291">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-291">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="cdb01-292">178</span><span class="sxs-lookup"><span data-stu-id="cdb01-292">178</span></span>    | <span data-ttu-id="cdb01-293">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-293">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="cdb01-294">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-294">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="cdb01-295">値です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-295">Value.</span></span> | <span data-ttu-id="cdb01-296">説明。</span><span class="sxs-lookup"><span data-stu-id="cdb01-296">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="cdb01-297">222</span><span class="sxs-lookup"><span data-stu-id="cdb01-297">222</span></span>    | <span data-ttu-id="cdb01-298">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="cdb01-298">THAI\_CHARSET</span></span> |

<span data-ttu-id="cdb01-299">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-299">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="cdb01-300">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-300">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="cdb01-301">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdb01-301">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="cdb01-302">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="cdb01-302">Method colorScheme</span></span>

<span data-ttu-id="cdb01-303">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-303">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="cdb01-304">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="cdb01-304">Parameters - colorScheme</span></span>

<span data-ttu-id="cdb01-305">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-305">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="cdb01-306">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="cdb01-306">Return Value - colorScheme</span></span>

<span data-ttu-id="cdb01-307">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="cdb01-307">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="cdb01-308">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="cdb01-308">Remarks - colorScheme</span></span>

<span data-ttu-id="cdb01-309">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-309">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="cdb01-310">値です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-310">Value.</span></span> | <span data-ttu-id="cdb01-311">スタイル。</span><span class="sxs-lookup"><span data-stu-id="cdb01-311">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="cdb01-312">0</span><span class="sxs-lookup"><span data-stu-id="cdb01-312">0</span></span>      | <span data-ttu-id="cdb01-313">既定。</span><span class="sxs-lookup"><span data-stu-id="cdb01-313">Default.</span></span>                       |
| <span data-ttu-id="cdb01-314">1</span><span class="sxs-lookup"><span data-stu-id="cdb01-314">1</span></span>      | <span data-ttu-id="cdb01-315">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="cdb01-315">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="cdb01-316">2</span><span class="sxs-lookup"><span data-stu-id="cdb01-316">2</span></span>      | <span data-ttu-id="cdb01-317">真の配色。</span><span class="sxs-lookup"><span data-stu-id="cdb01-317">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="cdb01-318">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="cdb01-318">Method configurationKey</span></span>

<span data-ttu-id="cdb01-319">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-319">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="cdb01-320">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="cdb01-320">Parameters - configurationKey</span></span>

<span data-ttu-id="cdb01-321">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-321">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="cdb01-322">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="cdb01-322">Return Value - configurationKey</span></span>

<span data-ttu-id="cdb01-323">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="cdb01-323">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="cdb01-324">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="cdb01-324">Remarks - configurationKey</span></span>

<span data-ttu-id="cdb01-325">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-325">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="cdb01-326">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="cdb01-326">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="cdb01-327">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="cdb01-327">Method containerId</span></span>

<span data-ttu-id="cdb01-328">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-328">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="cdb01-329">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="cdb01-329">Return Value - containerId</span></span>

<span data-ttu-id="cdb01-330">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="cdb01-330">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="cdb01-331">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="cdb01-331">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="cdb01-332">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="cdb01-332">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="cdb01-333">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-333">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="cdb01-334">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="cdb01-334">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="cdb01-335">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="cdb01-335">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="cdb01-336">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="cdb01-336">Parameters - dataRelationPath</span></span>

<span data-ttu-id="cdb01-337">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-337">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="cdb01-338">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="cdb01-338">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="cdb01-339">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="cdb01-339">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="cdb01-340">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="cdb01-340">Parameters - displayTarget</span></span>

<span data-ttu-id="cdb01-341">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-341">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="cdb01-342">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="cdb01-342">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="cdb01-343">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="cdb01-343">Method dragDrop</span></span>

<span data-ttu-id="cdb01-344">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-344">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="cdb01-345">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="cdb01-345">Parameters - dragDrop</span></span>

<span data-ttu-id="cdb01-346">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-346">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="cdb01-347">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="cdb01-347">Return Value - dragDrop</span></span>

<span data-ttu-id="cdb01-348">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="cdb01-348">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="cdb01-349">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="cdb01-349">Method enabled</span></span>

<span data-ttu-id="cdb01-350">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-350">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="cdb01-351">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="cdb01-351">Parameters - enabled</span></span>

<span data-ttu-id="cdb01-352">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-352">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="cdb01-353">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="cdb01-353">Return Value - enabled</span></span>

<span data-ttu-id="cdb01-354">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cdb01-354">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="cdb01-355">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="cdb01-355">Remarks - enabled</span></span>

<span data-ttu-id="cdb01-356">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-356">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="cdb01-357">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-357">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="cdb01-358">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-358">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="cdb01-359">メソッド font</span><span class="sxs-lookup"><span data-stu-id="cdb01-359">Method font</span></span>

<span data-ttu-id="cdb01-360">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-360">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="cdb01-361">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="cdb01-361">Parameters - font</span></span>

<span data-ttu-id="cdb01-362">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-362">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="cdb01-363">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="cdb01-363">Return Value - font</span></span>

<span data-ttu-id="cdb01-364">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="cdb01-364">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="cdb01-365">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="cdb01-365">Method fontSize</span></span>

<span data-ttu-id="cdb01-366">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-366">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="cdb01-367">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="cdb01-367">Parameters - fontSize</span></span>

<span data-ttu-id="cdb01-368">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-368">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="cdb01-369">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="cdb01-369">Return Value - fontSize</span></span>

<span data-ttu-id="cdb01-370">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="cdb01-370">The height of the font in points.</span></span>

## <a name="method-height"></a><span data-ttu-id="cdb01-371">メソッド height</span><span class="sxs-lookup"><span data-stu-id="cdb01-371">Method height</span></span>

<span data-ttu-id="cdb01-372">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-372">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="cdb01-373">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="cdb01-373">Parameters - height</span></span>

<span data-ttu-id="cdb01-374">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-374">value</span></span>  

<!-- -->

<span data-ttu-id="cdb01-375">モード</span><span class="sxs-lookup"><span data-stu-id="cdb01-375">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="cdb01-376">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="cdb01-376">Return Value - height</span></span>

<span data-ttu-id="cdb01-377">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="cdb01-377">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="cdb01-378">備考 - height</span><span class="sxs-lookup"><span data-stu-id="cdb01-378">Remarks - height</span></span>

<span data-ttu-id="cdb01-379">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-379">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="cdb01-380">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="cdb01-380">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="cdb01-381">モード。</span><span class="sxs-lookup"><span data-stu-id="cdb01-381">Mode.</span></span>            | <span data-ttu-id="cdb01-382">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="cdb01-382">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb01-383">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="cdb01-383">-1 Exact.</span></span>        | <span data-ttu-id="cdb01-384">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-384">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="cdb01-385">0 自動。</span><span class="sxs-lookup"><span data-stu-id="cdb01-385">0 Auto.</span></span>          | <span data-ttu-id="cdb01-386">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-386">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="cdb01-387">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="cdb01-387">1 Column height.</span></span> | <span data-ttu-id="cdb01-388">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-388">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="cdb01-389">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-389">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="cdb01-390">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-390">Method heightMode</span></span>

<span data-ttu-id="cdb01-391">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-391">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="cdb01-392">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-392">Parameters - heightMode</span></span>

<span data-ttu-id="cdb01-393">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-393">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="cdb01-394">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-394">Return Value - heightMode</span></span>

<span data-ttu-id="cdb01-395">計算モード。</span><span class="sxs-lookup"><span data-stu-id="cdb01-395">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="cdb01-396">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-396">Remarks - heightMode</span></span>

<span data-ttu-id="cdb01-397">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="cdb01-397">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="cdb01-398">モード。</span><span class="sxs-lookup"><span data-stu-id="cdb01-398">Mode.</span></span>          | <span data-ttu-id="cdb01-399">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="cdb01-399">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb01-400">正確。</span><span class="sxs-lookup"><span data-stu-id="cdb01-400">Exact.</span></span>         | <span data-ttu-id="cdb01-401">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-401">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="cdb01-402">自動。</span><span class="sxs-lookup"><span data-stu-id="cdb01-402">Auto.</span></span>          | <span data-ttu-id="cdb01-403">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-403">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="cdb01-404">列の高さ</span><span class="sxs-lookup"><span data-stu-id="cdb01-404">Column height.</span></span> | <span data-ttu-id="cdb01-405">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-405">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="cdb01-406">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-406">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="cdb01-407">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-407">Method heightValue</span></span>

<span data-ttu-id="cdb01-408">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-408">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="cdb01-409">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-409">Parameters - heightValue</span></span>

<span data-ttu-id="cdb01-410">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-410">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="cdb01-411">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-411">Return Value - heightValue</span></span>

<span data-ttu-id="cdb01-412">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="cdb01-412">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="cdb01-413">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-413">Remarks - heightValue</span></span>

<span data-ttu-id="cdb01-414">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="cdb01-414">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="cdb01-415">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="cdb01-415">Method helpText</span></span>

<span data-ttu-id="cdb01-416">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-416">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="cdb01-417">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="cdb01-417">Parameters - helpText</span></span>

<span data-ttu-id="cdb01-418">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-418">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="cdb01-419">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="cdb01-419">Return Value - helpText</span></span>

<span data-ttu-id="cdb01-420">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="cdb01-420">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="cdb01-421">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="cdb01-421">Remarks - helpText</span></span>

<span data-ttu-id="cdb01-422">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-422">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="cdb01-423">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="cdb01-423">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="cdb01-424">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="cdb01-424">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="cdb01-425">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="cdb01-425">Parameters - hierarchyParent</span></span>

<span data-ttu-id="cdb01-426">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-426">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="cdb01-427">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="cdb01-427">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="cdb01-428">メソッド id</span><span class="sxs-lookup"><span data-stu-id="cdb01-428">Method id</span></span>

<span data-ttu-id="cdb01-429">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-429">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="cdb01-430">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="cdb01-430">Return Value - id</span></span>

<span data-ttu-id="cdb01-431">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="cdb01-431">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="cdb01-432">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="cdb01-432">Method isContainer</span></span>

<span data-ttu-id="cdb01-433">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-433">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="cdb01-434">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="cdb01-434">Return Value - isContainer</span></span>

<span data-ttu-id="cdb01-435">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="cdb01-435">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="cdb01-436">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="cdb01-436">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="cdb01-437">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="cdb01-437">Parameters - italic</span></span>

<span data-ttu-id="cdb01-438">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-438">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="cdb01-439">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="cdb01-439">Return Value - italic</span></span>

## <a name="method-left"></a><span data-ttu-id="cdb01-440">メソッド left</span><span class="sxs-lookup"><span data-stu-id="cdb01-440">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="cdb01-441">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="cdb01-441">Parameters - left</span></span>

<span data-ttu-id="cdb01-442">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-442">value</span></span>  

<!-- -->

<span data-ttu-id="cdb01-443">モード</span><span class="sxs-lookup"><span data-stu-id="cdb01-443">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="cdb01-444">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="cdb01-444">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="cdb01-445">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-445">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="cdb01-446">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-446">Parameters - leftMode</span></span>

<span data-ttu-id="cdb01-447">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-447">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="cdb01-448">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-448">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="cdb01-449">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-449">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="cdb01-450">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-450">Parameters - leftValue</span></span>

<span data-ttu-id="cdb01-451">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-451">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="cdb01-452">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-452">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="cdb01-453">メソッド名</span><span class="sxs-lookup"><span data-stu-id="cdb01-453">Method name</span></span>

<span data-ttu-id="cdb01-454">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-454">Gets or sets the name that is used in code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="cdb01-455">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="cdb01-455">Parameters - name</span></span>

<span data-ttu-id="cdb01-456">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-456">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="cdb01-457">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="cdb01-457">Return Value - name</span></span>

<span data-ttu-id="cdb01-458">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="cdb01-458">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="cdb01-459">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="cdb01-459">Remarks - name</span></span>

<span data-ttu-id="cdb01-460">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-460">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="cdb01-461">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-461">It must start with a letter.</span></span>
-   <span data-ttu-id="cdb01-462">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="cdb01-462">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="cdb01-463">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-463">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="cdb01-464">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="cdb01-464">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="cdb01-465">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="cdb01-465">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="cdb01-466">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="cdb01-466">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="cdb01-467">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="cdb01-467">Parameters - neededPermission</span></span>

<span data-ttu-id="cdb01-468">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-468">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="cdb01-469">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="cdb01-469">Return Value - neededPermission</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="cdb01-470">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="cdb01-470">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="cdb01-471">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="cdb01-471">Parameters - securityKey</span></span>

<span data-ttu-id="cdb01-472">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-472">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="cdb01-473">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="cdb01-473">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="cdb01-474">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="cdb01-474">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="cdb01-475">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="cdb01-475">Parameters - skip</span></span>

<span data-ttu-id="cdb01-476">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-476">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="cdb01-477">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="cdb01-477">Return Value - skip</span></span>

## <a name="method-top"></a><span data-ttu-id="cdb01-478">メソッド top</span><span class="sxs-lookup"><span data-stu-id="cdb01-478">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="cdb01-479">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="cdb01-479">Parameters - top</span></span>

<span data-ttu-id="cdb01-480">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-480">value</span></span>  

<!-- -->

<span data-ttu-id="cdb01-481">モード</span><span class="sxs-lookup"><span data-stu-id="cdb01-481">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="cdb01-482">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="cdb01-482">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="cdb01-483">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-483">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="cdb01-484">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-484">Parameters - topMode</span></span>

<span data-ttu-id="cdb01-485">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-485">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="cdb01-486">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-486">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="cdb01-487">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-487">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="cdb01-488">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-488">Parameters - topValue</span></span>

<span data-ttu-id="cdb01-489">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-489">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="cdb01-490">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-490">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="cdb01-491">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="cdb01-491">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="cdb01-492">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="cdb01-492">Parameters - type</span></span>

<span data-ttu-id="cdb01-493">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-493">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="cdb01-494">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="cdb01-494">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="cdb01-495">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="cdb01-495">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="cdb01-496">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="cdb01-496">Parameters - underline</span></span>

<span data-ttu-id="cdb01-497">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-497">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="cdb01-498">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="cdb01-498">Return Value - underline</span></span>

## <a name="method-userdata"></a><span data-ttu-id="cdb01-499">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="cdb01-499">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="cdb01-500">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="cdb01-500">Parameters - userData</span></span>

<span data-ttu-id="cdb01-501">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-501">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="cdb01-502">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="cdb01-502">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="cdb01-503">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="cdb01-503">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="cdb01-504">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="cdb01-504">Parameters - userDataItem</span></span>

<span data-ttu-id="cdb01-505">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-505">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="cdb01-506">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="cdb01-506">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="cdb01-507">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="cdb01-507">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="cdb01-508">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="cdb01-508">Parameters - userDataItems</span></span>

<span data-ttu-id="cdb01-509">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-509">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="cdb01-510">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="cdb01-510">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="cdb01-511">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="cdb01-511">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="cdb01-512">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="cdb01-512">Parameters - verticalSpacing</span></span>

<span data-ttu-id="cdb01-513">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-513">value</span></span>  

<!-- -->

<span data-ttu-id="cdb01-514">モード</span><span class="sxs-lookup"><span data-stu-id="cdb01-514">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="cdb01-515">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="cdb01-515">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="cdb01-516">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-516">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="cdb01-517">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-517">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="cdb01-518">モード</span><span class="sxs-lookup"><span data-stu-id="cdb01-518">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="cdb01-519">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-519">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="cdb01-520">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-520">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="cdb01-521">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-521">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="cdb01-522">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-522">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="cdb01-523">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-523">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="cdb01-524">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="cdb01-524">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="cdb01-525">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="cdb01-525">Parameters - visible</span></span>

<span data-ttu-id="cdb01-526">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-526">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="cdb01-527">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="cdb01-527">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="cdb01-528">メソッド width</span><span class="sxs-lookup"><span data-stu-id="cdb01-528">Method width</span></span>

<span data-ttu-id="cdb01-529">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-529">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="cdb01-530">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="cdb01-530">Parameters - width</span></span>

<span data-ttu-id="cdb01-531">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-531">value</span></span>  

<!-- -->

<span data-ttu-id="cdb01-532">モード</span><span class="sxs-lookup"><span data-stu-id="cdb01-532">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="cdb01-533">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="cdb01-533">Return Value - width</span></span>

<span data-ttu-id="cdb01-534">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="cdb01-534">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="cdb01-535">備考 - width</span><span class="sxs-lookup"><span data-stu-id="cdb01-535">Remarks - width</span></span>

<span data-ttu-id="cdb01-536">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-536">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="cdb01-537">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="cdb01-537">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="cdb01-538">モード。</span><span class="sxs-lookup"><span data-stu-id="cdb01-538">Mode.</span></span>           | <span data-ttu-id="cdb01-539">幅計算。</span><span class="sxs-lookup"><span data-stu-id="cdb01-539">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb01-540">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="cdb01-540">-1 Exact.</span></span>       | <span data-ttu-id="cdb01-541">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-541">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="cdb01-542">0 自動。</span><span class="sxs-lookup"><span data-stu-id="cdb01-542">0 Auto.</span></span>         | <span data-ttu-id="cdb01-543">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-543">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="cdb01-544">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="cdb01-544">1 Column width.</span></span> | <span data-ttu-id="cdb01-545">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-545">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="cdb01-546">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-546">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="cdb01-547">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-547">Method widthMode</span></span>

<span data-ttu-id="cdb01-548">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-548">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="cdb01-549">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-549">Parameters - widthMode</span></span>

<span data-ttu-id="cdb01-550">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-550">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="cdb01-551">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-551">Return Value - widthMode</span></span>

<span data-ttu-id="cdb01-552">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="cdb01-552">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="cdb01-553">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="cdb01-553">Remarks - widthMode</span></span>

<span data-ttu-id="cdb01-554">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="cdb01-554">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="cdb01-555">モード。</span><span class="sxs-lookup"><span data-stu-id="cdb01-555">Mode.</span></span>         | <span data-ttu-id="cdb01-556">幅計算。</span><span class="sxs-lookup"><span data-stu-id="cdb01-556">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb01-557">正確。</span><span class="sxs-lookup"><span data-stu-id="cdb01-557">Exact.</span></span>        | <span data-ttu-id="cdb01-558">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-558">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="cdb01-559">自動。</span><span class="sxs-lookup"><span data-stu-id="cdb01-559">Auto.</span></span>         | <span data-ttu-id="cdb01-560">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cdb01-560">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="cdb01-561">列の幅。</span><span class="sxs-lookup"><span data-stu-id="cdb01-561">Column width.</span></span> | <span data-ttu-id="cdb01-562">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-562">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="cdb01-563">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="cdb01-563">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="cdb01-564">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-564">Method widthValue</span></span>

<span data-ttu-id="cdb01-565">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-565">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="cdb01-566">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-566">Parameters - widthValue</span></span>

<span data-ttu-id="cdb01-567">値</span><span class="sxs-lookup"><span data-stu-id="cdb01-567">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="cdb01-568">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-568">Return Value - widthValue</span></span>

<span data-ttu-id="cdb01-569">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="cdb01-569">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="cdb01-570">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="cdb01-570">Remarks - widthValue</span></span>

<span data-ttu-id="cdb01-571">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cdb01-571">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="cdb01-572">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="cdb01-572">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="cdb01-573">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="cdb01-573">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="cdb01-574">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="cdb01-574">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="cdb01-575">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="cdb01-575">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="cdb01-576">overrideObject</span><span class="sxs-lookup"><span data-stu-id="cdb01-576">overrideObject</span></span>  



