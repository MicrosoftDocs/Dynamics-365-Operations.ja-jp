---
title: FormCheckBoxControl クラス
description: このトピックでは、FormCheckBoxControl クラスについて説明します。
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
ms.openlocfilehash: 336a6f0668bdfad3325ccd1463b4bdc71f21c899
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502951"
---
# <a name="class-formcheckboxcontrol"></a><span data-ttu-id="877e2-103">クラス FormCheckBoxControl</span><span class="sxs-lookup"><span data-stu-id="877e2-103">Class FormCheckBoxControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormCheckBoxControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="877e2-104">備考</span><span class="sxs-lookup"><span data-stu-id="877e2-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="877e2-105">例</span><span class="sxs-lookup"><span data-stu-id="877e2-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="877e2-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="877e2-106">Methods</span></span>

| <span data-ttu-id="877e2-107">方法</span><span class="sxs-lookup"><span data-stu-id="877e2-107">Method</span></span>                                                                                                      | <span data-ttu-id="877e2-108">説明</span><span class="sxs-lookup"><span data-stu-id="877e2-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="877e2-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="877e2-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="877e2-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="877e2-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="877e2-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="877e2-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="877e2-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="877e2-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="877e2-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="877e2-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="877e2-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-118">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="877e2-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-119">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="877e2-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-120">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="877e2-121">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="877e2-121">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="877e2-122">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-122">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="877e2-123">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-123">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="877e2-124">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="877e2-124">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="877e2-125">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-125">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="877e2-126">public boolean checked(\[boolean check\])</span><span class="sxs-lookup"><span data-stu-id="877e2-126">public boolean checked(\[boolean check\])</span></span>                                                                   | <span data-ttu-id="877e2-127">チェック ボックスの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-127">Gets or sets the value of a check box.</span></span>                                                                                                                                  |
| <span data-ttu-id="877e2-128">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-128">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="877e2-129">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-129">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="877e2-130">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-130">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="877e2-131">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-131">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="877e2-132">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="877e2-132">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="877e2-133">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-133">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="877e2-134">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-134">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="877e2-135">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-135">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="877e2-136">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-136">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="877e2-137">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-137">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="877e2-138">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-138">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="877e2-139">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-139">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="877e2-140">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-140">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="877e2-141">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-141">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="877e2-142">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-142">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="877e2-143">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-143">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="877e2-144">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-144">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="877e2-145">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-145">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="877e2-146">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-146">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="877e2-147">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="877e2-147">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="877e2-148">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-148">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="877e2-149">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="877e2-149">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="877e2-150">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-150">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="877e2-151">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="877e2-151">public str dragText()</span></span>                                                                                       | <span data-ttu-id="877e2-152">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-152">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="877e2-153">public boolean drawFocusRect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-153">public boolean drawFocusRect(\[boolean value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="877e2-154">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-154">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="877e2-155">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-155">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="877e2-156">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-156">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="877e2-157">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-157">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="877e2-158">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="877e2-158">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="877e2-159">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-159">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="877e2-160">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="877e2-160">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="877e2-161">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-161">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="877e2-162">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="877e2-162">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="877e2-163">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-163">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="877e2-164">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-164">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="877e2-165">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-165">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="877e2-166">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-166">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="877e2-167">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-167">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="877e2-168">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="877e2-168">public str helpField()</span></span>                                                                                      | <span data-ttu-id="877e2-169">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-169">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="877e2-170">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-170">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="877e2-171">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-171">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="877e2-172">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-172">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="877e2-173">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-173">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="877e2-174">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="877e2-174">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="877e2-175">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-175">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="877e2-176">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="877e2-176">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="877e2-177">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="877e2-177">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="877e2-178">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-178">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="877e2-179">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="877e2-179">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="877e2-180">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-180">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="877e2-181">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="877e2-181">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="877e2-182">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-182">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="877e2-183">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-183">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="877e2-184">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-184">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="877e2-185">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-185">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="877e2-186">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-186">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="877e2-187">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-187">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="877e2-188">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-188">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="877e2-189">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-189">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="877e2-190">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-190">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="877e2-191">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-191">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="877e2-192">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="877e2-192">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="877e2-193">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-193">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="877e2-194">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-194">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="877e2-195">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-195">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="877e2-196">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="877e2-196">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="877e2-197">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="877e2-197">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="877e2-198">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="877e2-198">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="877e2-199">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-199">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="877e2-200">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-200">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="877e2-201">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="877e2-201">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="877e2-202">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-202">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="877e2-203">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-203">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="877e2-204">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="877e2-204">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="877e2-205">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="877e2-205">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="877e2-206">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-206">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="877e2-207">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-207">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="877e2-208">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-208">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="877e2-209">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-209">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="877e2-210">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-210">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="877e2-211">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-211">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="877e2-212">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="877e2-212">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="877e2-213">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="877e2-213">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="877e2-214">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="877e2-214">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="877e2-215">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-215">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="877e2-216">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="877e2-216">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="877e2-217">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-217">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="877e2-218">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="877e2-218">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="877e2-219">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-219">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="877e2-220">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="877e2-220">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="877e2-221">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-221">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="877e2-222">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-222">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="877e2-223">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-223">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="877e2-224">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-224">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="877e2-225">public boolean optionalRecordControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-225">public boolean optionalRecordControl(\[boolean value\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="877e2-226">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="877e2-226">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="877e2-227">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="877e2-227">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="877e2-228">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-228">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="877e2-229">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-229">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="877e2-230">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-230">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="877e2-231">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-231">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="877e2-232">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-232">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="877e2-233">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="877e2-233">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="877e2-234">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-234">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="877e2-235">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-235">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="877e2-236">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-236">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="877e2-237">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-237">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="877e2-238">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="877e2-238">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="877e2-239">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-239">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="877e2-240">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="877e2-240">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="877e2-241">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-241">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="877e2-242">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="877e2-242">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="877e2-243">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-243">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="877e2-244">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-244">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="877e2-245">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-245">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="877e2-246">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-246">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="877e2-247">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-247">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="877e2-248">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-248">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="877e2-249">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="877e2-249">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="877e2-250">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-250">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="877e2-251">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-251">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="877e2-252">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-252">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="877e2-253">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-253">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="877e2-254">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-254">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="877e2-255">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-255">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="877e2-256">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-256">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="877e2-257">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-257">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="877e2-258">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-258">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="877e2-259">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-259">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="877e2-260">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-260">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="877e2-261">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-261">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="877e2-262">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-262">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="877e2-263">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-263">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="877e2-264">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-264">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="877e2-265">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-265">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="877e2-266">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-266">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="877e2-267">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-267">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="877e2-268">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-268">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="877e2-269">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-269">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="877e2-270">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-270">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="877e2-271">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-271">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="877e2-272">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-272">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="877e2-273">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-273">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="877e2-274">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="877e2-274">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="877e2-275">public int value(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-275">public int value(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="877e2-276">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="877e2-276">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="877e2-277">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-277">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="877e2-278">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="877e2-278">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="877e2-279">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-279">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="877e2-280">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-280">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="877e2-281">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-281">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="877e2-282">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-282">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="877e2-283">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-283">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="877e2-284">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-284">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="877e2-285">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="877e2-285">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="877e2-286">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-286">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="877e2-287">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-287">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="877e2-288">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-288">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="877e2-289">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="877e2-289">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="877e2-290">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-290">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="877e2-291">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="877e2-291">public void clicked()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="877e2-292">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-292">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="877e2-293">public void paste()</span><span class="sxs-lookup"><span data-stu-id="877e2-293">public void paste()</span></span>                                                                                         | <span data-ttu-id="877e2-294">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="877e2-294">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="877e2-295">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="877e2-295">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="877e2-296">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-296">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="877e2-297">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-297">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="877e2-298">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="877e2-298">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="877e2-299">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="877e2-299">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="877e2-300">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-300">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="877e2-301">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="877e2-301">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="877e2-302">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-302">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="877e2-303">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="877e2-303">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="877e2-304">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="877e2-304">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="877e2-305">public void undo()</span><span class="sxs-lookup"><span data-stu-id="877e2-305">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="877e2-306">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-306">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="877e2-307">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="877e2-307">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="877e2-308">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-308">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="877e2-309">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="877e2-309">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="877e2-310">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-310">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="877e2-311">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-311">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="877e2-312">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="877e2-312">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="877e2-313">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-313">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="877e2-314">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="877e2-314">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="877e2-315">public void context()</span><span class="sxs-lookup"><span data-stu-id="877e2-315">public void context()</span></span>                                                                                       | <span data-ttu-id="877e2-316">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-316">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="877e2-317">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="877e2-317">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="877e2-318">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-318">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="877e2-319">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="877e2-319">public void displayControl()</span></span>                                                                                | <span data-ttu-id="877e2-320">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-320">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="877e2-321">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-321">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="877e2-322">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-322">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="877e2-323">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="877e2-323">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="877e2-324">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-324">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="877e2-325">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="877e2-325">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="877e2-326">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-326">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="877e2-327">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="877e2-327">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="877e2-328">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="877e2-328">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="877e2-329">public void copy()</span><span class="sxs-lookup"><span data-stu-id="877e2-329">public void copy()</span></span>                                                                                          | <span data-ttu-id="877e2-330">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="877e2-330">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="877e2-331">public void enter()</span><span class="sxs-lookup"><span data-stu-id="877e2-331">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="877e2-332">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="877e2-332">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="877e2-333">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-333">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="877e2-334">public void cut()</span><span class="sxs-lookup"><span data-stu-id="877e2-334">public void cut()</span></span>                                                                                           | <span data-ttu-id="877e2-335">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="877e2-335">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="877e2-336">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="877e2-336">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="877e2-337">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="877e2-337">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="877e2-338">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-338">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="877e2-339">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="877e2-339">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="877e2-340">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-340">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |

## <a name="method-aligncontrol"></a><span data-ttu-id="877e2-341">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="877e2-341">Method alignControl</span></span>

<span data-ttu-id="877e2-342">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-342">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="877e2-343">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="877e2-343">Parameters - alignControl</span></span>

<span data-ttu-id="877e2-344">値</span><span class="sxs-lookup"><span data-stu-id="877e2-344">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="877e2-345">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="877e2-345">Return Value - alignControl</span></span>

<span data-ttu-id="877e2-346">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="877e2-346">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="877e2-347">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="877e2-347">Remarks - alignControl</span></span>

<span data-ttu-id="877e2-348">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-348">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="877e2-349">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="877e2-349">Method allowEdit</span></span>

<span data-ttu-id="877e2-350">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-350">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="877e2-351">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="877e2-351">Parameters - allowEdit</span></span>

<span data-ttu-id="877e2-352">値</span><span class="sxs-lookup"><span data-stu-id="877e2-352">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="877e2-353">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="877e2-353">Return Value - allowEdit</span></span>

<span data-ttu-id="877e2-354">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-354">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="877e2-355">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="877e2-355">Remarks - allowEdit</span></span>

<span data-ttu-id="877e2-356">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="877e2-356">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="877e2-357">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="877e2-357">Method allowSysSetup</span></span>

<span data-ttu-id="877e2-358">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-358">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="877e2-359">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="877e2-359">Return Value - allowSysSetup</span></span>

<span data-ttu-id="877e2-360">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-360">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="877e2-361">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="877e2-361">Method autoDeclaration</span></span>

<span data-ttu-id="877e2-362">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-362">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="877e2-363">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="877e2-363">Parameters - autoDeclaration</span></span>

<span data-ttu-id="877e2-364">値</span><span class="sxs-lookup"><span data-stu-id="877e2-364">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="877e2-365">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="877e2-365">Return Value - autoDeclaration</span></span>

<span data-ttu-id="877e2-366">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-366">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="877e2-367">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="877e2-367">Remarks - autoDeclaration</span></span>

<span data-ttu-id="877e2-368">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="877e2-368">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="877e2-369">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-369">Method backgroundColor</span></span>

<span data-ttu-id="877e2-370">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-370">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="877e2-371">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-371">Parameters - backgroundColor</span></span>

<span data-ttu-id="877e2-372">値</span><span class="sxs-lookup"><span data-stu-id="877e2-372">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="877e2-373">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-373">Return Value - backgroundColor</span></span>

<span data-ttu-id="877e2-374">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="877e2-374">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="877e2-375">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-375">Remarks - backgroundColor</span></span>

<span data-ttu-id="877e2-376">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="877e2-376">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="877e2-377">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="877e2-377">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="877e2-378">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="877e2-378">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="877e2-379">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="877e2-379">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="877e2-380">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="877e2-380">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="877e2-381">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="877e2-381">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="877e2-382">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="877e2-382">Method backStyle</span></span>

<span data-ttu-id="877e2-383">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-383">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="877e2-384">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="877e2-384">Parameters - backStyle</span></span>

<span data-ttu-id="877e2-385">値</span><span class="sxs-lookup"><span data-stu-id="877e2-385">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="877e2-386">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="877e2-386">Return Value - backStyle</span></span>

<span data-ttu-id="877e2-387">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="877e2-387">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="877e2-388">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="877e2-388">Method beginDrag</span></span>

<span data-ttu-id="877e2-389">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-389">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="877e2-390">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="877e2-390">Parameters - beginDrag</span></span>

<span data-ttu-id="877e2-391">x</span><span class="sxs-lookup"><span data-stu-id="877e2-391">x</span></span>  
<span data-ttu-id="877e2-392">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-392">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="877e2-393">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="877e2-393">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="877e2-394">y</span><span class="sxs-lookup"><span data-stu-id="877e2-394">y</span></span>  
<span data-ttu-id="877e2-395">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-395">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="877e2-396">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="877e2-396">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="877e2-397">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="877e2-397">Return Value - beginDrag</span></span>

<span data-ttu-id="877e2-398">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="877e2-398">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="877e2-399">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="877e2-399">Remarks - beginDrag</span></span>

<span data-ttu-id="877e2-400">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="877e2-400">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="877e2-401">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="877e2-401">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-cachedatamethod"></a><span data-ttu-id="877e2-402">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="877e2-402">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="877e2-403">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="877e2-403">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="877e2-404">値</span><span class="sxs-lookup"><span data-stu-id="877e2-404">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="877e2-405">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="877e2-405">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="877e2-406">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="877e2-406">Method calcControlSize</span></span>

<span data-ttu-id="877e2-407">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-407">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="877e2-408">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="877e2-408">Parameters - calcControlSize</span></span>

<span data-ttu-id="877e2-409">chars</span><span class="sxs-lookup"><span data-stu-id="877e2-409">chars</span></span>  
<span data-ttu-id="877e2-410">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="877e2-410">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="877e2-411">明細行</span><span class="sxs-lookup"><span data-stu-id="877e2-411">lines</span></span>  
<span data-ttu-id="877e2-412">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="877e2-412">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="877e2-413">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="877e2-413">Return Value - calcControlSize</span></span>

<span data-ttu-id="877e2-414">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="877e2-414">The container that holds the width and height.</span></span>

## <a name="method-checked"></a><span data-ttu-id="877e2-415">メソッド checked</span><span class="sxs-lookup"><span data-stu-id="877e2-415">Method checked</span></span>

<span data-ttu-id="877e2-416">チェック ボックスの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-416">Gets or sets the value of a check box.</span></span>

```xpp
public boolean checked([boolean check])
```

### <a name="parameters---checked"></a><span data-ttu-id="877e2-417">パラメーター - checked</span><span class="sxs-lookup"><span data-stu-id="877e2-417">Parameters - checked</span></span>

<span data-ttu-id="877e2-418">小切手</span><span class="sxs-lookup"><span data-stu-id="877e2-418">check</span></span>  
<span data-ttu-id="877e2-419">チェック ボックスが選択されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-419">A Boolean value that indicates whether the check box is selected; optional.</span></span> <span data-ttu-id="877e2-420">true の値は、チェック ボックスをオンにし、false の値は、オフにします。</span><span class="sxs-lookup"><span data-stu-id="877e2-420">A value of true selects the check box, and a value of false clears it.</span></span>

### <a name="return-value---checked"></a><span data-ttu-id="877e2-421">戻り値 - checked</span><span class="sxs-lookup"><span data-stu-id="877e2-421">Return Value - checked</span></span>

<span data-ttu-id="877e2-422">チェック ボックスがオンになっている場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="877e2-422">true if the check box is selected; otherwise false.</span></span>

### <a name="remarks---checked"></a><span data-ttu-id="877e2-423">備考 - checked</span><span class="sxs-lookup"><span data-stu-id="877e2-423">Remarks - checked</span></span>

<span data-ttu-id="877e2-424">このメソッドは、Win32 API を使用してプロパティを照会せずにチェック ボックスの値を取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-424">This method uses the Win32 API to get and set the value of the check box without querying the properties.</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="877e2-425">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="877e2-425">Method colorScheme</span></span>

<span data-ttu-id="877e2-426">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-426">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="877e2-427">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="877e2-427">Parameters - colorScheme</span></span>

<span data-ttu-id="877e2-428">値</span><span class="sxs-lookup"><span data-stu-id="877e2-428">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="877e2-429">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="877e2-429">Return Value - colorScheme</span></span>

<span data-ttu-id="877e2-430">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="877e2-430">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="877e2-431">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="877e2-431">Remarks - colorScheme</span></span>

<span data-ttu-id="877e2-432">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-432">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="877e2-433">値です。</span><span class="sxs-lookup"><span data-stu-id="877e2-433">Value.</span></span> | <span data-ttu-id="877e2-434">スタイル。</span><span class="sxs-lookup"><span data-stu-id="877e2-434">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="877e2-435">0</span><span class="sxs-lookup"><span data-stu-id="877e2-435">0</span></span>      | <span data-ttu-id="877e2-436">既定。</span><span class="sxs-lookup"><span data-stu-id="877e2-436">Default.</span></span>                      |
| <span data-ttu-id="877e2-437">1</span><span class="sxs-lookup"><span data-stu-id="877e2-437">1</span></span>      | <span data-ttu-id="877e2-438">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="877e2-438">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="877e2-439">2</span><span class="sxs-lookup"><span data-stu-id="877e2-439">2</span></span>      | <span data-ttu-id="877e2-440">真の配色。</span><span class="sxs-lookup"><span data-stu-id="877e2-440">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="877e2-441">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="877e2-441">Method configurationKey</span></span>

<span data-ttu-id="877e2-442">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-442">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="877e2-443">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="877e2-443">Parameters - configurationKey</span></span>

<span data-ttu-id="877e2-444">値</span><span class="sxs-lookup"><span data-stu-id="877e2-444">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="877e2-445">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="877e2-445">Return Value - configurationKey</span></span>

<span data-ttu-id="877e2-446">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="877e2-446">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="877e2-447">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="877e2-447">Remarks - configurationKey</span></span>

<span data-ttu-id="877e2-448">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-448">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="877e2-449">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="877e2-449">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="877e2-450">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="877e2-450">Method configurationKeyEx</span></span>

<span data-ttu-id="877e2-451">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-451">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="877e2-452">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="877e2-452">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="877e2-453">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="877e2-453">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="877e2-454">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="877e2-454">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="877e2-455">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="877e2-455">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="877e2-456">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="877e2-456">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="877e2-457">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="877e2-457">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="877e2-458">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="877e2-458">Method countryRegionCodes</span></span>

<span data-ttu-id="877e2-459">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-459">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="877e2-460">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="877e2-460">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="877e2-461">値</span><span class="sxs-lookup"><span data-stu-id="877e2-461">value</span></span>  
<span data-ttu-id="877e2-462">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-462">The string that contains the country region/codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="877e2-463">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="877e2-463">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="877e2-464">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="877e2-464">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="877e2-465">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="877e2-465">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="877e2-466">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="877e2-466">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="877e2-467">値</span><span class="sxs-lookup"><span data-stu-id="877e2-467">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="877e2-468">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="877e2-468">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="877e2-469">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="877e2-469">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="877e2-470">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="877e2-470">Parameters - dataField</span></span>

<span data-ttu-id="877e2-471">値</span><span class="sxs-lookup"><span data-stu-id="877e2-471">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="877e2-472">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="877e2-472">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="877e2-473">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="877e2-473">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="877e2-474">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="877e2-474">Parameters - dataMethod</span></span>

<span data-ttu-id="877e2-475">値</span><span class="sxs-lookup"><span data-stu-id="877e2-475">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="877e2-476">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="877e2-476">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="877e2-477">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="877e2-477">Method dataRelationPath</span></span>

<span data-ttu-id="877e2-478">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-478">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="877e2-479">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="877e2-479">Parameters - dataRelationPath</span></span>

<span data-ttu-id="877e2-480">値</span><span class="sxs-lookup"><span data-stu-id="877e2-480">value</span></span>  
<span data-ttu-id="877e2-481">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-481">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="877e2-482">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="877e2-482">Return Value - dataRelationPath</span></span>

<span data-ttu-id="877e2-483">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="877e2-483">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="877e2-484">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="877e2-484">Remarks - dataRelationPath</span></span>

<span data-ttu-id="877e2-485">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="877e2-485">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="877e2-486">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="877e2-486">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="877e2-487">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="877e2-487">Method dataSource</span></span>

<span data-ttu-id="877e2-488">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-488">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="877e2-489">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="877e2-489">Parameters - dataSource</span></span>

<span data-ttu-id="877e2-490">値</span><span class="sxs-lookup"><span data-stu-id="877e2-490">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="877e2-491">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="877e2-491">Return Value - dataSource</span></span>

<span data-ttu-id="877e2-492">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="877e2-492">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="877e2-493">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="877e2-493">Method displayTarget</span></span>

<span data-ttu-id="877e2-494">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-494">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="877e2-495">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="877e2-495">Parameters - displayTarget</span></span>

<span data-ttu-id="877e2-496">値</span><span class="sxs-lookup"><span data-stu-id="877e2-496">value</span></span>  
<span data-ttu-id="877e2-497">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-497">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="877e2-498">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="877e2-498">Return Value - displayTarget</span></span>

<span data-ttu-id="877e2-499">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="877e2-499">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="877e2-500">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="877e2-500">Method dragDrop</span></span>

<span data-ttu-id="877e2-501">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-501">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="877e2-502">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="877e2-502">Parameters - dragDrop</span></span>

<span data-ttu-id="877e2-503">値</span><span class="sxs-lookup"><span data-stu-id="877e2-503">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="877e2-504">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="877e2-504">Return Value - dragDrop</span></span>

<span data-ttu-id="877e2-505">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="877e2-505">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="877e2-506">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="877e2-506">Method dragOver</span></span>

<span data-ttu-id="877e2-507">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-507">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="877e2-508">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="877e2-508">Parameters - dragOver</span></span>

<span data-ttu-id="877e2-509">dragSource</span><span class="sxs-lookup"><span data-stu-id="877e2-509">dragSource</span></span>  
<span data-ttu-id="877e2-510">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-510">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-511">dragMode</span><span class="sxs-lookup"><span data-stu-id="877e2-511">dragMode</span></span>  
<span data-ttu-id="877e2-512">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-512">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-513">x</span><span class="sxs-lookup"><span data-stu-id="877e2-513">x</span></span>  
<span data-ttu-id="877e2-514">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-514">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-515">y</span><span class="sxs-lookup"><span data-stu-id="877e2-515">y</span></span>  
<span data-ttu-id="877e2-516">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-516">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="877e2-517">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="877e2-517">Return Value - dragOver</span></span>

<span data-ttu-id="877e2-518">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="877e2-518">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="877e2-519">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="877e2-519">Method dragOverEx</span></span>

<span data-ttu-id="877e2-520">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-520">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="877e2-521">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="877e2-521">Parameters - dragOverEx</span></span>

<span data-ttu-id="877e2-522">dragSource</span><span class="sxs-lookup"><span data-stu-id="877e2-522">dragSource</span></span>  
<span data-ttu-id="877e2-523">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-523">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-524">dragMode</span><span class="sxs-lookup"><span data-stu-id="877e2-524">dragMode</span></span>  
<span data-ttu-id="877e2-525">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-525">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-526">x</span><span class="sxs-lookup"><span data-stu-id="877e2-526">x</span></span>  
<span data-ttu-id="877e2-527">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-527">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-528">y</span><span class="sxs-lookup"><span data-stu-id="877e2-528">y</span></span>  
<span data-ttu-id="877e2-529">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-529">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="877e2-530">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="877e2-530">Return Value - dragOverEx</span></span>

<span data-ttu-id="877e2-531">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="877e2-531">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="877e2-532">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="877e2-532">Method dragText</span></span>

<span data-ttu-id="877e2-533">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-533">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="877e2-534">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="877e2-534">Return Value - dragText</span></span>

<span data-ttu-id="877e2-535">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="877e2-535">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-drawfocusrect"></a><span data-ttu-id="877e2-536">メソッド drawFocusRect</span><span class="sxs-lookup"><span data-stu-id="877e2-536">Method drawFocusRect</span></span>

```xpp
public boolean drawFocusRect([boolean value])
```

### <a name="parameters---drawfocusrect"></a><span data-ttu-id="877e2-537">パラメーター - drawFocusRect</span><span class="sxs-lookup"><span data-stu-id="877e2-537">Parameters - drawFocusRect</span></span>

<span data-ttu-id="877e2-538">値</span><span class="sxs-lookup"><span data-stu-id="877e2-538">value</span></span>  

### <a name="return-value---drawfocusrect"></a><span data-ttu-id="877e2-539">戻り値 - drawFocusRect</span><span class="sxs-lookup"><span data-stu-id="877e2-539">Return Value - drawFocusRect</span></span>

## <a name="method-enabled"></a><span data-ttu-id="877e2-540">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="877e2-540">Method enabled</span></span>

<span data-ttu-id="877e2-541">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-541">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="877e2-542">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="877e2-542">Parameters - enabled</span></span>

<span data-ttu-id="877e2-543">値</span><span class="sxs-lookup"><span data-stu-id="877e2-543">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="877e2-544">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="877e2-544">Return Value - enabled</span></span>

<span data-ttu-id="877e2-545">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-545">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="877e2-546">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="877e2-546">Remarks - enabled</span></span>

<span data-ttu-id="877e2-547">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="877e2-547">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="877e2-548">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="877e2-548">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="877e2-549">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="877e2-549">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="877e2-550">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-550">Method foregroundColor</span></span>

<span data-ttu-id="877e2-551">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-551">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="877e2-552">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-552">Parameters - foregroundColor</span></span>

<span data-ttu-id="877e2-553">値</span><span class="sxs-lookup"><span data-stu-id="877e2-553">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="877e2-554">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-554">Return Value - foregroundColor</span></span>

<span data-ttu-id="877e2-555">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="877e2-555">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="877e2-556">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-556">Remarks - foregroundColor</span></span>

<span data-ttu-id="877e2-557">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="877e2-557">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="877e2-558">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="877e2-558">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="877e2-559">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="877e2-559">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="877e2-560">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="877e2-560">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="877e2-561">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="877e2-561">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="877e2-562">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="877e2-562">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="877e2-563">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="877e2-563">Method hasChanged</span></span>

<span data-ttu-id="877e2-564">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-564">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="877e2-565">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="877e2-565">Parameters - hasChanged</span></span>

<span data-ttu-id="877e2-566">val</span><span class="sxs-lookup"><span data-stu-id="877e2-566">val</span></span>  
<span data-ttu-id="877e2-567">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-567">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="877e2-568">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="877e2-568">Return Value - hasChanged</span></span>

<span data-ttu-id="877e2-569">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-569">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="877e2-570">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="877e2-570">Method hasUserSetting</span></span>

<span data-ttu-id="877e2-571">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-571">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="877e2-572">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="877e2-572">Return Value - hasUserSetting</span></span>

<span data-ttu-id="877e2-573">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-573">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="877e2-574">メソッド height</span><span class="sxs-lookup"><span data-stu-id="877e2-574">Method height</span></span>

<span data-ttu-id="877e2-575">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-575">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="877e2-576">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="877e2-576">Parameters - height</span></span>

<span data-ttu-id="877e2-577">値</span><span class="sxs-lookup"><span data-stu-id="877e2-577">value</span></span>  

<!-- -->

<span data-ttu-id="877e2-578">モード</span><span class="sxs-lookup"><span data-stu-id="877e2-578">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="877e2-579">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="877e2-579">Return Value - height</span></span>

<span data-ttu-id="877e2-580">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="877e2-580">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="877e2-581">備考 - height</span><span class="sxs-lookup"><span data-stu-id="877e2-581">Remarks - height</span></span>

<span data-ttu-id="877e2-582">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-582">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="877e2-583">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="877e2-583">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="877e2-584">モード。</span><span class="sxs-lookup"><span data-stu-id="877e2-584">Mode.</span></span>            | <span data-ttu-id="877e2-585">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="877e2-585">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="877e2-586">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="877e2-586">-1 Exact.</span></span>        | <span data-ttu-id="877e2-587">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-587">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="877e2-588">0 自動。</span><span class="sxs-lookup"><span data-stu-id="877e2-588">0 Auto.</span></span>          | <span data-ttu-id="877e2-589">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-589">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="877e2-590">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="877e2-590">1 Column height.</span></span> | <span data-ttu-id="877e2-591">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="877e2-591">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="877e2-592">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="877e2-592">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="877e2-593">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="877e2-593">Method heightMode</span></span>

<span data-ttu-id="877e2-594">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-594">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="877e2-595">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="877e2-595">Parameters - heightMode</span></span>

<span data-ttu-id="877e2-596">値</span><span class="sxs-lookup"><span data-stu-id="877e2-596">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="877e2-597">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="877e2-597">Return Value - heightMode</span></span>

<span data-ttu-id="877e2-598">計算モード。</span><span class="sxs-lookup"><span data-stu-id="877e2-598">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="877e2-599">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="877e2-599">Remarks - heightMode</span></span>

<span data-ttu-id="877e2-600">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="877e2-600">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="877e2-601">モード。</span><span class="sxs-lookup"><span data-stu-id="877e2-601">Mode.</span></span>          | <span data-ttu-id="877e2-602">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="877e2-602">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="877e2-603">正確。</span><span class="sxs-lookup"><span data-stu-id="877e2-603">Exact.</span></span>         | <span data-ttu-id="877e2-604">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-604">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="877e2-605">自動。</span><span class="sxs-lookup"><span data-stu-id="877e2-605">Auto.</span></span>          | <span data-ttu-id="877e2-606">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-606">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="877e2-607">列の高さ</span><span class="sxs-lookup"><span data-stu-id="877e2-607">Column height.</span></span> | <span data-ttu-id="877e2-608">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="877e2-608">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="877e2-609">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="877e2-609">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="877e2-610">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="877e2-610">Method heightValue</span></span>

<span data-ttu-id="877e2-611">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-611">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="877e2-612">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="877e2-612">Parameters - heightValue</span></span>

<span data-ttu-id="877e2-613">値</span><span class="sxs-lookup"><span data-stu-id="877e2-613">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="877e2-614">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="877e2-614">Return Value - heightValue</span></span>

<span data-ttu-id="877e2-615">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="877e2-615">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="877e2-616">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="877e2-616">Remarks - heightValue</span></span>

<span data-ttu-id="877e2-617">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="877e2-617">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="877e2-618">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="877e2-618">Method helpField</span></span>

<span data-ttu-id="877e2-619">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-619">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="877e2-620">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="877e2-620">Return Value - helpField</span></span>

<span data-ttu-id="877e2-621">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="877e2-621">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="877e2-622">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="877e2-622">Remarks - helpField</span></span>

<span data-ttu-id="877e2-623">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="877e2-623">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="877e2-624">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="877e2-624">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="877e2-625">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="877e2-625">Method helpText</span></span>

<span data-ttu-id="877e2-626">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-626">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="877e2-627">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="877e2-627">Parameters - helpText</span></span>

<span data-ttu-id="877e2-628">値</span><span class="sxs-lookup"><span data-stu-id="877e2-628">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="877e2-629">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="877e2-629">Return Value - helpText</span></span>

<span data-ttu-id="877e2-630">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="877e2-630">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="877e2-631">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="877e2-631">Remarks - helpText</span></span>

<span data-ttu-id="877e2-632">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-632">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="877e2-633">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="877e2-633">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="877e2-634">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="877e2-634">Method hierarchyParent</span></span>

<span data-ttu-id="877e2-635">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-635">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="877e2-636">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="877e2-636">Parameters - hierarchyParent</span></span>

<span data-ttu-id="877e2-637">値</span><span class="sxs-lookup"><span data-stu-id="877e2-637">value</span></span>  
<span data-ttu-id="877e2-638">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="877e2-638">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="877e2-639">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="877e2-639">Return Value - hierarchyParent</span></span>

<span data-ttu-id="877e2-640">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="877e2-640">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="877e2-641">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="877e2-641">Method hWnd</span></span>

<span data-ttu-id="877e2-642">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-642">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="877e2-643">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="877e2-643">Return Value - hWnd</span></span>

<span data-ttu-id="877e2-644">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="877e2-644">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="877e2-645">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="877e2-645">Remarks - hWnd</span></span>

<span data-ttu-id="877e2-646">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="877e2-646">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="877e2-647">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="877e2-647">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="877e2-648">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="877e2-648">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="877e2-649">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="877e2-649">Method isDisplayed</span></span>

<span data-ttu-id="877e2-650">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-650">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="877e2-651">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="877e2-651">Return Value - isDisplayed</span></span>

<span data-ttu-id="877e2-652">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="877e2-652">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="877e2-653">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="877e2-653">Remarks - isDisplayed</span></span>

<span data-ttu-id="877e2-654">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="877e2-654">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="877e2-655">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="877e2-655">Method isRestricted</span></span>

<span data-ttu-id="877e2-656">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-656">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="877e2-657">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="877e2-657">Return Value - isRestricted</span></span>

<span data-ttu-id="877e2-658">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="877e2-658">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="877e2-659">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="877e2-659">Method isUserSetupEnabled</span></span>

<span data-ttu-id="877e2-660">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-660">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="877e2-661">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="877e2-661">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="877e2-662">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="877e2-662">neededSetupRights</span></span>  
<span data-ttu-id="877e2-663">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="877e2-663">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="877e2-664">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="877e2-664">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="877e2-665">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-665">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="877e2-666">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="877e2-666">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="877e2-667">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="877e2-667">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="877e2-668">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="877e2-668">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="877e2-669">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="877e2-669">No changes can be made to the control.</span></span> <span data-ttu-id="877e2-670">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-670">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="877e2-671">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="877e2-671">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="877e2-672">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="877e2-672">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="877e2-673">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="877e2-673">The user cannot move the control.</span></span>   |
| <span data-ttu-id="877e2-674">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="877e2-674">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="877e2-675">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="877e2-675">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="877e2-676">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="877e2-676">The user can also move the control.</span></span> |

<span data-ttu-id="877e2-677">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="877e2-677">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-label"></a><span data-ttu-id="877e2-678">メソッド label</span><span class="sxs-lookup"><span data-stu-id="877e2-678">Method label</span></span>

<span data-ttu-id="877e2-679">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-679">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="877e2-680">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="877e2-680">Parameters - label</span></span>

<span data-ttu-id="877e2-681">値</span><span class="sxs-lookup"><span data-stu-id="877e2-681">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="877e2-682">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="877e2-682">Return Value - label</span></span>

<span data-ttu-id="877e2-683">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="877e2-683">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="877e2-684">備考 - label</span><span class="sxs-lookup"><span data-stu-id="877e2-684">Remarks - label</span></span>

<span data-ttu-id="877e2-685">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-685">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="877e2-686">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="877e2-686">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="877e2-687">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="877e2-687">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="877e2-688">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="877e2-688">Parameters - labelAlignment</span></span>

<span data-ttu-id="877e2-689">値</span><span class="sxs-lookup"><span data-stu-id="877e2-689">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="877e2-690">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="877e2-690">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="877e2-691">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="877e2-691">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="877e2-692">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="877e2-692">Parameters - labelBold</span></span>

<span data-ttu-id="877e2-693">値</span><span class="sxs-lookup"><span data-stu-id="877e2-693">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="877e2-694">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="877e2-694">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="877e2-695">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="877e2-695">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="877e2-696">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="877e2-696">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="877e2-697">値</span><span class="sxs-lookup"><span data-stu-id="877e2-697">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="877e2-698">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="877e2-698">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="877e2-699">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="877e2-699">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="877e2-700">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="877e2-700">Parameters - labelFont</span></span>

<span data-ttu-id="877e2-701">値</span><span class="sxs-lookup"><span data-stu-id="877e2-701">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="877e2-702">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="877e2-702">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="877e2-703">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="877e2-703">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="877e2-704">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="877e2-704">Parameters - labelFontSize</span></span>

<span data-ttu-id="877e2-705">値</span><span class="sxs-lookup"><span data-stu-id="877e2-705">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="877e2-706">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="877e2-706">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="877e2-707">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-707">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="877e2-708">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-708">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="877e2-709">値</span><span class="sxs-lookup"><span data-stu-id="877e2-709">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="877e2-710">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="877e2-710">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="877e2-711">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="877e2-711">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="877e2-712">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="877e2-712">Parameters - labelGuide</span></span>

<span data-ttu-id="877e2-713">値</span><span class="sxs-lookup"><span data-stu-id="877e2-713">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="877e2-714">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="877e2-714">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="877e2-715">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="877e2-715">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="877e2-716">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="877e2-716">Parameters - labelHeight</span></span>

<span data-ttu-id="877e2-717">値</span><span class="sxs-lookup"><span data-stu-id="877e2-717">value</span></span>  

<!-- -->

<span data-ttu-id="877e2-718">モード</span><span class="sxs-lookup"><span data-stu-id="877e2-718">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="877e2-719">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="877e2-719">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="877e2-720">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="877e2-720">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="877e2-721">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="877e2-721">Parameters - labelHeightMode</span></span>

<span data-ttu-id="877e2-722">値</span><span class="sxs-lookup"><span data-stu-id="877e2-722">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="877e2-723">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="877e2-723">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="877e2-724">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="877e2-724">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="877e2-725">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="877e2-725">Parameters - labelHeightValue</span></span>

<span data-ttu-id="877e2-726">値</span><span class="sxs-lookup"><span data-stu-id="877e2-726">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="877e2-727">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="877e2-727">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="877e2-728">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="877e2-728">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="877e2-729">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="877e2-729">Parameters - labelItalic</span></span>

<span data-ttu-id="877e2-730">値</span><span class="sxs-lookup"><span data-stu-id="877e2-730">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="877e2-731">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="877e2-731">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="877e2-732">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="877e2-732">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="877e2-733">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="877e2-733">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="877e2-734">x</span><span class="sxs-lookup"><span data-stu-id="877e2-734">x</span></span>  

<!-- -->

<span data-ttu-id="877e2-735">y</span><span class="sxs-lookup"><span data-stu-id="877e2-735">y</span></span>  

<!-- -->

<span data-ttu-id="877e2-736">ボタン</span><span class="sxs-lookup"><span data-stu-id="877e2-736">button</span></span>  

<!-- -->

<span data-ttu-id="877e2-737">Ctrl</span><span class="sxs-lookup"><span data-stu-id="877e2-737">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="877e2-738">Shift</span><span class="sxs-lookup"><span data-stu-id="877e2-738">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="877e2-739">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="877e2-739">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="877e2-740">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="877e2-740">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="877e2-741">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="877e2-741">Parameters - labelMouseDown</span></span>

<span data-ttu-id="877e2-742">x</span><span class="sxs-lookup"><span data-stu-id="877e2-742">x</span></span>  

<!-- -->

<span data-ttu-id="877e2-743">y</span><span class="sxs-lookup"><span data-stu-id="877e2-743">y</span></span>  

<!-- -->

<span data-ttu-id="877e2-744">ボタン</span><span class="sxs-lookup"><span data-stu-id="877e2-744">button</span></span>  

<!-- -->

<span data-ttu-id="877e2-745">Ctrl</span><span class="sxs-lookup"><span data-stu-id="877e2-745">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="877e2-746">Shift</span><span class="sxs-lookup"><span data-stu-id="877e2-746">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="877e2-747">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="877e2-747">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="877e2-748">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="877e2-748">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="877e2-749">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="877e2-749">Parameters - labelMouseUp</span></span>

<span data-ttu-id="877e2-750">x</span><span class="sxs-lookup"><span data-stu-id="877e2-750">x</span></span>  

<!-- -->

<span data-ttu-id="877e2-751">y</span><span class="sxs-lookup"><span data-stu-id="877e2-751">y</span></span>  

<!-- -->

<span data-ttu-id="877e2-752">ボタン</span><span class="sxs-lookup"><span data-stu-id="877e2-752">button</span></span>  

<!-- -->

<span data-ttu-id="877e2-753">Ctrl</span><span class="sxs-lookup"><span data-stu-id="877e2-753">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="877e2-754">Shift</span><span class="sxs-lookup"><span data-stu-id="877e2-754">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="877e2-755">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="877e2-755">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="877e2-756">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="877e2-756">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="877e2-757">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="877e2-757">Parameters - labelPosition</span></span>

<span data-ttu-id="877e2-758">値</span><span class="sxs-lookup"><span data-stu-id="877e2-758">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="877e2-759">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="877e2-759">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="877e2-760">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="877e2-760">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="877e2-761">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="877e2-761">Parameters - labelUnderline</span></span>

<span data-ttu-id="877e2-762">値</span><span class="sxs-lookup"><span data-stu-id="877e2-762">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="877e2-763">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="877e2-763">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="877e2-764">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="877e2-764">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="877e2-765">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="877e2-765">Parameters - labelWidth</span></span>

<span data-ttu-id="877e2-766">値</span><span class="sxs-lookup"><span data-stu-id="877e2-766">value</span></span>  

<!-- -->

<span data-ttu-id="877e2-767">モード</span><span class="sxs-lookup"><span data-stu-id="877e2-767">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="877e2-768">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="877e2-768">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="877e2-769">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="877e2-769">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="877e2-770">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="877e2-770">Parameters - labelWidthMode</span></span>

<span data-ttu-id="877e2-771">値</span><span class="sxs-lookup"><span data-stu-id="877e2-771">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="877e2-772">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="877e2-772">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="877e2-773">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="877e2-773">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="877e2-774">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="877e2-774">Parameters - labelWidthValue</span></span>

<span data-ttu-id="877e2-775">値</span><span class="sxs-lookup"><span data-stu-id="877e2-775">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="877e2-776">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="877e2-776">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="877e2-777">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="877e2-777">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="877e2-778">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="877e2-778">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="877e2-779">メソッド left</span><span class="sxs-lookup"><span data-stu-id="877e2-779">Method left</span></span>

<span data-ttu-id="877e2-780">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-780">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="877e2-781">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="877e2-781">Parameters - left</span></span>

<span data-ttu-id="877e2-782">値</span><span class="sxs-lookup"><span data-stu-id="877e2-782">value</span></span>  
<span data-ttu-id="877e2-783">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-783">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="877e2-784">モード</span><span class="sxs-lookup"><span data-stu-id="877e2-784">mode</span></span>  
<span data-ttu-id="877e2-785">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-785">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="877e2-786">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="877e2-786">Return Value - left</span></span>

<span data-ttu-id="877e2-787">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="877e2-787">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="877e2-788">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="877e2-788">Method leftMode</span></span>

<span data-ttu-id="877e2-789">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-789">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="877e2-790">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="877e2-790">Parameters - leftMode</span></span>

<span data-ttu-id="877e2-791">値</span><span class="sxs-lookup"><span data-stu-id="877e2-791">value</span></span>  
<span data-ttu-id="877e2-792">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-792">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="877e2-793">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="877e2-793">Return Value - leftMode</span></span>

<span data-ttu-id="877e2-794">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="877e2-794">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="877e2-795">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="877e2-795">Method leftValue</span></span>

<span data-ttu-id="877e2-796">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-796">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="877e2-797">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="877e2-797">Parameters - leftValue</span></span>

<span data-ttu-id="877e2-798">値</span><span class="sxs-lookup"><span data-stu-id="877e2-798">value</span></span>  
<span data-ttu-id="877e2-799">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-799">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="877e2-800">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="877e2-800">Return Value - leftValue</span></span>

<span data-ttu-id="877e2-801">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="877e2-801">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="877e2-802">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="877e2-802">Method markAsUserAdd</span></span>

<span data-ttu-id="877e2-803">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="877e2-803">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="877e2-804">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="877e2-804">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="877e2-805">値</span><span class="sxs-lookup"><span data-stu-id="877e2-805">value</span></span>  
<span data-ttu-id="877e2-806">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-806">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="877e2-807">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="877e2-807">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="877e2-808">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-808">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="877e2-809">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="877e2-809">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="877e2-810">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="877e2-810">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="877e2-811">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="877e2-811">Method mouseDblClick</span></span>

<span data-ttu-id="877e2-812">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-812">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="877e2-813">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="877e2-813">Parameters - mouseDblClick</span></span>

<span data-ttu-id="877e2-814">x</span><span class="sxs-lookup"><span data-stu-id="877e2-814">x</span></span>  
<span data-ttu-id="877e2-815">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-815">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-816">y</span><span class="sxs-lookup"><span data-stu-id="877e2-816">y</span></span>  
<span data-ttu-id="877e2-817">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-817">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-818">ボタン</span><span class="sxs-lookup"><span data-stu-id="877e2-818">button</span></span>  
<span data-ttu-id="877e2-819">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-819">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-820">Ctrl</span><span class="sxs-lookup"><span data-stu-id="877e2-820">Ctrl</span></span>  
<span data-ttu-id="877e2-821">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-821">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-822">シフト</span><span class="sxs-lookup"><span data-stu-id="877e2-822">Shift</span></span>  
<span data-ttu-id="877e2-823">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-823">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="877e2-824">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="877e2-824">Return Value - mouseDblClick</span></span>

<span data-ttu-id="877e2-825">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="877e2-825">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="877e2-826">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="877e2-826">Remarks - mouseDblClick</span></span>

<span data-ttu-id="877e2-827">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-827">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="877e2-828">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="877e2-828">Method mouseDown</span></span>

<span data-ttu-id="877e2-829">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-829">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="877e2-830">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="877e2-830">Parameters - mouseDown</span></span>

<span data-ttu-id="877e2-831">x</span><span class="sxs-lookup"><span data-stu-id="877e2-831">x</span></span>  
<span data-ttu-id="877e2-832">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-832">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-833">y</span><span class="sxs-lookup"><span data-stu-id="877e2-833">y</span></span>  
<span data-ttu-id="877e2-834">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-834">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-835">ボタン</span><span class="sxs-lookup"><span data-stu-id="877e2-835">button</span></span>  
<span data-ttu-id="877e2-836">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-836">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-837">Ctrl</span><span class="sxs-lookup"><span data-stu-id="877e2-837">Ctrl</span></span>  
<span data-ttu-id="877e2-838">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-838">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-839">シフト</span><span class="sxs-lookup"><span data-stu-id="877e2-839">Shift</span></span>  
<span data-ttu-id="877e2-840">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-840">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="877e2-841">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="877e2-841">Return Value - mouseDown</span></span>

<span data-ttu-id="877e2-842">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="877e2-842">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="877e2-843">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="877e2-843">Remarks - mouseDown</span></span>

<span data-ttu-id="877e2-844">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-844">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="877e2-845">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-845">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="877e2-846">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="877e2-846">Method mouseMove</span></span>

<span data-ttu-id="877e2-847">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-847">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="877e2-848">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="877e2-848">Parameters - mouseMove</span></span>

<span data-ttu-id="877e2-849">x</span><span class="sxs-lookup"><span data-stu-id="877e2-849">x</span></span>  
<span data-ttu-id="877e2-850">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-850">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-851">y</span><span class="sxs-lookup"><span data-stu-id="877e2-851">y</span></span>  
<span data-ttu-id="877e2-852">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-852">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-853">ボタン</span><span class="sxs-lookup"><span data-stu-id="877e2-853">button</span></span>  
<span data-ttu-id="877e2-854">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-854">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-855">Ctrl</span><span class="sxs-lookup"><span data-stu-id="877e2-855">Ctrl</span></span>  
<span data-ttu-id="877e2-856">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-856">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-857">シフト</span><span class="sxs-lookup"><span data-stu-id="877e2-857">Shift</span></span>  
<span data-ttu-id="877e2-858">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-858">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="877e2-859">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="877e2-859">Return Value - mouseMove</span></span>

<span data-ttu-id="877e2-860">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="877e2-860">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="877e2-861">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="877e2-861">Remarks - mouseMove</span></span>

<span data-ttu-id="877e2-862">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-862">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="877e2-863">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="877e2-863">Method mouseUp</span></span>

<span data-ttu-id="877e2-864">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-864">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="877e2-865">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="877e2-865">Parameters - mouseUp</span></span>

<span data-ttu-id="877e2-866">x</span><span class="sxs-lookup"><span data-stu-id="877e2-866">x</span></span>  
<span data-ttu-id="877e2-867">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-867">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-868">y</span><span class="sxs-lookup"><span data-stu-id="877e2-868">y</span></span>  
<span data-ttu-id="877e2-869">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-869">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-870">ボタン</span><span class="sxs-lookup"><span data-stu-id="877e2-870">button</span></span>  
<span data-ttu-id="877e2-871">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-871">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-872">Ctrl</span><span class="sxs-lookup"><span data-stu-id="877e2-872">Ctrl</span></span>  
<span data-ttu-id="877e2-873">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-873">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-874">シフト</span><span class="sxs-lookup"><span data-stu-id="877e2-874">Shift</span></span>  
<span data-ttu-id="877e2-875">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-875">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="877e2-876">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="877e2-876">Return Value - mouseUp</span></span>

<span data-ttu-id="877e2-877">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="877e2-877">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="877e2-878">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="877e2-878">Remarks - mouseUp</span></span>

<span data-ttu-id="877e2-879">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-879">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="877e2-880">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-880">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="877e2-881">メソッド名</span><span class="sxs-lookup"><span data-stu-id="877e2-881">Method name</span></span>

<span data-ttu-id="877e2-882">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-882">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="877e2-883">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="877e2-883">Parameters - name</span></span>

<span data-ttu-id="877e2-884">値</span><span class="sxs-lookup"><span data-stu-id="877e2-884">value</span></span>  
<span data-ttu-id="877e2-885">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-885">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="877e2-886">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="877e2-886">Return Value - name</span></span>

<span data-ttu-id="877e2-887">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="877e2-887">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="877e2-888">備考 - name</span><span class="sxs-lookup"><span data-stu-id="877e2-888">Remarks - name</span></span>

<span data-ttu-id="877e2-889">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="877e2-889">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="877e2-890">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="877e2-890">It must start with a letter.</span></span>
-   <span data-ttu-id="877e2-891">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="877e2-891">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="877e2-892">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="877e2-892">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="877e2-893">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="877e2-893">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="877e2-894">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="877e2-894">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="877e2-895">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="877e2-895">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="877e2-896">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="877e2-896">Parameters - neededPermission</span></span>

<span data-ttu-id="877e2-897">値</span><span class="sxs-lookup"><span data-stu-id="877e2-897">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="877e2-898">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="877e2-898">Return Value - neededPermission</span></span>

## <a name="method-optionalrecordcontrol"></a><span data-ttu-id="877e2-899">メソッド optionalRecordControl</span><span class="sxs-lookup"><span data-stu-id="877e2-899">Method optionalRecordControl</span></span>

```xpp
public boolean optionalRecordControl([boolean value])
```

### <a name="parameters---optionalrecordcontrol"></a><span data-ttu-id="877e2-900">パラメーター - optionalRecordControl</span><span class="sxs-lookup"><span data-stu-id="877e2-900">Parameters - optionalRecordControl</span></span>

<span data-ttu-id="877e2-901">値</span><span class="sxs-lookup"><span data-stu-id="877e2-901">value</span></span>  

### <a name="return-value---optionalrecordcontrol"></a><span data-ttu-id="877e2-902">戻り値 - optionalRecordControl</span><span class="sxs-lookup"><span data-stu-id="877e2-902">Return Value - optionalRecordControl</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="877e2-903">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="877e2-903">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="877e2-904">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="877e2-904">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="877e2-905">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="877e2-905">Method parentControl</span></span>

<span data-ttu-id="877e2-906">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-906">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="877e2-907">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="877e2-907">Return Value - parentControl</span></span>

<span data-ttu-id="877e2-908">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="877e2-908">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="877e2-909">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="877e2-909">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="877e2-910">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="877e2-910">Parameters - previewPartRef</span></span>

<span data-ttu-id="877e2-911">値</span><span class="sxs-lookup"><span data-stu-id="877e2-911">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="877e2-912">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="877e2-912">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="877e2-913">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="877e2-913">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="877e2-914">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="877e2-914">Parameters - promptrect</span></span>

<span data-ttu-id="877e2-915">値</span><span class="sxs-lookup"><span data-stu-id="877e2-915">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="877e2-916">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="877e2-916">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="877e2-917">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="877e2-917">Method securityKey</span></span>

<span data-ttu-id="877e2-918">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-918">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="877e2-919">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="877e2-919">Parameters - securityKey</span></span>

<span data-ttu-id="877e2-920">値</span><span class="sxs-lookup"><span data-stu-id="877e2-920">value</span></span>  
<span data-ttu-id="877e2-921">コントロールに割り当てられているセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-921">The ID of the security key being assigned to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="877e2-922">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="877e2-922">Return Value - securityKey</span></span>

<span data-ttu-id="877e2-923">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="877e2-923">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="877e2-924">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="877e2-924">Method showContextMenu</span></span>

<span data-ttu-id="877e2-925">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-925">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="877e2-926">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="877e2-926">Parameters - showContextMenu</span></span>

<span data-ttu-id="877e2-927">menuHandle</span><span class="sxs-lookup"><span data-stu-id="877e2-927">menuHandle</span></span>  
<span data-ttu-id="877e2-928">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="877e2-928">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="877e2-929">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="877e2-929">Return Value - showContextMenu</span></span>

<span data-ttu-id="877e2-930">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-930">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="877e2-931">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="877e2-931">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="877e2-932">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="877e2-932">Parameters - showLabel</span></span>

<span data-ttu-id="877e2-933">値</span><span class="sxs-lookup"><span data-stu-id="877e2-933">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="877e2-934">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="877e2-934">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="877e2-935">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="877e2-935">Method skip</span></span>

<span data-ttu-id="877e2-936">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-936">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="877e2-937">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="877e2-937">Parameters - skip</span></span>

<span data-ttu-id="877e2-938">値</span><span class="sxs-lookup"><span data-stu-id="877e2-938">value</span></span>  
<span data-ttu-id="877e2-939">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-939">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="877e2-940">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="877e2-940">Return Value - skip</span></span>

<span data-ttu-id="877e2-941">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="877e2-941">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="877e2-942">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="877e2-942">Remarks - skip</span></span>

<span data-ttu-id="877e2-943">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="877e2-943">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="877e2-944">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="877e2-944">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="877e2-945">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="877e2-945">Parameters - sort</span></span>

<span data-ttu-id="877e2-946">sortDirection</span><span class="sxs-lookup"><span data-stu-id="877e2-946">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="877e2-947">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="877e2-947">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="877e2-948">メソッド style</span><span class="sxs-lookup"><span data-stu-id="877e2-948">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="877e2-949">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="877e2-949">Parameters - style</span></span>

<span data-ttu-id="877e2-950">値</span><span class="sxs-lookup"><span data-stu-id="877e2-950">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="877e2-951">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="877e2-951">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="877e2-952">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="877e2-952">Method toolTip</span></span>

<span data-ttu-id="877e2-953">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="877e2-953">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="877e2-954">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="877e2-954">Return Value - toolTip</span></span>

<span data-ttu-id="877e2-955">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="877e2-955">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="877e2-956">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="877e2-956">Remarks - toolTip</span></span>

<span data-ttu-id="877e2-957">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="877e2-957">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="877e2-958">メソッド top</span><span class="sxs-lookup"><span data-stu-id="877e2-958">Method top</span></span>

<span data-ttu-id="877e2-959">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-959">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="877e2-960">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="877e2-960">Parameters - top</span></span>

<span data-ttu-id="877e2-961">値</span><span class="sxs-lookup"><span data-stu-id="877e2-961">value</span></span>  
<span data-ttu-id="877e2-962">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-962">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="877e2-963">モード</span><span class="sxs-lookup"><span data-stu-id="877e2-963">mode</span></span>  
<span data-ttu-id="877e2-964">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-964">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="877e2-965">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="877e2-965">Return Value - top</span></span>

<span data-ttu-id="877e2-966">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="877e2-966">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="877e2-967">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="877e2-967">Method topMode</span></span>

<span data-ttu-id="877e2-968">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-968">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="877e2-969">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="877e2-969">Parameters - topMode</span></span>

<span data-ttu-id="877e2-970">値</span><span class="sxs-lookup"><span data-stu-id="877e2-970">value</span></span>  
<span data-ttu-id="877e2-971">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-971">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="877e2-972">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="877e2-972">Return Value - topMode</span></span>

<span data-ttu-id="877e2-973">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="877e2-973">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="877e2-974">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="877e2-974">Method topValue</span></span>

<span data-ttu-id="877e2-975">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-975">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="877e2-976">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="877e2-976">Parameters - topValue</span></span>

<span data-ttu-id="877e2-977">値</span><span class="sxs-lookup"><span data-stu-id="877e2-977">value</span></span>  
<span data-ttu-id="877e2-978">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-978">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="877e2-979">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="877e2-979">Return Value - topValue</span></span>

<span data-ttu-id="877e2-980">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="877e2-980">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="877e2-981">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="877e2-981">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="877e2-982">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="877e2-982">Parameters - type</span></span>

<span data-ttu-id="877e2-983">値</span><span class="sxs-lookup"><span data-stu-id="877e2-983">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="877e2-984">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="877e2-984">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="877e2-985">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="877e2-985">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="877e2-986">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="877e2-986">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="877e2-987">データ</span><span class="sxs-lookup"><span data-stu-id="877e2-987">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="877e2-988">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="877e2-988">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="877e2-989">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="877e2-989">Method userData</span></span>

<span data-ttu-id="877e2-990">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-990">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="877e2-991">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="877e2-991">Parameters - userData</span></span>

<span data-ttu-id="877e2-992">値</span><span class="sxs-lookup"><span data-stu-id="877e2-992">value</span></span>  
<span data-ttu-id="877e2-993">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-993">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="877e2-994">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="877e2-994">Return Value - userData</span></span>

<span data-ttu-id="877e2-995">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="877e2-995">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="877e2-996">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="877e2-996">Method userDataItem</span></span>

<span data-ttu-id="877e2-997">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-997">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="877e2-998">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="877e2-998">Parameters - userDataItem</span></span>

<span data-ttu-id="877e2-999">値</span><span class="sxs-lookup"><span data-stu-id="877e2-999">value</span></span>  
<span data-ttu-id="877e2-1000">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-1000">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="877e2-1001">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="877e2-1001">Return Value - userDataItem</span></span>

<span data-ttu-id="877e2-1002">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="877e2-1002">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="877e2-1003">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="877e2-1003">Method userDataItems</span></span>

<span data-ttu-id="877e2-1004">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1004">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="877e2-1005">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="877e2-1005">Parameters - userDataItems</span></span>

<span data-ttu-id="877e2-1006">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1006">value</span></span>  
<span data-ttu-id="877e2-1007">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-1007">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="877e2-1008">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="877e2-1008">Return Value - userDataItems</span></span>

<span data-ttu-id="877e2-1009">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="877e2-1009">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="877e2-1010">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="877e2-1010">Method userDisable</span></span>

<span data-ttu-id="877e2-1011">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1011">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="877e2-1012">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="877e2-1012">Parameters - userDisable</span></span>

<span data-ttu-id="877e2-1013">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1013">value</span></span>  
<span data-ttu-id="877e2-1014">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1014">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="877e2-1015">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="877e2-1015">Return Value - userDisable</span></span>

<span data-ttu-id="877e2-1016">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="877e2-1016">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="877e2-1017">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="877e2-1017">Method userHeight</span></span>

<span data-ttu-id="877e2-1018">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1018">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="877e2-1019">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="877e2-1019">Parameters - userHeight</span></span>

<span data-ttu-id="877e2-1020">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1020">value</span></span>  
<span data-ttu-id="877e2-1021">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1021">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="877e2-1022">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="877e2-1022">Return Value - userHeight</span></span>

<span data-ttu-id="877e2-1023">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="877e2-1023">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="877e2-1024">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="877e2-1024">Method userHide</span></span>

<span data-ttu-id="877e2-1025">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1025">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="877e2-1026">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="877e2-1026">Parameters - userHide</span></span>

<span data-ttu-id="877e2-1027">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1027">value</span></span>  
<span data-ttu-id="877e2-1028">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1028">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="877e2-1029">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="877e2-1029">Return Value - userHide</span></span>

<span data-ttu-id="877e2-1030">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="877e2-1030">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="877e2-1031">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="877e2-1031">Remarks - userHide</span></span>

<span data-ttu-id="877e2-1032">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1032">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="877e2-1033">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1033">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="877e2-1034">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1034">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="877e2-1035">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="877e2-1035">Method userOrgContainer</span></span>

<span data-ttu-id="877e2-1036">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1036">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="877e2-1037">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="877e2-1037">Parameters - userOrgContainer</span></span>

<span data-ttu-id="877e2-1038">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1038">value</span></span>  
<span data-ttu-id="877e2-1039">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1039">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="877e2-1040">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="877e2-1040">Return Value - userOrgContainer</span></span>

<span data-ttu-id="877e2-1041">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="877e2-1041">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="877e2-1042">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="877e2-1042">Method userOrgSibling</span></span>

<span data-ttu-id="877e2-1043">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1043">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="877e2-1044">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="877e2-1044">Parameters - userOrgSibling</span></span>

<span data-ttu-id="877e2-1045">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1045">value</span></span>  
<span data-ttu-id="877e2-1046">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1046">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="877e2-1047">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="877e2-1047">Return Value - userOrgSibling</span></span>

<span data-ttu-id="877e2-1048">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="877e2-1048">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="877e2-1049">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="877e2-1049">Method userPromptText</span></span>

<span data-ttu-id="877e2-1050">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1050">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="877e2-1051">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="877e2-1051">Parameters - userPromptText</span></span>

<span data-ttu-id="877e2-1052">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1052">value</span></span>  
<span data-ttu-id="877e2-1053">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1053">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="877e2-1054">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="877e2-1054">Return Value - userPromptText</span></span>

<span data-ttu-id="877e2-1055">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="877e2-1055">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="877e2-1056">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="877e2-1056">Method userSecurityLevel</span></span>

<span data-ttu-id="877e2-1057">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1057">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="877e2-1058">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="877e2-1058">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="877e2-1059">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1059">value</span></span>  
<span data-ttu-id="877e2-1060">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1060">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="877e2-1061">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="877e2-1061">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="877e2-1062">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="877e2-1062">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="877e2-1063">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="877e2-1063">Method userSkip</span></span>

<span data-ttu-id="877e2-1064">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1064">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="877e2-1065">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="877e2-1065">Parameters - userSkip</span></span>

<span data-ttu-id="877e2-1066">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1066">value</span></span>  
<span data-ttu-id="877e2-1067">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1067">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="877e2-1068">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="877e2-1068">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="877e2-1069">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="877e2-1069">Return Value - userSkip</span></span>

<span data-ttu-id="877e2-1070">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="877e2-1070">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="877e2-1071">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="877e2-1071">Method userWidth</span></span>

<span data-ttu-id="877e2-1072">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1072">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="877e2-1073">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="877e2-1073">Parameters - userWidth</span></span>

<span data-ttu-id="877e2-1074">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1074">value</span></span>  
<span data-ttu-id="877e2-1075">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1075">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="877e2-1076">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="877e2-1076">Return Value - userWidth</span></span>

<span data-ttu-id="877e2-1077">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1077">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="877e2-1078">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="877e2-1078">Remarks - userWidth</span></span>

<span data-ttu-id="877e2-1079">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1079">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="877e2-1080">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="877e2-1080">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="877e2-1081">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1081">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="877e2-1082">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="877e2-1082">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="877e2-1083">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="877e2-1083">Return Value - validate</span></span>

## <a name="method-value"></a><span data-ttu-id="877e2-1084">メソッド value</span><span class="sxs-lookup"><span data-stu-id="877e2-1084">Method value</span></span>

```xpp
public int value([int value])
```

### <a name="parameters---value"></a><span data-ttu-id="877e2-1085">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="877e2-1085">Parameters - value</span></span>

<span data-ttu-id="877e2-1086">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1086">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="877e2-1087">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="877e2-1087">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="877e2-1088">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="877e2-1088">Method verticalSpacing</span></span>

<span data-ttu-id="877e2-1089">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1089">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="877e2-1090">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="877e2-1090">Parameters - verticalSpacing</span></span>

<span data-ttu-id="877e2-1091">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1091">value</span></span>  
<span data-ttu-id="877e2-1092">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-1092">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="877e2-1093">モード</span><span class="sxs-lookup"><span data-stu-id="877e2-1093">mode</span></span>  
<span data-ttu-id="877e2-1094">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-1094">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="877e2-1095">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="877e2-1095">Return Value - verticalSpacing</span></span>

<span data-ttu-id="877e2-1096">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="877e2-1096">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="877e2-1097">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1097">Method verticalSpacingMode</span></span>

<span data-ttu-id="877e2-1098">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1098">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="877e2-1099">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1099">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="877e2-1100">モード</span><span class="sxs-lookup"><span data-stu-id="877e2-1100">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="877e2-1101">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1101">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="877e2-1102">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="877e2-1102">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="877e2-1103">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="877e2-1103">Method verticalSpacingValue</span></span>

<span data-ttu-id="877e2-1104">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1104">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="877e2-1105">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="877e2-1105">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="877e2-1106">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1106">value</span></span>  
<span data-ttu-id="877e2-1107">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="877e2-1107">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="877e2-1108">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="877e2-1108">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="877e2-1109">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="877e2-1109">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="877e2-1110">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1110">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="877e2-1111">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1111">Parameters - viewEditMode</span></span>

<span data-ttu-id="877e2-1112">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1112">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="877e2-1113">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1113">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="877e2-1114">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="877e2-1114">Method visible</span></span>

<span data-ttu-id="877e2-1115">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1115">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="877e2-1116">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="877e2-1116">Parameters - visible</span></span>

<span data-ttu-id="877e2-1117">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1117">value</span></span>  
<span data-ttu-id="877e2-1118">コントロールの表示設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1118">The value to assign to the visible setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="877e2-1119">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="877e2-1119">Return Value - visible</span></span>

<span data-ttu-id="877e2-1120">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="877e2-1120">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="877e2-1121">メソッド width</span><span class="sxs-lookup"><span data-stu-id="877e2-1121">Method width</span></span>

<span data-ttu-id="877e2-1122">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1122">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="877e2-1123">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="877e2-1123">Parameters - width</span></span>

<span data-ttu-id="877e2-1124">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1124">value</span></span>  

<!-- -->

<span data-ttu-id="877e2-1125">モード</span><span class="sxs-lookup"><span data-stu-id="877e2-1125">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="877e2-1126">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="877e2-1126">Return Value - width</span></span>

<span data-ttu-id="877e2-1127">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="877e2-1127">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="877e2-1128">備考 - width</span><span class="sxs-lookup"><span data-stu-id="877e2-1128">Remarks - width</span></span>

<span data-ttu-id="877e2-1129">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1129">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="877e2-1130">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="877e2-1130">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="877e2-1131">モード。</span><span class="sxs-lookup"><span data-stu-id="877e2-1131">Mode.</span></span>           | <span data-ttu-id="877e2-1132">幅計算。</span><span class="sxs-lookup"><span data-stu-id="877e2-1132">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="877e2-1133">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="877e2-1133">-1 Exact.</span></span>       | <span data-ttu-id="877e2-1134">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1134">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="877e2-1135">0 自動。</span><span class="sxs-lookup"><span data-stu-id="877e2-1135">0 Auto.</span></span>         | <span data-ttu-id="877e2-1136">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1136">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="877e2-1137">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="877e2-1137">1 Column width.</span></span> | <span data-ttu-id="877e2-1138">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="877e2-1138">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="877e2-1139">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1139">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="877e2-1140">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1140">Method widthMode</span></span>

<span data-ttu-id="877e2-1141">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1141">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="877e2-1142">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1142">Parameters - widthMode</span></span>

<span data-ttu-id="877e2-1143">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1143">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="877e2-1144">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1144">Return Value - widthMode</span></span>

<span data-ttu-id="877e2-1145">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1145">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="877e2-1146">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1146">Remarks - widthMode</span></span>

<span data-ttu-id="877e2-1147">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="877e2-1147">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="877e2-1148">モード。</span><span class="sxs-lookup"><span data-stu-id="877e2-1148">Mode.</span></span>         | <span data-ttu-id="877e2-1149">幅計算。</span><span class="sxs-lookup"><span data-stu-id="877e2-1149">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="877e2-1150">正確。</span><span class="sxs-lookup"><span data-stu-id="877e2-1150">Exact.</span></span>        | <span data-ttu-id="877e2-1151">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1151">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="877e2-1152">自動。</span><span class="sxs-lookup"><span data-stu-id="877e2-1152">Auto.</span></span>         | <span data-ttu-id="877e2-1153">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1153">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="877e2-1154">列の幅。</span><span class="sxs-lookup"><span data-stu-id="877e2-1154">Column width.</span></span> | <span data-ttu-id="877e2-1155">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="877e2-1155">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="877e2-1156">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="877e2-1156">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="877e2-1157">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="877e2-1157">Method widthValue</span></span>

<span data-ttu-id="877e2-1158">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1158">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="877e2-1159">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="877e2-1159">Parameters - widthValue</span></span>

<span data-ttu-id="877e2-1160">値</span><span class="sxs-lookup"><span data-stu-id="877e2-1160">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="877e2-1161">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="877e2-1161">Return Value - widthValue</span></span>

<span data-ttu-id="877e2-1162">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="877e2-1162">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="877e2-1163">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="877e2-1163">Remarks - widthValue</span></span>

<span data-ttu-id="877e2-1164">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1164">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-clicked"></a><span data-ttu-id="877e2-1165">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="877e2-1165">Method clicked</span></span>

```xpp
public void clicked()
```

## <a name="method-onleaving"></a><span data-ttu-id="877e2-1166">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="877e2-1166">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="877e2-1167">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="877e2-1167">Parameters - OnLeaving</span></span>

<span data-ttu-id="877e2-1168">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1168">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1169">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1169">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="877e2-1170">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="877e2-1170">Method paste</span></span>

<span data-ttu-id="877e2-1171">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1171">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-jumpref"></a><span data-ttu-id="877e2-1172">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="877e2-1172">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-onvalidated"></a><span data-ttu-id="877e2-1173">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="877e2-1173">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="877e2-1174">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="877e2-1174">Parameters - OnValidated</span></span>

<span data-ttu-id="877e2-1175">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1175">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1176">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1176">e</span></span>  

## <a name="method-onclicked"></a><span data-ttu-id="877e2-1177">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="877e2-1177">Method OnClicked</span></span>

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a><span data-ttu-id="877e2-1178">パラメーター - OnClicked</span><span class="sxs-lookup"><span data-stu-id="877e2-1178">Parameters - OnClicked</span></span>

<span data-ttu-id="877e2-1179">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1179">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1180">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1180">e</span></span>  

## <a name="method-filter"></a><span data-ttu-id="877e2-1181">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="877e2-1181">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="877e2-1182">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="877e2-1182">Parameters - filter</span></span>

<span data-ttu-id="877e2-1183">filterStr</span><span class="sxs-lookup"><span data-stu-id="877e2-1183">filterStr</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="877e2-1184">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="877e2-1184">Method mouseLeave</span></span>

<span data-ttu-id="877e2-1185">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1185">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-lostfocus"></a><span data-ttu-id="877e2-1186">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="877e2-1186">Method lostFocus</span></span>

<span data-ttu-id="877e2-1187">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1187">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-inputsearch"></a><span data-ttu-id="877e2-1188">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="877e2-1188">Method inputSearch</span></span>

<span data-ttu-id="877e2-1189">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1189">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="877e2-1190">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="877e2-1190">Parameters - inputSearch</span></span>

<span data-ttu-id="877e2-1191">searchStr</span><span class="sxs-lookup"><span data-stu-id="877e2-1191">searchStr</span></span>  
<span data-ttu-id="877e2-1192">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="877e2-1192">The string value to use to filter data; optional.</span></span>

## <a name="method-undo"></a><span data-ttu-id="877e2-1193">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="877e2-1193">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="877e2-1194">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="877e2-1194">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="877e2-1195">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="877e2-1195">Parameters - OnGotFocus</span></span>

<span data-ttu-id="877e2-1196">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1196">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1197">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1197">e</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="877e2-1198">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="877e2-1198">Method prefColumnSize</span></span>

<span data-ttu-id="877e2-1199">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1199">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="877e2-1200">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="877e2-1200">Parameters - prefColumnSize</span></span>

<span data-ttu-id="877e2-1201">width</span><span class="sxs-lookup"><span data-stu-id="877e2-1201">width</span></span>  
<span data-ttu-id="877e2-1202">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="877e2-1202">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="877e2-1203">height</span><span class="sxs-lookup"><span data-stu-id="877e2-1203">height</span></span>  
<span data-ttu-id="877e2-1204">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="877e2-1204">The preferred height of the control.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="877e2-1205">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="877e2-1205">Method setFocus</span></span>

<span data-ttu-id="877e2-1206">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1206">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-onmodified"></a><span data-ttu-id="877e2-1207">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="877e2-1207">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="877e2-1208">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="877e2-1208">Parameters - OnModified</span></span>

<span data-ttu-id="877e2-1209">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1209">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1210">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1210">e</span></span>  

## <a name="method-drop"></a><span data-ttu-id="877e2-1211">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="877e2-1211">Method drop</span></span>

<span data-ttu-id="877e2-1212">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1212">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="877e2-1213">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="877e2-1213">Parameters - drop</span></span>

<span data-ttu-id="877e2-1214">dragSource</span><span class="sxs-lookup"><span data-stu-id="877e2-1214">dragSource</span></span>  
<span data-ttu-id="877e2-1215">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1215">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-1216">dragMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1216">dragMode</span></span>  
<span data-ttu-id="877e2-1217">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1217">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-1218">x</span><span class="sxs-lookup"><span data-stu-id="877e2-1218">x</span></span>  
<span data-ttu-id="877e2-1219">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1219">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-1220">y</span><span class="sxs-lookup"><span data-stu-id="877e2-1220">y</span></span>  
<span data-ttu-id="877e2-1221">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1221">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="877e2-1222">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="877e2-1222">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="877e2-1223">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="877e2-1223">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="877e2-1224">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="877e2-1224">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="877e2-1225">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="877e2-1225">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="877e2-1226">overrideObject</span><span class="sxs-lookup"><span data-stu-id="877e2-1226">overrideObject</span></span>  

## <a name="method-context"></a><span data-ttu-id="877e2-1227">メソッド context</span><span class="sxs-lookup"><span data-stu-id="877e2-1227">Method context</span></span>

<span data-ttu-id="877e2-1228">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1228">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enddrag"></a><span data-ttu-id="877e2-1229">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="877e2-1229">Method endDrag</span></span>

<span data-ttu-id="877e2-1230">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1230">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="877e2-1231">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="877e2-1231">Remarks - endDrag</span></span>

<span data-ttu-id="877e2-1232">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="877e2-1232">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="877e2-1233">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1233">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="877e2-1234">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="877e2-1234">Method displayControl</span></span>

<span data-ttu-id="877e2-1235">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1235">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-onlookup"></a><span data-ttu-id="877e2-1236">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="877e2-1236">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="877e2-1237">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="877e2-1237">Parameters - OnLookup</span></span>

<span data-ttu-id="877e2-1238">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1238">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1239">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1239">e</span></span>  

## <a name="method-onvalidating"></a><span data-ttu-id="877e2-1240">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="877e2-1240">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="877e2-1241">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="877e2-1241">Parameters - OnValidating</span></span>

<span data-ttu-id="877e2-1242">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1242">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1243">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1243">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="877e2-1244">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="877e2-1244">Method dropEx</span></span>

<span data-ttu-id="877e2-1245">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1245">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="877e2-1246">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="877e2-1246">Parameters - dropEx</span></span>

<span data-ttu-id="877e2-1247">dragSource</span><span class="sxs-lookup"><span data-stu-id="877e2-1247">dragSource</span></span>  
<span data-ttu-id="877e2-1248">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1248">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-1249">dragMode</span><span class="sxs-lookup"><span data-stu-id="877e2-1249">dragMode</span></span>  
<span data-ttu-id="877e2-1250">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1250">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-1251">x</span><span class="sxs-lookup"><span data-stu-id="877e2-1251">x</span></span>  
<span data-ttu-id="877e2-1252">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1252">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="877e2-1253">y</span><span class="sxs-lookup"><span data-stu-id="877e2-1253">y</span></span>  
<span data-ttu-id="877e2-1254">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1254">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="877e2-1255">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="877e2-1255">Method dragLeave</span></span>

<span data-ttu-id="877e2-1256">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1256">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="877e2-1257">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="877e2-1257">Method resetUserSetting</span></span>

<span data-ttu-id="877e2-1258">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="877e2-1258">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-copy"></a><span data-ttu-id="877e2-1259">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="877e2-1259">Method copy</span></span>

<span data-ttu-id="877e2-1260">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="877e2-1260">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-enter"></a><span data-ttu-id="877e2-1261">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="877e2-1261">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-lookup"></a><span data-ttu-id="877e2-1262">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="877e2-1262">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-onenter"></a><span data-ttu-id="877e2-1263">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="877e2-1263">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="877e2-1264">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="877e2-1264">Parameters - OnEnter</span></span>

<span data-ttu-id="877e2-1265">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1265">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1266">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1266">e</span></span>  

## <a name="method-cut"></a><span data-ttu-id="877e2-1267">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="877e2-1267">Method cut</span></span>

<span data-ttu-id="877e2-1268">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="877e2-1268">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="877e2-1269">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="877e2-1269">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="877e2-1270">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="877e2-1270">Parameters - OnLostFocus</span></span>

<span data-ttu-id="877e2-1271">sender</span><span class="sxs-lookup"><span data-stu-id="877e2-1271">sender</span></span>  

<!-- -->

<span data-ttu-id="877e2-1272">e</span><span class="sxs-lookup"><span data-stu-id="877e2-1272">e</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="877e2-1273">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="877e2-1273">Method gotFocus</span></span>

<span data-ttu-id="877e2-1274">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="877e2-1274">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="877e2-1275">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="877e2-1275">Method mouseEnter</span></span>

<span data-ttu-id="877e2-1276">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="877e2-1276">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="877e2-1277">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="877e2-1277">Parameters - mouseEnter</span></span>

<span data-ttu-id="877e2-1278">x</span><span class="sxs-lookup"><span data-stu-id="877e2-1278">x</span></span>  
<span data-ttu-id="877e2-1279">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1279">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-1280">y</span><span class="sxs-lookup"><span data-stu-id="877e2-1280">y</span></span>  
<span data-ttu-id="877e2-1281">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1281">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-1282">ボタン</span><span class="sxs-lookup"><span data-stu-id="877e2-1282">button</span></span>  
<span data-ttu-id="877e2-1283">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1283">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-1284">Ctrl</span><span class="sxs-lookup"><span data-stu-id="877e2-1284">Ctrl</span></span>  
<span data-ttu-id="877e2-1285">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1285">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="877e2-1286">シフト</span><span class="sxs-lookup"><span data-stu-id="877e2-1286">Shift</span></span>  
<span data-ttu-id="877e2-1287">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="877e2-1287">A Boolean value that indicates whether the SHIFT key is down.</span></span>

