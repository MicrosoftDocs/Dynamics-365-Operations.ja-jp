---
title: FormBuildManagedHostControl クラス
description: このトピックでは、FormBuildManagedHostControl クラスについて説明します。
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
ms.openlocfilehash: f3caf1df9a36dd7ba32b080d82c54b342345093b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502961"
---
# <a name="class-formbuildmanagedhostcontrol"></a><span data-ttu-id="0aa70-103">クラス FormBuildManagedHostControl</span><span class="sxs-lookup"><span data-stu-id="0aa70-103">Class FormBuildManagedHostControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildManagedHostControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="0aa70-104">備考</span><span class="sxs-lookup"><span data-stu-id="0aa70-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="0aa70-105">例</span><span class="sxs-lookup"><span data-stu-id="0aa70-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="0aa70-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="0aa70-106">Methods</span></span>

| <span data-ttu-id="0aa70-107">方法</span><span class="sxs-lookup"><span data-stu-id="0aa70-107">Method</span></span>                                                                                                      | <span data-ttu-id="0aa70-108">説明</span><span class="sxs-lookup"><span data-stu-id="0aa70-108">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa70-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="0aa70-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-110">Determines whether to align the control.</span></span>                                                                                                      |
| <span data-ttu-id="0aa70-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="0aa70-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-112">Determines whether the user can change the contents of the control.</span></span>                                                                           |
| <span data-ttu-id="0aa70-113">public str assemblyName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-113">public str assemblyName(\[str value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="0aa70-114">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-114">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="0aa70-115">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-115">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="0aa70-116">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-116">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="0aa70-117">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-117">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="0aa70-118">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="0aa70-118">public int containerId()</span></span>                                                                                    | <span data-ttu-id="0aa70-119">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-119">Retrieves the ID of the parent container for the control.</span></span>                                                                                     |
| <span data-ttu-id="0aa70-120">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-120">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="0aa70-121">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-121">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="0aa70-122">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-122">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="0aa70-123">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-123">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="0aa70-124">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-124">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                             |
| <span data-ttu-id="0aa70-125">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-125">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="0aa70-126">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-126">Determines whether to enable or disable the object.</span></span>                                                                                           |
| <span data-ttu-id="0aa70-127">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-127">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="0aa70-128">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-128">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="0aa70-129">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-129">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="0aa70-130">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-130">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="0aa70-131">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-131">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="0aa70-132">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-132">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="0aa70-133">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-133">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="0aa70-134">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-134">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="0aa70-135">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-135">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="0aa70-136">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-136">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="0aa70-137">public int id()</span><span class="sxs-lookup"><span data-stu-id="0aa70-137">public int id()</span></span>                                                                                             | <span data-ttu-id="0aa70-138">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-138">Retrieves the ID of the control.</span></span>                                                                                                              |
| <span data-ttu-id="0aa70-139">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="0aa70-139">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="0aa70-140">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-140">Retrieves a value that indicates whether the control is a container control.</span></span>                                                                  |
| <span data-ttu-id="0aa70-141">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-141">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="0aa70-142">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-142">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="0aa70-143">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-143">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="0aa70-144">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-144">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="0aa70-145">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-145">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="0aa70-146">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-146">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="0aa70-147">public boolean rTLCapable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-147">public boolean rTLCapable(\[boolean value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="0aa70-148">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-148">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="0aa70-149">public int sizing(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-149">public int sizing(\[int value\])</span></span>                                                                            |                                                                                                                                               |
| <span data-ttu-id="0aa70-150">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-150">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="0aa70-151">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-151">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="0aa70-152">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-152">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="0aa70-153">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-153">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="0aa70-154">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-154">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="0aa70-155">public str typeName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-155">public str typeName(\[str value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="0aa70-156">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-156">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="0aa70-157">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-157">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="0aa70-158">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-158">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="0aa70-159">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-159">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                               |
| <span data-ttu-id="0aa70-160">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-160">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="0aa70-161">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-161">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="0aa70-162">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-162">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="0aa70-163">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-163">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="0aa70-164">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-164">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="0aa70-165">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-165">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="0aa70-166">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-166">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="0aa70-167">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-167">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="0aa70-168">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-168">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="0aa70-169">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="0aa70-169">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                               |

## <a name="method-aligncontrol"></a><span data-ttu-id="0aa70-170">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="0aa70-170">Method alignControl</span></span>

<span data-ttu-id="0aa70-171">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-171">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="0aa70-172">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="0aa70-172">Parameters - alignControl</span></span>

<span data-ttu-id="0aa70-173">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-173">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="0aa70-174">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="0aa70-174">Return Value - alignControl</span></span>

<span data-ttu-id="0aa70-175">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="0aa70-175">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="0aa70-176">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="0aa70-176">Remarks - alignControl</span></span>

<span data-ttu-id="0aa70-177">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-177">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="0aa70-178">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="0aa70-178">Method allowEdit</span></span>

<span data-ttu-id="0aa70-179">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-179">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="0aa70-180">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0aa70-180">Parameters - allowEdit</span></span>

<span data-ttu-id="0aa70-181">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-181">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="0aa70-182">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0aa70-182">Return Value - allowEdit</span></span>

<span data-ttu-id="0aa70-183">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0aa70-183">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="0aa70-184">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0aa70-184">Remarks - allowEdit</span></span>

<span data-ttu-id="0aa70-185">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="0aa70-185">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-assemblyname"></a><span data-ttu-id="0aa70-186">メソッド assemblyName</span><span class="sxs-lookup"><span data-stu-id="0aa70-186">Method assemblyName</span></span>

```xpp
public str assemblyName([str value])
```

### <a name="parameters---assemblyname"></a><span data-ttu-id="0aa70-187">パラメーター - assemblyName</span><span class="sxs-lookup"><span data-stu-id="0aa70-187">Parameters - assemblyName</span></span>

<span data-ttu-id="0aa70-188">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-188">value</span></span>  

### <a name="return-value---assemblyname"></a><span data-ttu-id="0aa70-189">戻り値 - assemblyName</span><span class="sxs-lookup"><span data-stu-id="0aa70-189">Return Value - assemblyName</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="0aa70-190">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0aa70-190">Method autoDeclaration</span></span>

<span data-ttu-id="0aa70-191">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-191">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="0aa70-192">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0aa70-192">Parameters - autoDeclaration</span></span>

<span data-ttu-id="0aa70-193">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-193">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="0aa70-194">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0aa70-194">Return Value - autoDeclaration</span></span>

<span data-ttu-id="0aa70-195">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0aa70-195">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="0aa70-196">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0aa70-196">Remarks - autoDeclaration</span></span>

<span data-ttu-id="0aa70-197">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="0aa70-197">Controls cannot have identical names.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="0aa70-198">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="0aa70-198">Method configurationKey</span></span>

<span data-ttu-id="0aa70-199">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-199">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="0aa70-200">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0aa70-200">Parameters - configurationKey</span></span>

<span data-ttu-id="0aa70-201">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-201">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="0aa70-202">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0aa70-202">Return Value - configurationKey</span></span>

<span data-ttu-id="0aa70-203">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="0aa70-203">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="0aa70-204">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0aa70-204">Remarks - configurationKey</span></span>

<span data-ttu-id="0aa70-205">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-205">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="0aa70-206">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="0aa70-206">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="0aa70-207">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="0aa70-207">Method containerId</span></span>

<span data-ttu-id="0aa70-208">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-208">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="0aa70-209">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="0aa70-209">Return Value - containerId</span></span>

<span data-ttu-id="0aa70-210">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="0aa70-210">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="0aa70-211">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0aa70-211">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="0aa70-212">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0aa70-212">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="0aa70-213">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-213">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="0aa70-214">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0aa70-214">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="0aa70-215">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0aa70-215">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="0aa70-216">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0aa70-216">Parameters - dataRelationPath</span></span>

<span data-ttu-id="0aa70-217">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-217">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="0aa70-218">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0aa70-218">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="0aa70-219">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="0aa70-219">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="0aa70-220">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="0aa70-220">Parameters - displayTarget</span></span>

<span data-ttu-id="0aa70-221">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-221">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="0aa70-222">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="0aa70-222">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="0aa70-223">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="0aa70-223">Method dragDrop</span></span>

<span data-ttu-id="0aa70-224">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-224">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="0aa70-225">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0aa70-225">Parameters - dragDrop</span></span>

<span data-ttu-id="0aa70-226">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-226">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="0aa70-227">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0aa70-227">Return Value - dragDrop</span></span>

<span data-ttu-id="0aa70-228">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="0aa70-228">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="0aa70-229">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="0aa70-229">Method enabled</span></span>

<span data-ttu-id="0aa70-230">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-230">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="0aa70-231">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="0aa70-231">Parameters - enabled</span></span>

<span data-ttu-id="0aa70-232">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-232">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="0aa70-233">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="0aa70-233">Return Value - enabled</span></span>

<span data-ttu-id="0aa70-234">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0aa70-234">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="0aa70-235">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="0aa70-235">Remarks - enabled</span></span>

<span data-ttu-id="0aa70-236">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-236">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="0aa70-237">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-237">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="0aa70-238">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-238">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="0aa70-239">メソッド height</span><span class="sxs-lookup"><span data-stu-id="0aa70-239">Method height</span></span>

<span data-ttu-id="0aa70-240">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-240">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="0aa70-241">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="0aa70-241">Parameters - height</span></span>

<span data-ttu-id="0aa70-242">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-242">value</span></span>  

<!-- -->

<span data-ttu-id="0aa70-243">モード</span><span class="sxs-lookup"><span data-stu-id="0aa70-243">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="0aa70-244">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="0aa70-244">Return Value - height</span></span>

<span data-ttu-id="0aa70-245">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="0aa70-245">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="0aa70-246">備考 - height</span><span class="sxs-lookup"><span data-stu-id="0aa70-246">Remarks - height</span></span>

<span data-ttu-id="0aa70-247">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-247">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="0aa70-248">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="0aa70-248">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="0aa70-249">モード。</span><span class="sxs-lookup"><span data-stu-id="0aa70-249">Mode.</span></span>            | <span data-ttu-id="0aa70-250">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="0aa70-250">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa70-251">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="0aa70-251">-1 Exact.</span></span>        | <span data-ttu-id="0aa70-252">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-252">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0aa70-253">0 自動。</span><span class="sxs-lookup"><span data-stu-id="0aa70-253">0 Auto.</span></span>          | <span data-ttu-id="0aa70-254">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-254">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0aa70-255">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="0aa70-255">1 Column height.</span></span> | <span data-ttu-id="0aa70-256">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="0aa70-256">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="0aa70-257">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-257">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="0aa70-258">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-258">Method heightMode</span></span>

<span data-ttu-id="0aa70-259">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-259">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="0aa70-260">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-260">Parameters - heightMode</span></span>

<span data-ttu-id="0aa70-261">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-261">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="0aa70-262">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-262">Return Value - heightMode</span></span>

<span data-ttu-id="0aa70-263">計算モード。</span><span class="sxs-lookup"><span data-stu-id="0aa70-263">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="0aa70-264">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-264">Remarks - heightMode</span></span>

<span data-ttu-id="0aa70-265">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="0aa70-265">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="0aa70-266">モード。</span><span class="sxs-lookup"><span data-stu-id="0aa70-266">Mode.</span></span>          | <span data-ttu-id="0aa70-267">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="0aa70-267">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa70-268">正確。</span><span class="sxs-lookup"><span data-stu-id="0aa70-268">Exact.</span></span>         | <span data-ttu-id="0aa70-269">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-269">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0aa70-270">自動。</span><span class="sxs-lookup"><span data-stu-id="0aa70-270">Auto.</span></span>          | <span data-ttu-id="0aa70-271">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-271">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0aa70-272">列の高さ</span><span class="sxs-lookup"><span data-stu-id="0aa70-272">Column height.</span></span> | <span data-ttu-id="0aa70-273">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="0aa70-273">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="0aa70-274">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0aa70-274">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="0aa70-275">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-275">Method heightValue</span></span>

<span data-ttu-id="0aa70-276">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-276">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="0aa70-277">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-277">Parameters - heightValue</span></span>

<span data-ttu-id="0aa70-278">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-278">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="0aa70-279">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-279">Return Value - heightValue</span></span>

<span data-ttu-id="0aa70-280">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="0aa70-280">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="0aa70-281">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-281">Remarks - heightValue</span></span>

<span data-ttu-id="0aa70-282">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="0aa70-282">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="0aa70-283">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="0aa70-283">Method helpText</span></span>

<span data-ttu-id="0aa70-284">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-284">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="0aa70-285">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="0aa70-285">Parameters - helpText</span></span>

<span data-ttu-id="0aa70-286">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-286">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="0aa70-287">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="0aa70-287">Return Value - helpText</span></span>

<span data-ttu-id="0aa70-288">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="0aa70-288">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="0aa70-289">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="0aa70-289">Remarks - helpText</span></span>

<span data-ttu-id="0aa70-290">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-290">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="0aa70-291">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="0aa70-291">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="0aa70-292">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0aa70-292">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="0aa70-293">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0aa70-293">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="0aa70-294">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-294">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="0aa70-295">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0aa70-295">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="0aa70-296">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0aa70-296">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="0aa70-297">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0aa70-297">Parameters - hierarchyParent</span></span>

<span data-ttu-id="0aa70-298">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-298">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="0aa70-299">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0aa70-299">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="0aa70-300">メソッド id</span><span class="sxs-lookup"><span data-stu-id="0aa70-300">Method id</span></span>

<span data-ttu-id="0aa70-301">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-301">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="0aa70-302">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="0aa70-302">Return Value - id</span></span>

<span data-ttu-id="0aa70-303">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="0aa70-303">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="0aa70-304">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="0aa70-304">Method isContainer</span></span>

<span data-ttu-id="0aa70-305">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-305">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="0aa70-306">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="0aa70-306">Return Value - isContainer</span></span>

<span data-ttu-id="0aa70-307">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0aa70-307">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="0aa70-308">メソッド left</span><span class="sxs-lookup"><span data-stu-id="0aa70-308">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="0aa70-309">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="0aa70-309">Parameters - left</span></span>

<span data-ttu-id="0aa70-310">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-310">value</span></span>  

<!-- -->

<span data-ttu-id="0aa70-311">モード</span><span class="sxs-lookup"><span data-stu-id="0aa70-311">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="0aa70-312">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="0aa70-312">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="0aa70-313">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-313">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="0aa70-314">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-314">Parameters - leftMode</span></span>

<span data-ttu-id="0aa70-315">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-315">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="0aa70-316">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-316">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="0aa70-317">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-317">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="0aa70-318">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-318">Parameters - leftValue</span></span>

<span data-ttu-id="0aa70-319">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-319">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="0aa70-320">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-320">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="0aa70-321">メソッド名</span><span class="sxs-lookup"><span data-stu-id="0aa70-321">Method name</span></span>

<span data-ttu-id="0aa70-322">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-322">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="0aa70-323">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="0aa70-323">Parameters - name</span></span>

<span data-ttu-id="0aa70-324">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-324">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="0aa70-325">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="0aa70-325">Return Value - name</span></span>

<span data-ttu-id="0aa70-326">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="0aa70-326">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="0aa70-327">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="0aa70-327">Remarks - name</span></span>

<span data-ttu-id="0aa70-328">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aa70-328">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="0aa70-329">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-329">Begins with a letter.</span></span>
-   <span data-ttu-id="0aa70-330">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="0aa70-330">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="0aa70-331">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-331">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="0aa70-332">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="0aa70-332">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="0aa70-333">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="0aa70-333">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="0aa70-334">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="0aa70-334">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="0aa70-335">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="0aa70-335">Parameters - neededPermission</span></span>

<span data-ttu-id="0aa70-336">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-336">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="0aa70-337">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="0aa70-337">Return Value - neededPermission</span></span>

## <a name="method-rtlcapable"></a><span data-ttu-id="0aa70-338">メソッド rTLCapable</span><span class="sxs-lookup"><span data-stu-id="0aa70-338">Method rTLCapable</span></span>

```xpp
public boolean rTLCapable([boolean value])
```

### <a name="parameters---rtlcapable"></a><span data-ttu-id="0aa70-339">パラメーター - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="0aa70-339">Parameters - rTLCapable</span></span>

<span data-ttu-id="0aa70-340">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-340">value</span></span>  

### <a name="return-value---rtlcapable"></a><span data-ttu-id="0aa70-341">戻り値 - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="0aa70-341">Return Value - rTLCapable</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="0aa70-342">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="0aa70-342">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="0aa70-343">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="0aa70-343">Parameters - securityKey</span></span>

<span data-ttu-id="0aa70-344">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-344">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="0aa70-345">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="0aa70-345">Return Value - securityKey</span></span>

## <a name="method-sizing"></a><span data-ttu-id="0aa70-346">メソッド sizing</span><span class="sxs-lookup"><span data-stu-id="0aa70-346">Method sizing</span></span>

```xpp
public int sizing([int value])
```

### <a name="parameters---sizing"></a><span data-ttu-id="0aa70-347">パラメーター - sizing</span><span class="sxs-lookup"><span data-stu-id="0aa70-347">Parameters - sizing</span></span>

<span data-ttu-id="0aa70-348">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-348">value</span></span>  

### <a name="return-value---sizing"></a><span data-ttu-id="0aa70-349">戻り値 - sizing</span><span class="sxs-lookup"><span data-stu-id="0aa70-349">Return Value - sizing</span></span>

## <a name="method-skip"></a><span data-ttu-id="0aa70-350">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="0aa70-350">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="0aa70-351">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="0aa70-351">Parameters - skip</span></span>

<span data-ttu-id="0aa70-352">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-352">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="0aa70-353">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="0aa70-353">Return Value - skip</span></span>

## <a name="method-top"></a><span data-ttu-id="0aa70-354">メソッド top</span><span class="sxs-lookup"><span data-stu-id="0aa70-354">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="0aa70-355">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="0aa70-355">Parameters - top</span></span>

<span data-ttu-id="0aa70-356">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-356">value</span></span>  

<!-- -->

<span data-ttu-id="0aa70-357">モード</span><span class="sxs-lookup"><span data-stu-id="0aa70-357">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="0aa70-358">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="0aa70-358">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="0aa70-359">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-359">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="0aa70-360">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-360">Parameters - topMode</span></span>

<span data-ttu-id="0aa70-361">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-361">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="0aa70-362">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-362">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="0aa70-363">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-363">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="0aa70-364">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-364">Parameters - topValue</span></span>

<span data-ttu-id="0aa70-365">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-365">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="0aa70-366">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-366">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="0aa70-367">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="0aa70-367">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="0aa70-368">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="0aa70-368">Parameters - type</span></span>

<span data-ttu-id="0aa70-369">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-369">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="0aa70-370">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="0aa70-370">Return Value - type</span></span>

## <a name="method-typename"></a><span data-ttu-id="0aa70-371">メソッド typeName</span><span class="sxs-lookup"><span data-stu-id="0aa70-371">Method typeName</span></span>

```xpp
public str typeName([str value])
```

### <a name="parameters---typename"></a><span data-ttu-id="0aa70-372">パラメーター - typeName</span><span class="sxs-lookup"><span data-stu-id="0aa70-372">Parameters - typeName</span></span>

<span data-ttu-id="0aa70-373">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-373">value</span></span>  

### <a name="return-value---typename"></a><span data-ttu-id="0aa70-374">戻り値 - typeName</span><span class="sxs-lookup"><span data-stu-id="0aa70-374">Return Value - typeName</span></span>

## <a name="method-userdata"></a><span data-ttu-id="0aa70-375">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="0aa70-375">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="0aa70-376">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="0aa70-376">Parameters - userData</span></span>

<span data-ttu-id="0aa70-377">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-377">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="0aa70-378">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="0aa70-378">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="0aa70-379">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="0aa70-379">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="0aa70-380">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="0aa70-380">Parameters - userDataItem</span></span>

<span data-ttu-id="0aa70-381">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-381">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="0aa70-382">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="0aa70-382">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="0aa70-383">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="0aa70-383">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="0aa70-384">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="0aa70-384">Parameters - userDataItems</span></span>

<span data-ttu-id="0aa70-385">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-385">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="0aa70-386">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="0aa70-386">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="0aa70-387">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0aa70-387">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="0aa70-388">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0aa70-388">Parameters - verticalSpacing</span></span>

<span data-ttu-id="0aa70-389">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-389">value</span></span>  

<!-- -->

<span data-ttu-id="0aa70-390">モード</span><span class="sxs-lookup"><span data-stu-id="0aa70-390">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="0aa70-391">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0aa70-391">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="0aa70-392">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-392">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="0aa70-393">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-393">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="0aa70-394">モード</span><span class="sxs-lookup"><span data-stu-id="0aa70-394">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="0aa70-395">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-395">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="0aa70-396">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-396">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="0aa70-397">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-397">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="0aa70-398">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-398">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="0aa70-399">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-399">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="0aa70-400">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="0aa70-400">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="0aa70-401">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="0aa70-401">Parameters - visible</span></span>

<span data-ttu-id="0aa70-402">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-402">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="0aa70-403">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="0aa70-403">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="0aa70-404">メソッド width</span><span class="sxs-lookup"><span data-stu-id="0aa70-404">Method width</span></span>

<span data-ttu-id="0aa70-405">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-405">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="0aa70-406">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="0aa70-406">Parameters - width</span></span>

<span data-ttu-id="0aa70-407">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-407">value</span></span>  

<!-- -->

<span data-ttu-id="0aa70-408">モード</span><span class="sxs-lookup"><span data-stu-id="0aa70-408">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="0aa70-409">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="0aa70-409">Return Value - width</span></span>

<span data-ttu-id="0aa70-410">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="0aa70-410">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="0aa70-411">備考 - width</span><span class="sxs-lookup"><span data-stu-id="0aa70-411">Remarks - width</span></span>

<span data-ttu-id="0aa70-412">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-412">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="0aa70-413">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="0aa70-413">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="0aa70-414">モード。</span><span class="sxs-lookup"><span data-stu-id="0aa70-414">Mode.</span></span>           | <span data-ttu-id="0aa70-415">幅計算。</span><span class="sxs-lookup"><span data-stu-id="0aa70-415">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa70-416">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="0aa70-416">-1 Exact.</span></span>       | <span data-ttu-id="0aa70-417">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-417">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0aa70-418">0 自動。</span><span class="sxs-lookup"><span data-stu-id="0aa70-418">0 Auto.</span></span>         | <span data-ttu-id="0aa70-419">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-419">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0aa70-420">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="0aa70-420">1 Column width.</span></span> | <span data-ttu-id="0aa70-421">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="0aa70-421">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="0aa70-422">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-422">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="0aa70-423">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-423">Method widthMode</span></span>

<span data-ttu-id="0aa70-424">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-424">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="0aa70-425">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-425">Parameters - widthMode</span></span>

<span data-ttu-id="0aa70-426">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-426">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="0aa70-427">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-427">Return Value - widthMode</span></span>

<span data-ttu-id="0aa70-428">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0aa70-428">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="0aa70-429">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="0aa70-429">Remarks - widthMode</span></span>

<span data-ttu-id="0aa70-430">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="0aa70-430">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="0aa70-431">モード。</span><span class="sxs-lookup"><span data-stu-id="0aa70-431">Mode.</span></span>         | <span data-ttu-id="0aa70-432">幅計算。</span><span class="sxs-lookup"><span data-stu-id="0aa70-432">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa70-433">正確。</span><span class="sxs-lookup"><span data-stu-id="0aa70-433">Exact.</span></span>        | <span data-ttu-id="0aa70-434">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-434">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0aa70-435">自動。</span><span class="sxs-lookup"><span data-stu-id="0aa70-435">Auto.</span></span>         | <span data-ttu-id="0aa70-436">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0aa70-436">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0aa70-437">列の幅。</span><span class="sxs-lookup"><span data-stu-id="0aa70-437">Column width.</span></span> | <span data-ttu-id="0aa70-438">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="0aa70-438">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="0aa70-439">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0aa70-439">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="0aa70-440">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-440">Method widthValue</span></span>

<span data-ttu-id="0aa70-441">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-441">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="0aa70-442">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-442">Parameters - widthValue</span></span>

<span data-ttu-id="0aa70-443">値</span><span class="sxs-lookup"><span data-stu-id="0aa70-443">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="0aa70-444">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-444">Return Value - widthValue</span></span>

<span data-ttu-id="0aa70-445">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="0aa70-445">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="0aa70-446">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="0aa70-446">Remarks - widthValue</span></span>

<span data-ttu-id="0aa70-447">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="0aa70-447">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="0aa70-448">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="0aa70-448">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="0aa70-449">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="0aa70-449">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="0aa70-450">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="0aa70-450">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="0aa70-451">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="0aa70-451">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="0aa70-452">overrideObject</span><span class="sxs-lookup"><span data-stu-id="0aa70-452">overrideObject</span></span>  

