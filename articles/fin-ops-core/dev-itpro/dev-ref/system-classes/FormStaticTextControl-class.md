---
title: FormStaticTextControl クラス
description: このトピックでは、FormStaticTextControl クラスについて説明します。
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
ms.openlocfilehash: 1ce62f9efdc112d9a1c708f0c1c6bea374323cbc
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502614"
---
# <a name="class-formstatictextcontrol"></a><span data-ttu-id="c93df-103">クラス FormStaticTextControl</span><span class="sxs-lookup"><span data-stu-id="c93df-103">Class FormStaticTextControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormStaticTextControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="c93df-104">備考</span><span class="sxs-lookup"><span data-stu-id="c93df-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c93df-105">例</span><span class="sxs-lookup"><span data-stu-id="c93df-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c93df-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c93df-106">Methods</span></span>

| <span data-ttu-id="c93df-107">方法</span><span class="sxs-lookup"><span data-stu-id="c93df-107">Method</span></span>                                                                                                      | <span data-ttu-id="c93df-108">説明</span><span class="sxs-lookup"><span data-stu-id="c93df-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93df-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="c93df-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="c93df-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="c93df-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="c93df-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="c93df-114">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="c93df-114">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="c93df-115">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-115">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="c93df-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="c93df-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="c93df-118">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-118">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="c93df-119">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-119">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="c93df-120">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-120">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="c93df-121">コントロールの背景色を透明にできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-121">Indicates whether the control background can be transparent.</span></span>                                                                                                            |
| <span data-ttu-id="c93df-122">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c93df-122">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="c93df-123">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-123">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="c93df-124">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-124">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="c93df-125">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-125">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                                             |
| <span data-ttu-id="c93df-126">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-126">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="c93df-127">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="c93df-127">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="c93df-128">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-128">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="c93df-129">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-129">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="c93df-130">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-130">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="c93df-131">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-131">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="c93df-132">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-132">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="c93df-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="c93df-134">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-134">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="c93df-135">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="c93df-135">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="c93df-136">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-136">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="c93df-137">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-137">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="c93df-138">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-138">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="c93df-139">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-139">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="c93df-140">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-140">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="c93df-141">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-141">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="c93df-142">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-142">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="c93df-143">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-143">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="c93df-144">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-144">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="c93df-145">コントロールまたはフォームで使用するデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-145">Gets or sets a data source for use by the control or the form.</span></span>                                                                                                          |
| <span data-ttu-id="c93df-146">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-146">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="c93df-147">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-147">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="c93df-148">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-148">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="c93df-149">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-149">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="c93df-150">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-150">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="c93df-151">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-151">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="c93df-152">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-152">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="c93df-153">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-153">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="c93df-154">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-154">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="c93df-155">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-155">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                        |
| <span data-ttu-id="c93df-156">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c93df-156">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="c93df-157">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-157">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="c93df-158">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c93df-158">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="c93df-159">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-159">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="c93df-160">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="c93df-160">public str dragText()</span></span>                                                                                       | <span data-ttu-id="c93df-161">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-161">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="c93df-162">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-162">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="c93df-163">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-163">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="c93df-164">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-164">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="c93df-165">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-165">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="c93df-166">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-166">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="c93df-167">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-167">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="c93df-168">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-168">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="c93df-169">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-169">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="c93df-170">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="c93df-170">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="c93df-171">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-171">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="c93df-172">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="c93df-172">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="c93df-173">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-173">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="c93df-174">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-174">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="c93df-175">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-175">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="c93df-176">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-176">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="c93df-177">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-177">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="c93df-178">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-178">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="c93df-179">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-179">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="c93df-180">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="c93df-180">public str helpField()</span></span>                                                                                      | <span data-ttu-id="c93df-181">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-181">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="c93df-182">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-182">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="c93df-183">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-183">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="c93df-184">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-184">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="c93df-185">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-185">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="c93df-186">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="c93df-186">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="c93df-187">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-187">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="c93df-188">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="c93df-188">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="c93df-189">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="c93df-189">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="c93df-190">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-190">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="c93df-191">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="c93df-191">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="c93df-192">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-192">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="c93df-193">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="c93df-193">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="c93df-194">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-194">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="c93df-195">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-195">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="c93df-196">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-196">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="c93df-197">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-197">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="c93df-198">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-198">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="c93df-199">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-199">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="c93df-200">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-200">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="c93df-201">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-201">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="c93df-202">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-202">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="c93df-203">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="c93df-203">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="c93df-204">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c93df-204">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="c93df-205">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-205">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="c93df-206">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c93df-206">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="c93df-207">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-207">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="c93df-208">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c93df-208">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="c93df-209">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-209">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="c93df-210">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c93df-210">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="c93df-211">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-211">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="c93df-212">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-212">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="c93df-213">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-213">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="c93df-214">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-214">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="c93df-215">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="c93df-215">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="c93df-216">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="c93df-216">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="c93df-217">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-217">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="c93df-218">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-218">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="c93df-219">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-219">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="c93df-220">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-220">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="c93df-221">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="c93df-221">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="c93df-222">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-222">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="c93df-223">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-223">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="c93df-224">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-224">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="c93df-225">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="c93df-225">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="c93df-226">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-226">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="c93df-227">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-227">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="c93df-228">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="c93df-228">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="c93df-229">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-229">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="c93df-230">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-230">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="c93df-231">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-231">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="c93df-232">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-232">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="c93df-233">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-233">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="c93df-234">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-234">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="c93df-235">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-235">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="c93df-236">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-236">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="c93df-237">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-237">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="c93df-238">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="c93df-238">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="c93df-239">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-239">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="c93df-240">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-240">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="c93df-241">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-241">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="c93df-242">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-242">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="c93df-243">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-243">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="c93df-244">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-244">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="c93df-245">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-245">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="c93df-246">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-246">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="c93df-247">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-247">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="c93df-248">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-248">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="c93df-249">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-249">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="c93df-250">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-250">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="c93df-251">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-251">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="c93df-252">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-252">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="c93df-253">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-253">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="c93df-254">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-254">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="c93df-255">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-255">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="c93df-256">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-256">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="c93df-257">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-257">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="c93df-258">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-258">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="c93df-259">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-259">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="c93df-260">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-260">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="c93df-261">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-261">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="c93df-262">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-262">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="c93df-263">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-263">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="c93df-264">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-264">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="c93df-265">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-265">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="c93df-266">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-266">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="c93df-267">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-267">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="c93df-268">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-268">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="c93df-269">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-269">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="c93df-270">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-270">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="c93df-271">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c93df-271">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="c93df-272">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-272">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="c93df-273">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-273">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="c93df-274">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-274">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="c93df-275">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c93df-275">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="c93df-276">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-276">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="c93df-277">public void paste()</span><span class="sxs-lookup"><span data-stu-id="c93df-277">public void paste()</span></span>                                                                                         | <span data-ttu-id="c93df-278">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="c93df-278">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="c93df-279">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="c93df-279">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="c93df-280">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="c93df-280">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="c93df-281">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-281">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="c93df-282">public void context()</span><span class="sxs-lookup"><span data-stu-id="c93df-282">public void context()</span></span>                                                                                       | <span data-ttu-id="c93df-283">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-283">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="c93df-284">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="c93df-284">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="c93df-285">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="c93df-285">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="c93df-286">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="c93df-286">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="c93df-287">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-287">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="c93df-288">public void copy()</span><span class="sxs-lookup"><span data-stu-id="c93df-288">public void copy()</span></span>                                                                                          | <span data-ttu-id="c93df-289">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="c93df-289">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="c93df-290">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="c93df-290">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="c93df-291">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c93df-291">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="c93df-292">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-292">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="c93df-293">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="c93df-293">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="c93df-294">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="c93df-294">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="c93df-295">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="c93df-295">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="c93df-296">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="c93df-296">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="c93df-297">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-297">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="c93df-298">public void cut()</span><span class="sxs-lookup"><span data-stu-id="c93df-298">public void cut()</span></span>                                                                                           | <span data-ttu-id="c93df-299">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="c93df-299">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="c93df-300">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="c93df-300">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="c93df-301">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-301">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="c93df-302">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c93df-302">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="c93df-303">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-303">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="c93df-304">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="c93df-304">public void displayControl()</span></span>                                                                                | <span data-ttu-id="c93df-305">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-305">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="c93df-306">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="c93df-306">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="c93df-307">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="c93df-307">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="c93df-308">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="c93df-308">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="c93df-309">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-309">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="c93df-310">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c93df-310">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="c93df-311">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-311">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="c93df-312">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="c93df-312">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="c93df-313">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-313">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="c93df-314">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="c93df-314">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="c93df-315">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-315">Indicates that the control has received focus.</span></span>                                                                                                                          |

## <a name="method-aligncontrol"></a><span data-ttu-id="c93df-316">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="c93df-316">Method alignControl</span></span>

<span data-ttu-id="c93df-317">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-317">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="c93df-318">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="c93df-318">Parameters - alignControl</span></span>

<span data-ttu-id="c93df-319">値</span><span class="sxs-lookup"><span data-stu-id="c93df-319">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="c93df-320">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="c93df-320">Return Value - alignControl</span></span>

<span data-ttu-id="c93df-321">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="c93df-321">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="c93df-322">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="c93df-322">Remarks - alignControl</span></span>

<span data-ttu-id="c93df-323">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-323">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="c93df-324">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="c93df-324">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="c93df-325">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="c93df-325">Parameters - alignment</span></span>

<span data-ttu-id="c93df-326">値</span><span class="sxs-lookup"><span data-stu-id="c93df-326">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="c93df-327">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="c93df-327">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="c93df-328">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="c93df-328">Method allowEdit</span></span>

<span data-ttu-id="c93df-329">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-329">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="c93df-330">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="c93df-330">Parameters - allowEdit</span></span>

<span data-ttu-id="c93df-331">値</span><span class="sxs-lookup"><span data-stu-id="c93df-331">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="c93df-332">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="c93df-332">Return Value - allowEdit</span></span>

<span data-ttu-id="c93df-333">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-333">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="c93df-334">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="c93df-334">Remarks - allowEdit</span></span>

<span data-ttu-id="c93df-335">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="c93df-335">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="c93df-336">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="c93df-336">Method allowSysSetup</span></span>

<span data-ttu-id="c93df-337">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-337">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="c93df-338">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="c93df-338">Return Value - allowSysSetup</span></span>

<span data-ttu-id="c93df-339">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-339">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="c93df-340">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c93df-340">Method autoDeclaration</span></span>

<span data-ttu-id="c93df-341">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-341">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="c93df-342">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c93df-342">Parameters - autoDeclaration</span></span>

<span data-ttu-id="c93df-343">値</span><span class="sxs-lookup"><span data-stu-id="c93df-343">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="c93df-344">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c93df-344">Return Value - autoDeclaration</span></span>

<span data-ttu-id="c93df-345">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-345">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="c93df-346">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c93df-346">Remarks - autoDeclaration</span></span>

<span data-ttu-id="c93df-347">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="c93df-347">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="c93df-348">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="c93df-348">Method backgroundColor</span></span>

<span data-ttu-id="c93df-349">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-349">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="c93df-350">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="c93df-350">Parameters - backgroundColor</span></span>

<span data-ttu-id="c93df-351">値</span><span class="sxs-lookup"><span data-stu-id="c93df-351">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="c93df-352">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="c93df-352">Return Value - backgroundColor</span></span>

<span data-ttu-id="c93df-353">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="c93df-353">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="c93df-354">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="c93df-354">Remarks - backgroundColor</span></span>

<span data-ttu-id="c93df-355">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c93df-355">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="c93df-356">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c93df-356">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="c93df-357">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="c93df-357">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="c93df-358">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="c93df-358">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="c93df-359">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c93df-359">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="c93df-360">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="c93df-360">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="c93df-361">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="c93df-361">Method backStyle</span></span>

<span data-ttu-id="c93df-362">コントロールの背景色を透明にできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-362">Indicates whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="c93df-363">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="c93df-363">Parameters - backStyle</span></span>

<span data-ttu-id="c93df-364">値</span><span class="sxs-lookup"><span data-stu-id="c93df-364">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="c93df-365">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="c93df-365">Return Value - backStyle</span></span>

<span data-ttu-id="c93df-366">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="c93df-366">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="c93df-367">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="c93df-367">Method beginDrag</span></span>

<span data-ttu-id="c93df-368">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-368">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="c93df-369">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="c93df-369">Parameters - beginDrag</span></span>

<span data-ttu-id="c93df-370">x</span><span class="sxs-lookup"><span data-stu-id="c93df-370">x</span></span>  
<span data-ttu-id="c93df-371">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-371">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="c93df-372">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="c93df-372">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="c93df-373">y</span><span class="sxs-lookup"><span data-stu-id="c93df-373">y</span></span>  
<span data-ttu-id="c93df-374">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-374">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="c93df-375">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="c93df-375">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="c93df-376">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="c93df-376">Return Value - beginDrag</span></span>

<span data-ttu-id="c93df-377">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c93df-377">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="c93df-378">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="c93df-378">Remarks - beginDrag</span></span>

<span data-ttu-id="c93df-379">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="c93df-379">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="c93df-380">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="c93df-380">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="c93df-381">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="c93df-381">Method bold</span></span>

<span data-ttu-id="c93df-382">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-382">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="c93df-383">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="c93df-383">Parameters - bold</span></span>

<span data-ttu-id="c93df-384">値</span><span class="sxs-lookup"><span data-stu-id="c93df-384">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="c93df-385">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="c93df-385">Return Value - bold</span></span>

<span data-ttu-id="c93df-386">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-386">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="c93df-387">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="c93df-387">Remarks - bold</span></span>

<span data-ttu-id="c93df-388">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c93df-388">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="c93df-389">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="c93df-389">0 Use the default font weight.</span></span>
-   <span data-ttu-id="c93df-390">1 シン。</span><span class="sxs-lookup"><span data-stu-id="c93df-390">1 Thin.</span></span>
-   <span data-ttu-id="c93df-391">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="c93df-391">2 Extra-light.</span></span>
-   <span data-ttu-id="c93df-392">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="c93df-392">3 Light.</span></span>
-   <span data-ttu-id="c93df-393">4 標準。</span><span class="sxs-lookup"><span data-stu-id="c93df-393">4 Normal.</span></span>
-   <span data-ttu-id="c93df-394">5 中。</span><span class="sxs-lookup"><span data-stu-id="c93df-394">5 Medium.</span></span>
-   <span data-ttu-id="c93df-395">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="c93df-395">6 Semibold.</span></span>
-   <span data-ttu-id="c93df-396">7 太字。</span><span class="sxs-lookup"><span data-stu-id="c93df-396">7 Bold.</span></span>
-   <span data-ttu-id="c93df-397">8 極太。</span><span class="sxs-lookup"><span data-stu-id="c93df-397">8 Extra-bold.</span></span>
-   <span data-ttu-id="c93df-398">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="c93df-398">9 Heavy.</span></span>

## <a name="method-cachedatamethod"></a><span data-ttu-id="c93df-399">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="c93df-399">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="c93df-400">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="c93df-400">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="c93df-401">値</span><span class="sxs-lookup"><span data-stu-id="c93df-401">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="c93df-402">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="c93df-402">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="c93df-403">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="c93df-403">Method calcControlSize</span></span>

<span data-ttu-id="c93df-404">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-404">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="c93df-405">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="c93df-405">Parameters - calcControlSize</span></span>

<span data-ttu-id="c93df-406">chars</span><span class="sxs-lookup"><span data-stu-id="c93df-406">chars</span></span>  
<span data-ttu-id="c93df-407">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="c93df-407">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="c93df-408">明細行</span><span class="sxs-lookup"><span data-stu-id="c93df-408">lines</span></span>  
<span data-ttu-id="c93df-409">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="c93df-409">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="c93df-410">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="c93df-410">Return Value - calcControlSize</span></span>

<span data-ttu-id="c93df-411">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="c93df-411">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="c93df-412">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="c93df-412">Method characterSet</span></span>

<span data-ttu-id="c93df-413">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-413">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="c93df-414">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="c93df-414">Parameters - characterSet</span></span>

<span data-ttu-id="c93df-415">値</span><span class="sxs-lookup"><span data-stu-id="c93df-415">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="c93df-416">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="c93df-416">Return Value - characterSet</span></span>

<span data-ttu-id="c93df-417">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-417">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="c93df-418">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="c93df-418">Remarks - characterSet</span></span>

<span data-ttu-id="c93df-419">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-419">The values for the integer that is returned indicate the character set according to the following table.</span></span>

| <span data-ttu-id="c93df-420">先頭値</span><span class="sxs-lookup"><span data-stu-id="c93df-420">Value</span></span> | <span data-ttu-id="c93df-421">説明</span><span class="sxs-lookup"><span data-stu-id="c93df-421">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="c93df-422">0</span><span class="sxs-lookup"><span data-stu-id="c93df-422">0</span></span>     | <span data-ttu-id="c93df-423">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-423">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="c93df-424">1</span><span class="sxs-lookup"><span data-stu-id="c93df-424">1</span></span>     | <span data-ttu-id="c93df-425">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-425">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="c93df-426">2</span><span class="sxs-lookup"><span data-stu-id="c93df-426">2</span></span>     | <span data-ttu-id="c93df-427">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-427">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="c93df-428">77</span><span class="sxs-lookup"><span data-stu-id="c93df-428">77</span></span>    | <span data-ttu-id="c93df-429">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-429">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="c93df-430">128</span><span class="sxs-lookup"><span data-stu-id="c93df-430">128</span></span>   | <span data-ttu-id="c93df-431">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-431">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="c93df-432">129</span><span class="sxs-lookup"><span data-stu-id="c93df-432">129</span></span>   | <span data-ttu-id="c93df-433">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-433">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="c93df-434">134</span><span class="sxs-lookup"><span data-stu-id="c93df-434">134</span></span>   | <span data-ttu-id="c93df-435">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-435">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="c93df-436">136</span><span class="sxs-lookup"><span data-stu-id="c93df-436">136</span></span>   | <span data-ttu-id="c93df-437">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-437">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="c93df-438">161</span><span class="sxs-lookup"><span data-stu-id="c93df-438">161</span></span>   | <span data-ttu-id="c93df-439">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-439">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="c93df-440">162</span><span class="sxs-lookup"><span data-stu-id="c93df-440">162</span></span>   | <span data-ttu-id="c93df-441">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-441">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="c93df-442">163</span><span class="sxs-lookup"><span data-stu-id="c93df-442">163</span></span>   | <span data-ttu-id="c93df-443">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-443">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="c93df-444">186</span><span class="sxs-lookup"><span data-stu-id="c93df-444">186</span></span>   | <span data-ttu-id="c93df-445">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-445">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="c93df-446">204</span><span class="sxs-lookup"><span data-stu-id="c93df-446">204</span></span>   | <span data-ttu-id="c93df-447">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-447">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="c93df-448">238</span><span class="sxs-lookup"><span data-stu-id="c93df-448">238</span></span>   | <span data-ttu-id="c93df-449">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-449">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="c93df-450">255</span><span class="sxs-lookup"><span data-stu-id="c93df-450">255</span></span>   | <span data-ttu-id="c93df-451">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-451">OEM\_CHARSET</span></span>         |

<span data-ttu-id="c93df-452">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="c93df-452">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="c93df-453">金額</span><span class="sxs-lookup"><span data-stu-id="c93df-453">Value</span></span> | <span data-ttu-id="c93df-454">説明</span><span class="sxs-lookup"><span data-stu-id="c93df-454">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="c93df-455">130</span><span class="sxs-lookup"><span data-stu-id="c93df-455">130</span></span>   | <span data-ttu-id="c93df-456">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-456">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="c93df-457">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="c93df-457">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="c93df-458">先頭値</span><span class="sxs-lookup"><span data-stu-id="c93df-458">Value</span></span> | <span data-ttu-id="c93df-459">説明</span><span class="sxs-lookup"><span data-stu-id="c93df-459">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="c93df-460">177</span><span class="sxs-lookup"><span data-stu-id="c93df-460">177</span></span>   | <span data-ttu-id="c93df-461">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-461">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="c93df-462">178</span><span class="sxs-lookup"><span data-stu-id="c93df-462">178</span></span>   | <span data-ttu-id="c93df-463">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-463">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="c93df-464">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="c93df-464">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="c93df-465">先頭値</span><span class="sxs-lookup"><span data-stu-id="c93df-465">Value</span></span> | <span data-ttu-id="c93df-466">説明</span><span class="sxs-lookup"><span data-stu-id="c93df-466">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="c93df-467">222</span><span class="sxs-lookup"><span data-stu-id="c93df-467">222</span></span>   | <span data-ttu-id="c93df-468">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="c93df-468">THAI\_CHARSET</span></span> |

<span data-ttu-id="c93df-469">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-469">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="c93df-470">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-470">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="c93df-471">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c93df-471">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="c93df-472">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="c93df-472">Method colorScheme</span></span>

<span data-ttu-id="c93df-473">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-473">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="c93df-474">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="c93df-474">Parameters - colorScheme</span></span>

<span data-ttu-id="c93df-475">値</span><span class="sxs-lookup"><span data-stu-id="c93df-475">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="c93df-476">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="c93df-476">Return Value - colorScheme</span></span>

<span data-ttu-id="c93df-477">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="c93df-477">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="c93df-478">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="c93df-478">Remarks - colorScheme</span></span>

<span data-ttu-id="c93df-479">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-479">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="c93df-480">先頭値</span><span class="sxs-lookup"><span data-stu-id="c93df-480">Value</span></span> | <span data-ttu-id="c93df-481">スタイル</span><span class="sxs-lookup"><span data-stu-id="c93df-481">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="c93df-482">0</span><span class="sxs-lookup"><span data-stu-id="c93df-482">0</span></span>     | <span data-ttu-id="c93df-483">既定</span><span class="sxs-lookup"><span data-stu-id="c93df-483">Default</span></span>               |
| <span data-ttu-id="c93df-484">1</span><span class="sxs-lookup"><span data-stu-id="c93df-484">1</span></span>     | <span data-ttu-id="c93df-485">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="c93df-485">The Windows palette</span></span>   |
| <span data-ttu-id="c93df-486">2</span><span class="sxs-lookup"><span data-stu-id="c93df-486">2</span></span>     | <span data-ttu-id="c93df-487">真の配色</span><span class="sxs-lookup"><span data-stu-id="c93df-487">The true-color scheme</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="c93df-488">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="c93df-488">Method configurationKey</span></span>

<span data-ttu-id="c93df-489">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-489">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="c93df-490">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="c93df-490">Parameters - configurationKey</span></span>

<span data-ttu-id="c93df-491">値</span><span class="sxs-lookup"><span data-stu-id="c93df-491">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="c93df-492">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="c93df-492">Return Value - configurationKey</span></span>

<span data-ttu-id="c93df-493">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="c93df-493">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="c93df-494">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="c93df-494">Remarks - configurationKey</span></span>

<span data-ttu-id="c93df-495">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-495">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="c93df-496">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="c93df-496">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="c93df-497">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="c93df-497">Method configurationKeyEx</span></span>

<span data-ttu-id="c93df-498">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-498">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="c93df-499">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="c93df-499">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="c93df-500">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="c93df-500">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="c93df-501">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="c93df-501">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="c93df-502">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="c93df-502">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="c93df-503">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="c93df-503">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="c93df-504">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c93df-504">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="c93df-505">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c93df-505">Method countryRegionCodes</span></span>

<span data-ttu-id="c93df-506">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-506">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="c93df-507">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c93df-507">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="c93df-508">値</span><span class="sxs-lookup"><span data-stu-id="c93df-508">value</span></span>  
<span data-ttu-id="c93df-509">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-509">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="c93df-510">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c93df-510">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="c93df-511">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="c93df-511">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="c93df-512">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="c93df-512">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="c93df-513">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="c93df-513">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="c93df-514">値</span><span class="sxs-lookup"><span data-stu-id="c93df-514">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="c93df-515">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="c93df-515">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="c93df-516">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="c93df-516">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="c93df-517">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="c93df-517">Parameters - dataField</span></span>

<span data-ttu-id="c93df-518">値</span><span class="sxs-lookup"><span data-stu-id="c93df-518">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="c93df-519">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="c93df-519">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="c93df-520">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="c93df-520">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="c93df-521">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="c93df-521">Parameters - dataMethod</span></span>

<span data-ttu-id="c93df-522">値</span><span class="sxs-lookup"><span data-stu-id="c93df-522">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="c93df-523">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="c93df-523">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="c93df-524">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="c93df-524">Method dataRelationPath</span></span>

<span data-ttu-id="c93df-525">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-525">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="c93df-526">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="c93df-526">Parameters - dataRelationPath</span></span>

<span data-ttu-id="c93df-527">値</span><span class="sxs-lookup"><span data-stu-id="c93df-527">value</span></span>  
<span data-ttu-id="c93df-528">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-528">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="c93df-529">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="c93df-529">Return Value - dataRelationPath</span></span>

<span data-ttu-id="c93df-530">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="c93df-530">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="c93df-531">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="c93df-531">Remarks - dataRelationPath</span></span>

<span data-ttu-id="c93df-532">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="c93df-532">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="c93df-533">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="c93df-533">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="c93df-534">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="c93df-534">Method dataSource</span></span>

<span data-ttu-id="c93df-535">コントロールまたはフォームで使用するデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-535">Gets or sets a data source for use by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="c93df-536">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="c93df-536">Parameters - dataSource</span></span>

<span data-ttu-id="c93df-537">値</span><span class="sxs-lookup"><span data-stu-id="c93df-537">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="c93df-538">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="c93df-538">Return Value - dataSource</span></span>

<span data-ttu-id="c93df-539">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="c93df-539">The identifier of the data source to use.</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="c93df-540">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="c93df-540">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="c93df-541">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="c93df-541">Parameters - displayHeight</span></span>

<span data-ttu-id="c93df-542">値</span><span class="sxs-lookup"><span data-stu-id="c93df-542">value</span></span>  

<!-- -->

<span data-ttu-id="c93df-543">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-543">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="c93df-544">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="c93df-544">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="c93df-545">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="c93df-545">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="c93df-546">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="c93df-546">Parameters - displayHeightMode</span></span>

<span data-ttu-id="c93df-547">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-547">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="c93df-548">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="c93df-548">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="c93df-549">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="c93df-549">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="c93df-550">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="c93df-550">Parameters - displayHeightValue</span></span>

<span data-ttu-id="c93df-551">値</span><span class="sxs-lookup"><span data-stu-id="c93df-551">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="c93df-552">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="c93df-552">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="c93df-553">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="c93df-553">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="c93df-554">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="c93df-554">Parameters - displayLength</span></span>

<span data-ttu-id="c93df-555">値</span><span class="sxs-lookup"><span data-stu-id="c93df-555">value</span></span>  

<!-- -->

<span data-ttu-id="c93df-556">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-556">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="c93df-557">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="c93df-557">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="c93df-558">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="c93df-558">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="c93df-559">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="c93df-559">Parameters - displayLengthMode</span></span>

<span data-ttu-id="c93df-560">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-560">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="c93df-561">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="c93df-561">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="c93df-562">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="c93df-562">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="c93df-563">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="c93df-563">Parameters - displayLengthValue</span></span>

<span data-ttu-id="c93df-564">値</span><span class="sxs-lookup"><span data-stu-id="c93df-564">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="c93df-565">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="c93df-565">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="c93df-566">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="c93df-566">Method displayTarget</span></span>

<span data-ttu-id="c93df-567">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-567">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="c93df-568">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="c93df-568">Parameters - displayTarget</span></span>

<span data-ttu-id="c93df-569">値</span><span class="sxs-lookup"><span data-stu-id="c93df-569">value</span></span>  
<span data-ttu-id="c93df-570">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-570">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="c93df-571">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="c93df-571">Return Value - displayTarget</span></span>

<span data-ttu-id="c93df-572">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="c93df-572">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="c93df-573">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="c93df-573">Method dragDrop</span></span>

<span data-ttu-id="c93df-574">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-574">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="c93df-575">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="c93df-575">Parameters - dragDrop</span></span>

<span data-ttu-id="c93df-576">値</span><span class="sxs-lookup"><span data-stu-id="c93df-576">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="c93df-577">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="c93df-577">Return Value - dragDrop</span></span>

<span data-ttu-id="c93df-578">ドラッグ アンド ドロップ操作が有効な場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-578">true if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="c93df-579">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="c93df-579">Method dragOver</span></span>

<span data-ttu-id="c93df-580">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-580">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="c93df-581">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="c93df-581">Parameters - dragOver</span></span>

<span data-ttu-id="c93df-582">dragSource</span><span class="sxs-lookup"><span data-stu-id="c93df-582">dragSource</span></span>  
<span data-ttu-id="c93df-583">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-583">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-584">dragMode</span><span class="sxs-lookup"><span data-stu-id="c93df-584">dragMode</span></span>  
<span data-ttu-id="c93df-585">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-585">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-586">x</span><span class="sxs-lookup"><span data-stu-id="c93df-586">x</span></span>  
<span data-ttu-id="c93df-587">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-587">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-588">y</span><span class="sxs-lookup"><span data-stu-id="c93df-588">y</span></span>  
<span data-ttu-id="c93df-589">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-589">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="c93df-590">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="c93df-590">Return Value - dragOver</span></span>

<span data-ttu-id="c93df-591">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="c93df-591">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="c93df-592">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="c93df-592">Method dragOverEx</span></span>

<span data-ttu-id="c93df-593">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-593">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="c93df-594">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="c93df-594">Parameters - dragOverEx</span></span>

<span data-ttu-id="c93df-595">dragSource</span><span class="sxs-lookup"><span data-stu-id="c93df-595">dragSource</span></span>  
<span data-ttu-id="c93df-596">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-596">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-597">dragMode</span><span class="sxs-lookup"><span data-stu-id="c93df-597">dragMode</span></span>  
<span data-ttu-id="c93df-598">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-598">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-599">x</span><span class="sxs-lookup"><span data-stu-id="c93df-599">x</span></span>  
<span data-ttu-id="c93df-600">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-600">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-601">y</span><span class="sxs-lookup"><span data-stu-id="c93df-601">y</span></span>  
<span data-ttu-id="c93df-602">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-602">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="c93df-603">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="c93df-603">Return Value - dragOverEx</span></span>

<span data-ttu-id="c93df-604">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="c93df-604">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="c93df-605">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="c93df-605">Method dragText</span></span>

<span data-ttu-id="c93df-606">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-606">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="c93df-607">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="c93df-607">Return Value - dragText</span></span>

<span data-ttu-id="c93df-608">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="c93df-608">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="c93df-609">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="c93df-609">Method enabled</span></span>

<span data-ttu-id="c93df-610">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-610">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="c93df-611">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="c93df-611">Parameters - enabled</span></span>

<span data-ttu-id="c93df-612">値</span><span class="sxs-lookup"><span data-stu-id="c93df-612">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="c93df-613">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="c93df-613">Return Value - enabled</span></span>

<span data-ttu-id="c93df-614">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-614">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="c93df-615">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="c93df-615">Remarks - enabled</span></span>

<span data-ttu-id="c93df-616">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="c93df-616">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="c93df-617">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c93df-617">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="c93df-618">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c93df-618">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="c93df-619">メソッド font</span><span class="sxs-lookup"><span data-stu-id="c93df-619">Method font</span></span>

<span data-ttu-id="c93df-620">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-620">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="c93df-621">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="c93df-621">Parameters - font</span></span>

<span data-ttu-id="c93df-622">値</span><span class="sxs-lookup"><span data-stu-id="c93df-622">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="c93df-623">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="c93df-623">Return Value - font</span></span>

<span data-ttu-id="c93df-624">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="c93df-624">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="c93df-625">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="c93df-625">Method fontSize</span></span>

<span data-ttu-id="c93df-626">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-626">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="c93df-627">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="c93df-627">Parameters - fontSize</span></span>

<span data-ttu-id="c93df-628">値</span><span class="sxs-lookup"><span data-stu-id="c93df-628">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="c93df-629">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="c93df-629">Return Value - fontSize</span></span>

<span data-ttu-id="c93df-630">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="c93df-630">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="c93df-631">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="c93df-631">Method foregroundColor</span></span>

<span data-ttu-id="c93df-632">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-632">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="c93df-633">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="c93df-633">Parameters - foregroundColor</span></span>

<span data-ttu-id="c93df-634">値</span><span class="sxs-lookup"><span data-stu-id="c93df-634">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="c93df-635">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="c93df-635">Return Value - foregroundColor</span></span>

<span data-ttu-id="c93df-636">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="c93df-636">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="c93df-637">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="c93df-637">Remarks - foregroundColor</span></span>

<span data-ttu-id="c93df-638">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c93df-638">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="c93df-639">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c93df-639">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="c93df-640">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="c93df-640">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="c93df-641">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="c93df-641">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="c93df-642">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c93df-642">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="c93df-643">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="c93df-643">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="c93df-644">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="c93df-644">Method hasChanged</span></span>

<span data-ttu-id="c93df-645">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-645">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="c93df-646">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="c93df-646">Parameters - hasChanged</span></span>

<span data-ttu-id="c93df-647">val</span><span class="sxs-lookup"><span data-stu-id="c93df-647">val</span></span>  
<span data-ttu-id="c93df-648">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-648">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="c93df-649">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="c93df-649">Return Value - hasChanged</span></span>

<span data-ttu-id="c93df-650">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-650">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="c93df-651">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="c93df-651">Method hasUserSetting</span></span>

<span data-ttu-id="c93df-652">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-652">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="c93df-653">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="c93df-653">Return Value - hasUserSetting</span></span>

<span data-ttu-id="c93df-654">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-654">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="c93df-655">メソッド height</span><span class="sxs-lookup"><span data-stu-id="c93df-655">Method height</span></span>

<span data-ttu-id="c93df-656">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-656">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="c93df-657">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="c93df-657">Parameters - height</span></span>

<span data-ttu-id="c93df-658">値</span><span class="sxs-lookup"><span data-stu-id="c93df-658">value</span></span>  

<!-- -->

<span data-ttu-id="c93df-659">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-659">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="c93df-660">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="c93df-660">Return Value - height</span></span>

<span data-ttu-id="c93df-661">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="c93df-661">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="c93df-662">備考 - height</span><span class="sxs-lookup"><span data-stu-id="c93df-662">Remarks - height</span></span>

<span data-ttu-id="c93df-663">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-663">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="c93df-664">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="c93df-664">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="c93df-665">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-665">Mode</span></span>            | <span data-ttu-id="c93df-666">高さの計算</span><span class="sxs-lookup"><span data-stu-id="c93df-666">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93df-667">-1 正確</span><span class="sxs-lookup"><span data-stu-id="c93df-667">-1 Exact</span></span>        | <span data-ttu-id="c93df-668">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-668">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="c93df-669">0 自動</span><span class="sxs-lookup"><span data-stu-id="c93df-669">0 Auto</span></span>          | <span data-ttu-id="c93df-670">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-670">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="c93df-671">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="c93df-671">1 Column height</span></span> | <span data-ttu-id="c93df-672">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="c93df-672">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="c93df-673">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="c93df-673">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="c93df-674">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="c93df-674">Method heightMode</span></span>

<span data-ttu-id="c93df-675">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-675">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="c93df-676">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="c93df-676">Parameters - heightMode</span></span>

<span data-ttu-id="c93df-677">値</span><span class="sxs-lookup"><span data-stu-id="c93df-677">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="c93df-678">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="c93df-678">Return Value - heightMode</span></span>

<span data-ttu-id="c93df-679">計算モード。</span><span class="sxs-lookup"><span data-stu-id="c93df-679">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="c93df-680">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="c93df-680">Remarks - heightMode</span></span>

<span data-ttu-id="c93df-681">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="c93df-681">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="c93df-682">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-682">Mode</span></span>          | <span data-ttu-id="c93df-683">高さの計算</span><span class="sxs-lookup"><span data-stu-id="c93df-683">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93df-684">正確</span><span class="sxs-lookup"><span data-stu-id="c93df-684">Exact</span></span>         | <span data-ttu-id="c93df-685">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-685">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="c93df-686">自動</span><span class="sxs-lookup"><span data-stu-id="c93df-686">Auto</span></span>          | <span data-ttu-id="c93df-687">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-687">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="c93df-688">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="c93df-688">Column height</span></span> | <span data-ttu-id="c93df-689">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="c93df-689">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="c93df-690">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="c93df-690">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="c93df-691">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="c93df-691">Method heightValue</span></span>

<span data-ttu-id="c93df-692">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-692">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="c93df-693">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="c93df-693">Parameters - heightValue</span></span>

<span data-ttu-id="c93df-694">値</span><span class="sxs-lookup"><span data-stu-id="c93df-694">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="c93df-695">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="c93df-695">Return Value - heightValue</span></span>

<span data-ttu-id="c93df-696">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="c93df-696">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="c93df-697">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="c93df-697">Remarks - heightValue</span></span>

<span data-ttu-id="c93df-698">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="c93df-698">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="c93df-699">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="c93df-699">Method helpField</span></span>

<span data-ttu-id="c93df-700">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-700">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="c93df-701">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="c93df-701">Return Value - helpField</span></span>

<span data-ttu-id="c93df-702">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="c93df-702">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="c93df-703">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="c93df-703">Remarks - helpField</span></span>

<span data-ttu-id="c93df-704">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c93df-704">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="c93df-705">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="c93df-705">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="c93df-706">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="c93df-706">Method helpText</span></span>

<span data-ttu-id="c93df-707">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-707">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="c93df-708">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="c93df-708">Parameters - helpText</span></span>

<span data-ttu-id="c93df-709">値</span><span class="sxs-lookup"><span data-stu-id="c93df-709">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="c93df-710">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="c93df-710">Return Value - helpText</span></span>

<span data-ttu-id="c93df-711">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="c93df-711">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="c93df-712">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="c93df-712">Remarks - helpText</span></span>

<span data-ttu-id="c93df-713">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-713">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="c93df-714">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="c93df-714">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="c93df-715">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="c93df-715">Method hierarchyParent</span></span>

<span data-ttu-id="c93df-716">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-716">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="c93df-717">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="c93df-717">Parameters - hierarchyParent</span></span>

<span data-ttu-id="c93df-718">値</span><span class="sxs-lookup"><span data-stu-id="c93df-718">value</span></span>  
<span data-ttu-id="c93df-719">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="c93df-719">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="c93df-720">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="c93df-720">Return Value - hierarchyParent</span></span>

<span data-ttu-id="c93df-721">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="c93df-721">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="c93df-722">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="c93df-722">Method hWnd</span></span>

<span data-ttu-id="c93df-723">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-723">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="c93df-724">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="c93df-724">Return Value - hWnd</span></span>

<span data-ttu-id="c93df-725">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="c93df-725">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="c93df-726">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="c93df-726">Remarks - hWnd</span></span>

<span data-ttu-id="c93df-727">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="c93df-727">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="c93df-728">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="c93df-728">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="c93df-729">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="c93df-729">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="c93df-730">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="c93df-730">Method isDisplayed</span></span>

<span data-ttu-id="c93df-731">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-731">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="c93df-732">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="c93df-732">Return Value - isDisplayed</span></span>

<span data-ttu-id="c93df-733">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="c93df-733">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="c93df-734">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="c93df-734">Remarks - isDisplayed</span></span>

<span data-ttu-id="c93df-735">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c93df-735">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="c93df-736">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="c93df-736">Method isRestricted</span></span>

<span data-ttu-id="c93df-737">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-737">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="c93df-738">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="c93df-738">Return Value - isRestricted</span></span>

<span data-ttu-id="c93df-739">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="c93df-739">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="c93df-740">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="c93df-740">Method isUserSetupEnabled</span></span>

<span data-ttu-id="c93df-741">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-741">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="c93df-742">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="c93df-742">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="c93df-743">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="c93df-743">neededSetupRights</span></span>  
<span data-ttu-id="c93df-744">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="c93df-744">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="c93df-745">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="c93df-745">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="c93df-746">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-746">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="c93df-747">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="c93df-747">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="c93df-748">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="c93df-748">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93df-749">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="c93df-749">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="c93df-750">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="c93df-750">No changes can be made to the control.</span></span> <span data-ttu-id="c93df-751">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-751">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="c93df-752">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="c93df-752">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="c93df-753">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="c93df-753">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="c93df-754">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="c93df-754">The user cannot move the control.</span></span>   |
| <span data-ttu-id="c93df-755">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="c93df-755">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="c93df-756">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="c93df-756">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="c93df-757">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="c93df-757">The user can also move the control.</span></span> |

<span data-ttu-id="c93df-758">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="c93df-758">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="c93df-759">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="c93df-759">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="c93df-760">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="c93df-760">Parameters - italic</span></span>

<span data-ttu-id="c93df-761">値</span><span class="sxs-lookup"><span data-stu-id="c93df-761">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="c93df-762">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="c93df-762">Return Value - italic</span></span>

## <a name="method-left"></a><span data-ttu-id="c93df-763">メソッド left</span><span class="sxs-lookup"><span data-stu-id="c93df-763">Method left</span></span>

<span data-ttu-id="c93df-764">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-764">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="c93df-765">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="c93df-765">Parameters - left</span></span>

<span data-ttu-id="c93df-766">値</span><span class="sxs-lookup"><span data-stu-id="c93df-766">value</span></span>  
<span data-ttu-id="c93df-767">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-767">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="c93df-768">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-768">mode</span></span>  
<span data-ttu-id="c93df-769">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-769">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="c93df-770">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="c93df-770">Return Value - left</span></span>

<span data-ttu-id="c93df-771">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="c93df-771">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="c93df-772">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="c93df-772">Method leftMode</span></span>

<span data-ttu-id="c93df-773">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-773">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="c93df-774">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="c93df-774">Parameters - leftMode</span></span>

<span data-ttu-id="c93df-775">値</span><span class="sxs-lookup"><span data-stu-id="c93df-775">value</span></span>  
<span data-ttu-id="c93df-776">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-776">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="c93df-777">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="c93df-777">Return Value - leftMode</span></span>

<span data-ttu-id="c93df-778">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="c93df-778">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="c93df-779">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="c93df-779">Method leftValue</span></span>

<span data-ttu-id="c93df-780">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-780">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="c93df-781">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="c93df-781">Parameters - leftValue</span></span>

<span data-ttu-id="c93df-782">値</span><span class="sxs-lookup"><span data-stu-id="c93df-782">value</span></span>  
<span data-ttu-id="c93df-783">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-783">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="c93df-784">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="c93df-784">Return Value - leftValue</span></span>

<span data-ttu-id="c93df-785">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="c93df-785">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="c93df-786">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c93df-786">Method markAsUserAdd</span></span>

<span data-ttu-id="c93df-787">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="c93df-787">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="c93df-788">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c93df-788">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="c93df-789">値</span><span class="sxs-lookup"><span data-stu-id="c93df-789">value</span></span>  
<span data-ttu-id="c93df-790">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-790">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="c93df-791">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c93df-791">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="c93df-792">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-792">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="c93df-793">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="c93df-793">Method mouseDblClick</span></span>

<span data-ttu-id="c93df-794">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-794">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="c93df-795">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="c93df-795">Parameters - mouseDblClick</span></span>

<span data-ttu-id="c93df-796">x</span><span class="sxs-lookup"><span data-stu-id="c93df-796">x</span></span>  
<span data-ttu-id="c93df-797">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-797">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-798">y</span><span class="sxs-lookup"><span data-stu-id="c93df-798">y</span></span>  
<span data-ttu-id="c93df-799">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-799">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-800">ボタン</span><span class="sxs-lookup"><span data-stu-id="c93df-800">button</span></span>  
<span data-ttu-id="c93df-801">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-801">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-802">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c93df-802">Ctrl</span></span>  
<span data-ttu-id="c93df-803">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-803">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-804">シフト</span><span class="sxs-lookup"><span data-stu-id="c93df-804">Shift</span></span>  
<span data-ttu-id="c93df-805">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-805">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="c93df-806">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="c93df-806">Return Value - mouseDblClick</span></span>

<span data-ttu-id="c93df-807">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c93df-807">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="c93df-808">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="c93df-808">Remarks - mouseDblClick</span></span>

<span data-ttu-id="c93df-809">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-809">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="c93df-810">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="c93df-810">Method mouseDown</span></span>

<span data-ttu-id="c93df-811">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-811">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="c93df-812">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="c93df-812">Parameters - mouseDown</span></span>

<span data-ttu-id="c93df-813">x</span><span class="sxs-lookup"><span data-stu-id="c93df-813">x</span></span>  
<span data-ttu-id="c93df-814">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-814">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-815">y</span><span class="sxs-lookup"><span data-stu-id="c93df-815">y</span></span>  
<span data-ttu-id="c93df-816">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-816">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-817">ボタン</span><span class="sxs-lookup"><span data-stu-id="c93df-817">button</span></span>  
<span data-ttu-id="c93df-818">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-818">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-819">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c93df-819">Ctrl</span></span>  
<span data-ttu-id="c93df-820">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-820">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-821">シフト</span><span class="sxs-lookup"><span data-stu-id="c93df-821">Shift</span></span>  
<span data-ttu-id="c93df-822">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-822">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="c93df-823">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="c93df-823">Return Value - mouseDown</span></span>

<span data-ttu-id="c93df-824">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c93df-824">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="c93df-825">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="c93df-825">Remarks - mouseDown</span></span>

<span data-ttu-id="c93df-826">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-826">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="c93df-827">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-827">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="c93df-828">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="c93df-828">Method mouseMove</span></span>

<span data-ttu-id="c93df-829">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-829">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="c93df-830">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="c93df-830">Parameters - mouseMove</span></span>

<span data-ttu-id="c93df-831">x</span><span class="sxs-lookup"><span data-stu-id="c93df-831">x</span></span>  
<span data-ttu-id="c93df-832">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-832">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-833">y</span><span class="sxs-lookup"><span data-stu-id="c93df-833">y</span></span>  
<span data-ttu-id="c93df-834">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-834">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-835">ボタン</span><span class="sxs-lookup"><span data-stu-id="c93df-835">button</span></span>  
<span data-ttu-id="c93df-836">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-836">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-837">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c93df-837">Ctrl</span></span>  
<span data-ttu-id="c93df-838">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-838">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-839">シフト</span><span class="sxs-lookup"><span data-stu-id="c93df-839">Shift</span></span>  
<span data-ttu-id="c93df-840">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-840">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="c93df-841">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="c93df-841">Return Value - mouseMove</span></span>

<span data-ttu-id="c93df-842">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c93df-842">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="c93df-843">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="c93df-843">Remarks - mouseMove</span></span>

<span data-ttu-id="c93df-844">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-844">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="c93df-845">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="c93df-845">Method mouseUp</span></span>

<span data-ttu-id="c93df-846">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-846">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="c93df-847">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="c93df-847">Parameters - mouseUp</span></span>

<span data-ttu-id="c93df-848">x</span><span class="sxs-lookup"><span data-stu-id="c93df-848">x</span></span>  
<span data-ttu-id="c93df-849">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-849">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-850">y</span><span class="sxs-lookup"><span data-stu-id="c93df-850">y</span></span>  
<span data-ttu-id="c93df-851">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-851">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-852">ボタン</span><span class="sxs-lookup"><span data-stu-id="c93df-852">button</span></span>  
<span data-ttu-id="c93df-853">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-853">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-854">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c93df-854">Ctrl</span></span>  
<span data-ttu-id="c93df-855">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-855">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-856">シフト</span><span class="sxs-lookup"><span data-stu-id="c93df-856">Shift</span></span>  
<span data-ttu-id="c93df-857">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-857">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="c93df-858">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="c93df-858">Return Value - mouseUp</span></span>

<span data-ttu-id="c93df-859">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c93df-859">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="c93df-860">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="c93df-860">Remarks - mouseUp</span></span>

<span data-ttu-id="c93df-861">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-861">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="c93df-862">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-862">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="c93df-863">メソッド名</span><span class="sxs-lookup"><span data-stu-id="c93df-863">Method name</span></span>

<span data-ttu-id="c93df-864">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-864">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="c93df-865">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="c93df-865">Parameters - name</span></span>

<span data-ttu-id="c93df-866">値</span><span class="sxs-lookup"><span data-stu-id="c93df-866">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="c93df-867">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="c93df-867">Return Value - name</span></span>

<span data-ttu-id="c93df-868">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="c93df-868">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="c93df-869">備考 - name</span><span class="sxs-lookup"><span data-stu-id="c93df-869">Remarks - name</span></span>

<span data-ttu-id="c93df-870">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c93df-870">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="c93df-871">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="c93df-871">It must start with a letter.</span></span>
-   <span data-ttu-id="c93df-872">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="c93df-872">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="c93df-873">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c93df-873">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="c93df-874">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="c93df-874">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="c93df-875">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="c93df-875">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="c93df-876">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="c93df-876">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="c93df-877">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="c93df-877">Parameters - neededPermission</span></span>

<span data-ttu-id="c93df-878">値</span><span class="sxs-lookup"><span data-stu-id="c93df-878">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="c93df-879">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="c93df-879">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="c93df-880">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c93df-880">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="c93df-881">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c93df-881">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="c93df-882">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="c93df-882">Method parentControl</span></span>

<span data-ttu-id="c93df-883">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-883">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="c93df-884">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="c93df-884">Return Value - parentControl</span></span>

<span data-ttu-id="c93df-885">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="c93df-885">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="c93df-886">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="c93df-886">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="c93df-887">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="c93df-887">Parameters - previewPartRef</span></span>

<span data-ttu-id="c93df-888">値</span><span class="sxs-lookup"><span data-stu-id="c93df-888">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="c93df-889">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="c93df-889">Return Value - previewPartRef</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="c93df-890">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="c93df-890">Method securityKey</span></span>

<span data-ttu-id="c93df-891">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-891">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="c93df-892">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="c93df-892">Parameters - securityKey</span></span>

<span data-ttu-id="c93df-893">値</span><span class="sxs-lookup"><span data-stu-id="c93df-893">value</span></span>  
<span data-ttu-id="c93df-894">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-894">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="c93df-895">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="c93df-895">Return Value - securityKey</span></span>

<span data-ttu-id="c93df-896">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="c93df-896">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="c93df-897">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="c93df-897">Method showContextMenu</span></span>

<span data-ttu-id="c93df-898">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-898">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="c93df-899">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="c93df-899">Parameters - showContextMenu</span></span>

<span data-ttu-id="c93df-900">menuHandle</span><span class="sxs-lookup"><span data-stu-id="c93df-900">menuHandle</span></span>  
<span data-ttu-id="c93df-901">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="c93df-901">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="c93df-902">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="c93df-902">Return Value - showContextMenu</span></span>

<span data-ttu-id="c93df-903">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-903">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="c93df-904">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="c93df-904">Method skip</span></span>

<span data-ttu-id="c93df-905">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-905">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="c93df-906">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="c93df-906">Parameters - skip</span></span>

<span data-ttu-id="c93df-907">値</span><span class="sxs-lookup"><span data-stu-id="c93df-907">value</span></span>  
<span data-ttu-id="c93df-908">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-908">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="c93df-909">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="c93df-909">Return Value - skip</span></span>

<span data-ttu-id="c93df-910">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c93df-910">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="c93df-911">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="c93df-911">Remarks - skip</span></span>

<span data-ttu-id="c93df-912">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="c93df-912">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="c93df-913">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="c93df-913">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="c93df-914">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="c93df-914">Parameters - sort</span></span>

<span data-ttu-id="c93df-915">sortDirection</span><span class="sxs-lookup"><span data-stu-id="c93df-915">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="c93df-916">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="c93df-916">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="c93df-917">メソッド style</span><span class="sxs-lookup"><span data-stu-id="c93df-917">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="c93df-918">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="c93df-918">Parameters - style</span></span>

<span data-ttu-id="c93df-919">値</span><span class="sxs-lookup"><span data-stu-id="c93df-919">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="c93df-920">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="c93df-920">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="c93df-921">メソッド text</span><span class="sxs-lookup"><span data-stu-id="c93df-921">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="c93df-922">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="c93df-922">Parameters - text</span></span>

<span data-ttu-id="c93df-923">値</span><span class="sxs-lookup"><span data-stu-id="c93df-923">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="c93df-924">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="c93df-924">Return Value - text</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="c93df-925">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="c93df-925">Method toolTip</span></span>

<span data-ttu-id="c93df-926">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="c93df-926">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="c93df-927">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="c93df-927">Return Value - toolTip</span></span>

<span data-ttu-id="c93df-928">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="c93df-928">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="c93df-929">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="c93df-929">Remarks - toolTip</span></span>

<span data-ttu-id="c93df-930">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="c93df-930">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="c93df-931">メソッド top</span><span class="sxs-lookup"><span data-stu-id="c93df-931">Method top</span></span>

<span data-ttu-id="c93df-932">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-932">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="c93df-933">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="c93df-933">Parameters - top</span></span>

<span data-ttu-id="c93df-934">値</span><span class="sxs-lookup"><span data-stu-id="c93df-934">value</span></span>  
<span data-ttu-id="c93df-935">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-935">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="c93df-936">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-936">mode</span></span>  
<span data-ttu-id="c93df-937">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-937">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="c93df-938">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="c93df-938">Return Value - top</span></span>

<span data-ttu-id="c93df-939">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="c93df-939">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="c93df-940">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="c93df-940">Method topMode</span></span>

<span data-ttu-id="c93df-941">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-941">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="c93df-942">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="c93df-942">Parameters - topMode</span></span>

<span data-ttu-id="c93df-943">値</span><span class="sxs-lookup"><span data-stu-id="c93df-943">value</span></span>  
<span data-ttu-id="c93df-944">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-944">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="c93df-945">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="c93df-945">Return Value - topMode</span></span>

<span data-ttu-id="c93df-946">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="c93df-946">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="c93df-947">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="c93df-947">Method topValue</span></span>

<span data-ttu-id="c93df-948">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-948">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="c93df-949">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="c93df-949">Parameters - topValue</span></span>

<span data-ttu-id="c93df-950">値</span><span class="sxs-lookup"><span data-stu-id="c93df-950">value</span></span>  
<span data-ttu-id="c93df-951">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-951">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="c93df-952">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="c93df-952">Return Value - topValue</span></span>

<span data-ttu-id="c93df-953">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="c93df-953">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="c93df-954">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="c93df-954">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="c93df-955">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="c93df-955">Parameters - type</span></span>

<span data-ttu-id="c93df-956">値</span><span class="sxs-lookup"><span data-stu-id="c93df-956">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="c93df-957">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="c93df-957">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="c93df-958">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="c93df-958">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="c93df-959">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="c93df-959">Parameters - underline</span></span>

<span data-ttu-id="c93df-960">値</span><span class="sxs-lookup"><span data-stu-id="c93df-960">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="c93df-961">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="c93df-961">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="c93df-962">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c93df-962">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="c93df-963">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c93df-963">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="c93df-964">データ</span><span class="sxs-lookup"><span data-stu-id="c93df-964">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="c93df-965">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c93df-965">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="c93df-966">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="c93df-966">Method userData</span></span>

<span data-ttu-id="c93df-967">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-967">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="c93df-968">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="c93df-968">Parameters - userData</span></span>

<span data-ttu-id="c93df-969">値</span><span class="sxs-lookup"><span data-stu-id="c93df-969">value</span></span>  
<span data-ttu-id="c93df-970">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-970">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="c93df-971">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="c93df-971">Return Value - userData</span></span>

<span data-ttu-id="c93df-972">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="c93df-972">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="c93df-973">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="c93df-973">Method userDataItem</span></span>

<span data-ttu-id="c93df-974">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-974">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="c93df-975">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="c93df-975">Parameters - userDataItem</span></span>

<span data-ttu-id="c93df-976">値</span><span class="sxs-lookup"><span data-stu-id="c93df-976">value</span></span>  
<span data-ttu-id="c93df-977">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-977">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="c93df-978">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="c93df-978">Return Value - userDataItem</span></span>

<span data-ttu-id="c93df-979">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="c93df-979">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="c93df-980">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="c93df-980">Method userDataItems</span></span>

<span data-ttu-id="c93df-981">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-981">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="c93df-982">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="c93df-982">Parameters - userDataItems</span></span>

<span data-ttu-id="c93df-983">値</span><span class="sxs-lookup"><span data-stu-id="c93df-983">value</span></span>  
<span data-ttu-id="c93df-984">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-984">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="c93df-985">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="c93df-985">Return Value - userDataItems</span></span>

<span data-ttu-id="c93df-986">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="c93df-986">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="c93df-987">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="c93df-987">Method userDisable</span></span>

<span data-ttu-id="c93df-988">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-988">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="c93df-989">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="c93df-989">Parameters - userDisable</span></span>

<span data-ttu-id="c93df-990">値</span><span class="sxs-lookup"><span data-stu-id="c93df-990">value</span></span>  
<span data-ttu-id="c93df-991">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-991">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="c93df-992">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="c93df-992">Return Value - userDisable</span></span>

<span data-ttu-id="c93df-993">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="c93df-993">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="c93df-994">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="c93df-994">Method userHeight</span></span>

<span data-ttu-id="c93df-995">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-995">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="c93df-996">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="c93df-996">Parameters - userHeight</span></span>

<span data-ttu-id="c93df-997">値</span><span class="sxs-lookup"><span data-stu-id="c93df-997">value</span></span>  
<span data-ttu-id="c93df-998">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-998">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="c93df-999">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="c93df-999">Return Value - userHeight</span></span>

<span data-ttu-id="c93df-1000">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="c93df-1000">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="c93df-1001">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="c93df-1001">Method userHide</span></span>

<span data-ttu-id="c93df-1002">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1002">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="c93df-1003">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="c93df-1003">Parameters - userHide</span></span>

<span data-ttu-id="c93df-1004">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1004">value</span></span>  
<span data-ttu-id="c93df-1005">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1005">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="c93df-1006">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="c93df-1006">Return Value - userHide</span></span>

<span data-ttu-id="c93df-1007">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="c93df-1007">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="c93df-1008">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="c93df-1008">Remarks - userHide</span></span>

<span data-ttu-id="c93df-1009">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1009">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="c93df-1010">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1010">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="c93df-1011">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1011">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="c93df-1012">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c93df-1012">Method userOrgContainer</span></span>

<span data-ttu-id="c93df-1013">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1013">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="c93df-1014">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c93df-1014">Parameters - userOrgContainer</span></span>

<span data-ttu-id="c93df-1015">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1015">value</span></span>  
<span data-ttu-id="c93df-1016">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1016">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="c93df-1017">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c93df-1017">Return Value - userOrgContainer</span></span>

<span data-ttu-id="c93df-1018">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="c93df-1018">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="c93df-1019">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c93df-1019">Method userOrgSibling</span></span>

<span data-ttu-id="c93df-1020">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1020">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="c93df-1021">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c93df-1021">Parameters - userOrgSibling</span></span>

<span data-ttu-id="c93df-1022">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1022">value</span></span>  
<span data-ttu-id="c93df-1023">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1023">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="c93df-1024">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c93df-1024">Return Value - userOrgSibling</span></span>

<span data-ttu-id="c93df-1025">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="c93df-1025">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="c93df-1026">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="c93df-1026">Method userPromptText</span></span>

<span data-ttu-id="c93df-1027">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1027">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="c93df-1028">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="c93df-1028">Parameters - userPromptText</span></span>

<span data-ttu-id="c93df-1029">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1029">value</span></span>  
<span data-ttu-id="c93df-1030">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1030">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="c93df-1031">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="c93df-1031">Return Value - userPromptText</span></span>

<span data-ttu-id="c93df-1032">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="c93df-1032">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="c93df-1033">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c93df-1033">Method userSecurityLevel</span></span>

<span data-ttu-id="c93df-1034">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1034">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="c93df-1035">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c93df-1035">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="c93df-1036">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1036">value</span></span>  
<span data-ttu-id="c93df-1037">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1037">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="c93df-1038">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c93df-1038">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="c93df-1039">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="c93df-1039">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="c93df-1040">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="c93df-1040">Method userSkip</span></span>

<span data-ttu-id="c93df-1041">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1041">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="c93df-1042">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="c93df-1042">Parameters - userSkip</span></span>

<span data-ttu-id="c93df-1043">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1043">value</span></span>  
<span data-ttu-id="c93df-1044">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1044">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="c93df-1045">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c93df-1045">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="c93df-1046">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="c93df-1046">Return Value - userSkip</span></span>

<span data-ttu-id="c93df-1047">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c93df-1047">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="c93df-1048">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="c93df-1048">Method userWidth</span></span>

<span data-ttu-id="c93df-1049">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1049">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="c93df-1050">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="c93df-1050">Parameters - userWidth</span></span>

<span data-ttu-id="c93df-1051">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1051">value</span></span>  
<span data-ttu-id="c93df-1052">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1052">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="c93df-1053">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="c93df-1053">Return Value - userWidth</span></span>

<span data-ttu-id="c93df-1054">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1054">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="c93df-1055">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="c93df-1055">Remarks - userWidth</span></span>

<span data-ttu-id="c93df-1056">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1056">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="c93df-1057">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="c93df-1057">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="c93df-1058">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1058">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="c93df-1059">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="c93df-1059">Method verticalSpacing</span></span>

<span data-ttu-id="c93df-1060">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1060">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="c93df-1061">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="c93df-1061">Parameters - verticalSpacing</span></span>

<span data-ttu-id="c93df-1062">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1062">value</span></span>  
<span data-ttu-id="c93df-1063">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-1063">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="c93df-1064">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-1064">mode</span></span>  
<span data-ttu-id="c93df-1065">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-1065">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="c93df-1066">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="c93df-1066">Return Value - verticalSpacing</span></span>

<span data-ttu-id="c93df-1067">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="c93df-1067">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="c93df-1068">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1068">Method verticalSpacingMode</span></span>

<span data-ttu-id="c93df-1069">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1069">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="c93df-1070">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1070">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="c93df-1071">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-1071">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="c93df-1072">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1072">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="c93df-1073">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="c93df-1073">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="c93df-1074">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="c93df-1074">Method verticalSpacingValue</span></span>

<span data-ttu-id="c93df-1075">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1075">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="c93df-1076">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="c93df-1076">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="c93df-1077">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1077">value</span></span>  
<span data-ttu-id="c93df-1078">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c93df-1078">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="c93df-1079">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="c93df-1079">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="c93df-1080">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="c93df-1080">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="c93df-1081">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="c93df-1081">Method visible</span></span>

<span data-ttu-id="c93df-1082">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1082">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="c93df-1083">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="c93df-1083">Parameters - visible</span></span>

<span data-ttu-id="c93df-1084">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1084">value</span></span>  
<span data-ttu-id="c93df-1085">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1085">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="c93df-1086">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="c93df-1086">Return Value - visible</span></span>

<span data-ttu-id="c93df-1087">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="c93df-1087">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="c93df-1088">メソッド width</span><span class="sxs-lookup"><span data-stu-id="c93df-1088">Method width</span></span>

<span data-ttu-id="c93df-1089">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1089">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="c93df-1090">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="c93df-1090">Parameters - width</span></span>

<span data-ttu-id="c93df-1091">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1091">value</span></span>  

<!-- -->

<span data-ttu-id="c93df-1092">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-1092">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="c93df-1093">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="c93df-1093">Return Value - width</span></span>

<span data-ttu-id="c93df-1094">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="c93df-1094">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="c93df-1095">備考 - width</span><span class="sxs-lookup"><span data-stu-id="c93df-1095">Remarks - width</span></span>

<span data-ttu-id="c93df-1096">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1096">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="c93df-1097">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1097">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="c93df-1098">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-1098">Mode</span></span>           | <span data-ttu-id="c93df-1099">幅計算</span><span class="sxs-lookup"><span data-stu-id="c93df-1099">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93df-1100">-1 正確</span><span class="sxs-lookup"><span data-stu-id="c93df-1100">-1 Exact</span></span>       | <span data-ttu-id="c93df-1101">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1101">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="c93df-1102">0 自動</span><span class="sxs-lookup"><span data-stu-id="c93df-1102">0 Auto</span></span>         | <span data-ttu-id="c93df-1103">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1103">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="c93df-1104">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="c93df-1104">1 Column width</span></span> | <span data-ttu-id="c93df-1105">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="c93df-1105">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="c93df-1106">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1106">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="c93df-1107">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1107">Method widthMode</span></span>

<span data-ttu-id="c93df-1108">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1108">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="c93df-1109">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1109">Parameters - widthMode</span></span>

<span data-ttu-id="c93df-1110">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1110">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="c93df-1111">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1111">Return Value - widthMode</span></span>

<span data-ttu-id="c93df-1112">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1112">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="c93df-1113">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1113">Remarks - widthMode</span></span>

<span data-ttu-id="c93df-1114">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1114">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="c93df-1115">モード</span><span class="sxs-lookup"><span data-stu-id="c93df-1115">Mode</span></span>         | <span data-ttu-id="c93df-1116">幅計算</span><span class="sxs-lookup"><span data-stu-id="c93df-1116">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93df-1117">正確</span><span class="sxs-lookup"><span data-stu-id="c93df-1117">Exact</span></span>        | <span data-ttu-id="c93df-1118">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1118">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="c93df-1119">自動</span><span class="sxs-lookup"><span data-stu-id="c93df-1119">Auto</span></span>         | <span data-ttu-id="c93df-1120">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1120">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="c93df-1121">列の幅</span><span class="sxs-lookup"><span data-stu-id="c93df-1121">Column width</span></span> | <span data-ttu-id="c93df-1122">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="c93df-1122">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="c93df-1123">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="c93df-1123">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="c93df-1124">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="c93df-1124">Method widthValue</span></span>

<span data-ttu-id="c93df-1125">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1125">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="c93df-1126">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="c93df-1126">Parameters - widthValue</span></span>

<span data-ttu-id="c93df-1127">値</span><span class="sxs-lookup"><span data-stu-id="c93df-1127">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="c93df-1128">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="c93df-1128">Return Value - widthValue</span></span>

<span data-ttu-id="c93df-1129">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="c93df-1129">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="c93df-1130">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="c93df-1130">Remarks - widthValue</span></span>

<span data-ttu-id="c93df-1131">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1131">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-paste"></a><span data-ttu-id="c93df-1132">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="c93df-1132">Method paste</span></span>

<span data-ttu-id="c93df-1133">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1133">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-filter"></a><span data-ttu-id="c93df-1134">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="c93df-1134">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="c93df-1135">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="c93df-1135">Parameters - filter</span></span>

<span data-ttu-id="c93df-1136">filterStr</span><span class="sxs-lookup"><span data-stu-id="c93df-1136">filterStr</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="c93df-1137">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="c93df-1137">Method endDrag</span></span>

<span data-ttu-id="c93df-1138">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1138">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="c93df-1139">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="c93df-1139">Remarks - endDrag</span></span>

<span data-ttu-id="c93df-1140">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="c93df-1140">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="c93df-1141">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1141">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-context"></a><span data-ttu-id="c93df-1142">メソッド context</span><span class="sxs-lookup"><span data-stu-id="c93df-1142">Method context</span></span>

<span data-ttu-id="c93df-1143">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1143">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="c93df-1144">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="c93df-1144">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="c93df-1145">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="c93df-1145">Parameters - OnGotFocus</span></span>

<span data-ttu-id="c93df-1146">sender</span><span class="sxs-lookup"><span data-stu-id="c93df-1146">sender</span></span>  

<!-- -->

<span data-ttu-id="c93df-1147">e</span><span class="sxs-lookup"><span data-stu-id="c93df-1147">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="c93df-1148">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="c93df-1148">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-lostfocus"></a><span data-ttu-id="c93df-1149">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="c93df-1149">Method lostFocus</span></span>

<span data-ttu-id="c93df-1150">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1150">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-copy"></a><span data-ttu-id="c93df-1151">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="c93df-1151">Method copy</span></span>

<span data-ttu-id="c93df-1152">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="c93df-1152">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="c93df-1153">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="c93df-1153">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="c93df-1154">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="c93df-1154">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="c93df-1155">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="c93df-1155">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="c93df-1156">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="c93df-1156">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="c93df-1157">overrideObject</span><span class="sxs-lookup"><span data-stu-id="c93df-1157">overrideObject</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="c93df-1158">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="c93df-1158">Method dropEx</span></span>

<span data-ttu-id="c93df-1159">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1159">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="c93df-1160">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="c93df-1160">Parameters - dropEx</span></span>

<span data-ttu-id="c93df-1161">dragSource</span><span class="sxs-lookup"><span data-stu-id="c93df-1161">dragSource</span></span>  
<span data-ttu-id="c93df-1162">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1162">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-1163">dragMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1163">dragMode</span></span>  
<span data-ttu-id="c93df-1164">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1164">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-1165">x</span><span class="sxs-lookup"><span data-stu-id="c93df-1165">x</span></span>  
<span data-ttu-id="c93df-1166">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1166">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-1167">y</span><span class="sxs-lookup"><span data-stu-id="c93df-1167">y</span></span>  
<span data-ttu-id="c93df-1168">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1168">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="c93df-1169">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="c93df-1169">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="c93df-1170">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="c93df-1170">Parameters - OnLostFocus</span></span>

<span data-ttu-id="c93df-1171">sender</span><span class="sxs-lookup"><span data-stu-id="c93df-1171">sender</span></span>  

<!-- -->

<span data-ttu-id="c93df-1172">e</span><span class="sxs-lookup"><span data-stu-id="c93df-1172">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="c93df-1173">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="c93df-1173">Method inputSearch</span></span>

<span data-ttu-id="c93df-1174">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1174">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="c93df-1175">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="c93df-1175">Parameters - inputSearch</span></span>

<span data-ttu-id="c93df-1176">searchStr</span><span class="sxs-lookup"><span data-stu-id="c93df-1176">searchStr</span></span>  
<span data-ttu-id="c93df-1177">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c93df-1177">The string value to use to filter data; optional.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="c93df-1178">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="c93df-1178">Method dragLeave</span></span>

<span data-ttu-id="c93df-1179">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1179">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-cut"></a><span data-ttu-id="c93df-1180">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="c93df-1180">Method cut</span></span>

<span data-ttu-id="c93df-1181">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="c93df-1181">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-setfocus"></a><span data-ttu-id="c93df-1182">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="c93df-1182">Method setFocus</span></span>

<span data-ttu-id="c93df-1183">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1183">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-drop"></a><span data-ttu-id="c93df-1184">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="c93df-1184">Method drop</span></span>

<span data-ttu-id="c93df-1185">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1185">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="c93df-1186">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="c93df-1186">Parameters - drop</span></span>

<span data-ttu-id="c93df-1187">dragSource</span><span class="sxs-lookup"><span data-stu-id="c93df-1187">dragSource</span></span>  
<span data-ttu-id="c93df-1188">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1188">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-1189">dragMode</span><span class="sxs-lookup"><span data-stu-id="c93df-1189">dragMode</span></span>  
<span data-ttu-id="c93df-1190">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1190">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-1191">x</span><span class="sxs-lookup"><span data-stu-id="c93df-1191">x</span></span>  
<span data-ttu-id="c93df-1192">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1192">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="c93df-1193">y</span><span class="sxs-lookup"><span data-stu-id="c93df-1193">y</span></span>  
<span data-ttu-id="c93df-1194">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1194">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="c93df-1195">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="c93df-1195">Method displayControl</span></span>

<span data-ttu-id="c93df-1196">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1196">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="c93df-1197">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="c93df-1197">Method resetUserSetting</span></span>

<span data-ttu-id="c93df-1198">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="c93df-1198">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="c93df-1199">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="c93df-1199">Method prefColumnSize</span></span>

<span data-ttu-id="c93df-1200">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1200">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="c93df-1201">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="c93df-1201">Parameters - prefColumnSize</span></span>

<span data-ttu-id="c93df-1202">width</span><span class="sxs-lookup"><span data-stu-id="c93df-1202">width</span></span>  
<span data-ttu-id="c93df-1203">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="c93df-1203">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="c93df-1204">height</span><span class="sxs-lookup"><span data-stu-id="c93df-1204">height</span></span>  
<span data-ttu-id="c93df-1205">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="c93df-1205">The preferred height of the control.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="c93df-1206">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="c93df-1206">Method mouseEnter</span></span>

<span data-ttu-id="c93df-1207">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c93df-1207">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="c93df-1208">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="c93df-1208">Parameters - mouseEnter</span></span>

<span data-ttu-id="c93df-1209">x</span><span class="sxs-lookup"><span data-stu-id="c93df-1209">x</span></span>  
<span data-ttu-id="c93df-1210">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1210">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-1211">y</span><span class="sxs-lookup"><span data-stu-id="c93df-1211">y</span></span>  
<span data-ttu-id="c93df-1212">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1212">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-1213">ボタン</span><span class="sxs-lookup"><span data-stu-id="c93df-1213">button</span></span>  
<span data-ttu-id="c93df-1214">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1214">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-1215">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c93df-1215">Ctrl</span></span>  
<span data-ttu-id="c93df-1216">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1216">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="c93df-1217">シフト</span><span class="sxs-lookup"><span data-stu-id="c93df-1217">Shift</span></span>  
<span data-ttu-id="c93df-1218">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c93df-1218">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="c93df-1219">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="c93df-1219">Method mouseLeave</span></span>

<span data-ttu-id="c93df-1220">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1220">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-gotfocus"></a><span data-ttu-id="c93df-1221">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="c93df-1221">Method gotFocus</span></span>

<span data-ttu-id="c93df-1222">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="c93df-1222">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

