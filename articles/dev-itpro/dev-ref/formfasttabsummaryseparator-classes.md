---
title: F クラス (FormFastTabSummarySeparator から FormGridControl)
description: FormFastTabSummarySeparator から FormGridControl までのクラスの API 参照。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 63473
ms.assetid: 95c712f2-d71d-4dd1-a9fd-f1b88fe21807
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cc5985b683c0da547be0c5daf8ef65e8b5ebd5d
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595422"
---
# <a name="f-classes-formfasttabsummaryseparator-to-formgridcontrol"></a><span data-ttu-id="07b6d-103">F クラス (FormFastTabSummarySeparator から FormGridControl)</span><span class="sxs-lookup"><span data-stu-id="07b6d-103">F classes (FormFastTabSummarySeparator to FormGridControl)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07b6d-104">FormFastTabSummarySeparator から FormGridControl までのクラスの API 参照。</span><span class="sxs-lookup"><span data-stu-id="07b6d-104">API reference for classes from FormFastTabSummarySeparator to FormGridControl.</span></span>

<a name="class-formfasttabsummaryseparator"></a><span data-ttu-id="07b6d-105">クラス FormFastTabSummarySeparator</span><span class="sxs-lookup"><span data-stu-id="07b6d-105">Class FormFastTabSummarySeparator</span></span>
---------------------------------

    class FormFastTabSummarySeparator extends FormControl

### <a name="remarks"></a><span data-ttu-id="07b6d-106">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="07b6d-107">例</span><span class="sxs-lookup"><span data-stu-id="07b6d-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="07b6d-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="07b6d-108">Methods</span></span>

| <span data-ttu-id="07b6d-109">方法</span><span class="sxs-lookup"><span data-stu-id="07b6d-109">Method</span></span>                                                                                                      | <span data-ttu-id="07b6d-110">説明</span><span class="sxs-lookup"><span data-stu-id="07b6d-110">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="07b6d-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-112">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="07b6d-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-114">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-115">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="07b6d-115">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="07b6d-116">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-116">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="07b6d-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="07b6d-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="07b6d-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="07b6d-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="07b6d-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="07b6d-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="07b6d-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-126">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-127">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="07b6d-127">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="07b6d-128">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-128">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="07b6d-129">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-129">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="07b6d-130">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-130">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-131">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-131">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="07b6d-132">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-132">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="07b6d-134">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-134">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-135">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="07b6d-135">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="07b6d-136">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-136">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-137">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-137">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="07b6d-138">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-138">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="07b6d-139">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-139">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="07b6d-140">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-140">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="07b6d-141">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-141">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="07b6d-142">コントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-142">Gets or sets the value that indicates whether the control is displayed.</span></span> |
| <span data-ttu-id="07b6d-143">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-143">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-144">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-144">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="07b6d-145">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-145">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="07b6d-146">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-146">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="07b6d-147">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-147">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="07b6d-148">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-148">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-149">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="07b6d-149">public str dragText()</span></span>                                                                                       | <span data-ttu-id="07b6d-150">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-150">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-151">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-151">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="07b6d-152">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-152">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-153">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-153">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="07b6d-154">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-154">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="07b6d-155">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-155">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-156">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-156">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="07b6d-157">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-157">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="07b6d-158">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-158">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="07b6d-159">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="07b6d-159">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="07b6d-160">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-160">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="07b6d-161">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-161">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="07b6d-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-162">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-163">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-165">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-165">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="07b6d-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-166">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-167">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="07b6d-167">public str helpField()</span></span>                                                                                      | <span data-ttu-id="07b6d-168">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-168">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-169">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-169">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="07b6d-170">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-170">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="07b6d-171">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-171">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="07b6d-172">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-172">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="07b6d-173">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="07b6d-173">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="07b6d-174">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-174">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-175">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="07b6d-175">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-176">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="07b6d-176">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="07b6d-177">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-177">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="07b6d-178">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="07b6d-178">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="07b6d-179">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-179">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-180">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="07b6d-180">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="07b6d-181">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-181">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="07b6d-182">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-182">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-183">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-183">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="07b6d-184">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-184">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="07b6d-185">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-185">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-186">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-186">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-187">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-187">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-188">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-188">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="07b6d-189">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-189">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="07b6d-190">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-190">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="07b6d-191">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-191">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="07b6d-192">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-192">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="07b6d-193">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-193">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="07b6d-194">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-194">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-195">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-195">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="07b6d-196">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-196">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-197">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-197">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="07b6d-198">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-198">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="07b6d-199">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-199">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="07b6d-200">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-200">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="07b6d-201">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-201">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-202">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="07b6d-202">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-203">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="07b6d-203">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="07b6d-204">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-204">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-205">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-205">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="07b6d-206">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-206">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-207">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="07b6d-207">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="07b6d-208">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-208">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-209">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-209">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="07b6d-210">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-210">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="07b6d-211">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="07b6d-211">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="07b6d-212">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-212">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-213">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-213">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="07b6d-214">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-214">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-215">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-215">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="07b6d-216">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-216">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-217">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-217">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-218">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-218">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-219">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-219">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-220">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-220">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-221">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="07b6d-221">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-222">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-222">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-223">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-223">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-224">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-224">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="07b6d-225">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-225">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="07b6d-226">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-226">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="07b6d-227">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-227">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-228">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-228">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="07b6d-229">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-229">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="07b6d-230">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-230">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-231">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-231">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="07b6d-232">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-232">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-233">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-233">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="07b6d-234">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-234">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="07b6d-235">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-235">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="07b6d-236">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-236">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="07b6d-237">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-237">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-238">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-238">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="07b6d-239">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-239">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="07b6d-240">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-240">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="07b6d-241">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-241">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="07b6d-242">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-242">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-243">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-243">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="07b6d-244">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-244">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-245">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-245">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-246">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-246">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="07b6d-247">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-247">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-248">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-248">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="07b6d-249">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-249">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-250">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-250">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="07b6d-251">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-251">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-252">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-252">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="07b6d-253">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-253">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-254">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-254">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="07b6d-255">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-255">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="07b6d-256">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-256">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-257">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-257">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-258">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-258">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-259">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-259">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="07b6d-260">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-260">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="07b6d-261">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-261">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="07b6d-262">public void copy()</span><span class="sxs-lookup"><span data-stu-id="07b6d-262">public void copy()</span></span>                                                                                          | <span data-ttu-id="07b6d-263">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-263">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="07b6d-264">public void cut()</span><span class="sxs-lookup"><span data-stu-id="07b6d-264">public void cut()</span></span>                                                                                           | <span data-ttu-id="07b6d-265">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-265">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="07b6d-266">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-266">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="07b6d-267">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-267">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="07b6d-268">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-268">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="07b6d-269">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-269">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-270">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="07b6d-270">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="07b6d-271">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-271">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-272">public void context()</span><span class="sxs-lookup"><span data-stu-id="07b6d-272">public void context()</span></span>                                                                                       | <span data-ttu-id="07b6d-273">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-273">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-274">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-274">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="07b6d-275">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-275">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="07b6d-276">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="07b6d-276">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="07b6d-277">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-277">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="07b6d-278">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-278">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="07b6d-279">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-279">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="07b6d-280">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="07b6d-280">public void displayControl()</span></span>                                                                                | <span data-ttu-id="07b6d-281">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-281">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="07b6d-282">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-282">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-283">public void paste()</span><span class="sxs-lookup"><span data-stu-id="07b6d-283">public void paste()</span></span>                                                                                         | <span data-ttu-id="07b6d-284">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-284">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-285">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="07b6d-285">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="07b6d-286">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-286">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="07b6d-287">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-287">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="07b6d-288">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-288">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="07b6d-289">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-289">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="07b6d-290">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-290">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-291">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="07b6d-291">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="07b6d-292">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-292">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="07b6d-293">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-293">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="07b6d-294">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-294">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |

### <a name="method-aligncontrol"></a><span data-ttu-id="07b6d-295">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-295">Method alignControl</span></span>

<span data-ttu-id="07b6d-296">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-296">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-297">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-297">Parameters</span></span>

<span data-ttu-id="07b6d-298">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-298">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-299">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-299">Return Value</span></span>

<span data-ttu-id="07b6d-300">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-300">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-301">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-301">Remarks</span></span>

<span data-ttu-id="07b6d-302">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-302">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="07b6d-303">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="07b6d-303">Method allowEdit</span></span>

<span data-ttu-id="07b6d-304">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-304">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-305">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-305">Parameters</span></span>

<span data-ttu-id="07b6d-306">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-306">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-307">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-307">Return Value</span></span>

<span data-ttu-id="07b6d-308">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-308">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-309">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-309">Remarks</span></span>

<span data-ttu-id="07b6d-310">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-310">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="07b6d-311">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="07b6d-311">Method allowSysSetup</span></span>

<span data-ttu-id="07b6d-312">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-312">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="07b6d-313">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-313">Return Value</span></span>

<span data-ttu-id="07b6d-314">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-314">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="07b6d-315">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="07b6d-315">Method autoDeclaration</span></span>

<span data-ttu-id="07b6d-316">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-316">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-317">Parameters</span></span>

<span data-ttu-id="07b6d-318">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-318">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-319">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-319">Return Value</span></span>

<span data-ttu-id="07b6d-320">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-320">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-321">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-321">Remarks</span></span>

<span data-ttu-id="07b6d-322">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-322">Controls cannot have identical names.</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="07b6d-323">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="07b6d-323">Method backgroundColor</span></span>

<span data-ttu-id="07b6d-324">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-324">Gets or sets the background color of the control.</span></span>

    public int backgroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-325">Parameters</span></span>

<span data-ttu-id="07b6d-326">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-326">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-327">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-327">Return Value</span></span>

<span data-ttu-id="07b6d-328">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-328">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-329">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-329">Remarks</span></span>

<span data-ttu-id="07b6d-330">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-330">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="07b6d-331">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-331">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="07b6d-332">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-332">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="07b6d-333">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-333">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="07b6d-334">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-334">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="07b6d-335">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-335">The maximum value for a single byte is 255.</span></span>

### <a name="method-backstyle"></a><span data-ttu-id="07b6d-336">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="07b6d-336">Method backStyle</span></span>

<span data-ttu-id="07b6d-337">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-337">Determines whether the control background can be transparent.</span></span>

    public int backStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-338">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-338">Parameters</span></span>

<span data-ttu-id="07b6d-339">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-339">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-340">Return Value</span></span>

<span data-ttu-id="07b6d-341">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-341">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="07b6d-342">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="07b6d-342">Method beginDrag</span></span>

<span data-ttu-id="07b6d-343">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-343">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-344">Parameters</span></span>

<span data-ttu-id="07b6d-345">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-345">x</span></span>  
<span data-ttu-id="07b6d-346">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-346">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="07b6d-347">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-347">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="07b6d-348">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-348">y</span></span>  
<span data-ttu-id="07b6d-349">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-349">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="07b6d-350">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-350">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-351">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-351">Return Value</span></span>

<span data-ttu-id="07b6d-352">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-352">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-353">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-353">Remarks</span></span>

<span data-ttu-id="07b6d-354">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-354">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="07b6d-355">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-355">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-bold"></a><span data-ttu-id="07b6d-356">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="07b6d-356">Method bold</span></span>

<span data-ttu-id="07b6d-357">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-357">Gets or sets the weight of font used to output text in the control.</span></span>

    public int bold([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-358">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-358">Parameters</span></span>

<span data-ttu-id="07b6d-359">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-359">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-360">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-360">Return Value</span></span>

<span data-ttu-id="07b6d-361">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-361">An integer value between zero and nine, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-362">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-362">Remarks</span></span>

<span data-ttu-id="07b6d-363">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-363">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="07b6d-364">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-364">0 Use the default font weight.</span></span>
-   <span data-ttu-id="07b6d-365">1 シン。</span><span class="sxs-lookup"><span data-stu-id="07b6d-365">1 Thin.</span></span>
-   <span data-ttu-id="07b6d-366">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-366">2 Extra-light.</span></span>
-   <span data-ttu-id="07b6d-367">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-367">3 Light.</span></span>
-   <span data-ttu-id="07b6d-368">4 標準。</span><span class="sxs-lookup"><span data-stu-id="07b6d-368">4 Normal.</span></span>
-   <span data-ttu-id="07b6d-369">5 中。</span><span class="sxs-lookup"><span data-stu-id="07b6d-369">5 Medium.</span></span>
-   <span data-ttu-id="07b6d-370">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="07b6d-370">6 Semibold.</span></span>
-   <span data-ttu-id="07b6d-371">7 太字。</span><span class="sxs-lookup"><span data-stu-id="07b6d-371">7 Bold.</span></span>
-   <span data-ttu-id="07b6d-372">8 極太。</span><span class="sxs-lookup"><span data-stu-id="07b6d-372">8 Extra-bold.</span></span>
-   <span data-ttu-id="07b6d-373">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-373">9 Heavy.</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="07b6d-374">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-374">Method calcControlSize</span></span>

<span data-ttu-id="07b6d-375">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-375">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="07b6d-376">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-376">Parameters</span></span>

<span data-ttu-id="07b6d-377">chars</span><span class="sxs-lookup"><span data-stu-id="07b6d-377">chars</span></span>  
<span data-ttu-id="07b6d-378">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-378">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="07b6d-379">明細行</span><span class="sxs-lookup"><span data-stu-id="07b6d-379">lines</span></span>  
<span data-ttu-id="07b6d-380">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-380">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-381">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-381">Return Value</span></span>

<span data-ttu-id="07b6d-382">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-382">The container that holds the width and height.</span></span>

### <a name="method-characterset"></a><span data-ttu-id="07b6d-383">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="07b6d-383">Method characterSet</span></span>

<span data-ttu-id="07b6d-384">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-384">Gets or sets the character set of the font.</span></span>

    public int characterSet([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-385">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-385">Parameters</span></span>

<span data-ttu-id="07b6d-386">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-386">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-387">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-387">Return Value</span></span>

<span data-ttu-id="07b6d-388">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-388">An integer value that indicates the character set of the font.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-389">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-389">Remarks</span></span>

<span data-ttu-id="07b6d-390">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-390">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="07b6d-391">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-391">Value.</span></span> | <span data-ttu-id="07b6d-392">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-392">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="07b6d-393">0</span><span class="sxs-lookup"><span data-stu-id="07b6d-393">0</span></span>      | <span data-ttu-id="07b6d-394">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-394">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="07b6d-395">1</span><span class="sxs-lookup"><span data-stu-id="07b6d-395">1</span></span>      | <span data-ttu-id="07b6d-396">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-396">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="07b6d-397">2</span><span class="sxs-lookup"><span data-stu-id="07b6d-397">2</span></span>      | <span data-ttu-id="07b6d-398">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-398">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="07b6d-399">77</span><span class="sxs-lookup"><span data-stu-id="07b6d-399">77</span></span>     | <span data-ttu-id="07b6d-400">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-400">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="07b6d-401">128</span><span class="sxs-lookup"><span data-stu-id="07b6d-401">128</span></span>    | <span data-ttu-id="07b6d-402">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-402">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="07b6d-403">129</span><span class="sxs-lookup"><span data-stu-id="07b6d-403">129</span></span>    | <span data-ttu-id="07b6d-404">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-404">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="07b6d-405">134</span><span class="sxs-lookup"><span data-stu-id="07b6d-405">134</span></span>    | <span data-ttu-id="07b6d-406">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-406">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="07b6d-407">136</span><span class="sxs-lookup"><span data-stu-id="07b6d-407">136</span></span>    | <span data-ttu-id="07b6d-408">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-408">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="07b6d-409">161</span><span class="sxs-lookup"><span data-stu-id="07b6d-409">161</span></span>    | <span data-ttu-id="07b6d-410">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-410">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="07b6d-411">162</span><span class="sxs-lookup"><span data-stu-id="07b6d-411">162</span></span>    | <span data-ttu-id="07b6d-412">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-412">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="07b6d-413">163</span><span class="sxs-lookup"><span data-stu-id="07b6d-413">163</span></span>    | <span data-ttu-id="07b6d-414">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-414">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="07b6d-415">186</span><span class="sxs-lookup"><span data-stu-id="07b6d-415">186</span></span>    | <span data-ttu-id="07b6d-416">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-416">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="07b6d-417">204</span><span class="sxs-lookup"><span data-stu-id="07b6d-417">204</span></span>    | <span data-ttu-id="07b6d-418">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-418">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="07b6d-419">238</span><span class="sxs-lookup"><span data-stu-id="07b6d-419">238</span></span>    | <span data-ttu-id="07b6d-420">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-420">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="07b6d-421">255</span><span class="sxs-lookup"><span data-stu-id="07b6d-421">255</span></span>    | <span data-ttu-id="07b6d-422">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-422">OEM\_CHARSET</span></span>         |

<span data-ttu-id="07b6d-423">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-423">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="07b6d-424">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-424">Value.</span></span> | <span data-ttu-id="07b6d-425">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-425">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="07b6d-426">130</span><span class="sxs-lookup"><span data-stu-id="07b6d-426">130</span></span>    | <span data-ttu-id="07b6d-427">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-427">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="07b6d-428">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-428">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="07b6d-429">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-429">Value.</span></span> | <span data-ttu-id="07b6d-430">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-430">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="07b6d-431">177</span><span class="sxs-lookup"><span data-stu-id="07b6d-431">177</span></span>    | <span data-ttu-id="07b6d-432">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-432">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="07b6d-433">178</span><span class="sxs-lookup"><span data-stu-id="07b6d-433">178</span></span>    | <span data-ttu-id="07b6d-434">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-434">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="07b6d-435">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-435">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="07b6d-436">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-436">Value.</span></span> | <span data-ttu-id="07b6d-437">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-437">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="07b6d-438">222</span><span class="sxs-lookup"><span data-stu-id="07b6d-438">222</span></span>    | <span data-ttu-id="07b6d-439">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-439">THAI\_CHARSET</span></span> |

<span data-ttu-id="07b6d-440">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-440">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="07b6d-441">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-441">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="07b6d-442">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b6d-442">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

### <a name="method-colorscheme"></a><span data-ttu-id="07b6d-443">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="07b6d-443">Method colorScheme</span></span>

<span data-ttu-id="07b6d-444">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-444">Gets or sets the color scheme of the control.</span></span>

    public int colorScheme([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-445">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-445">Parameters</span></span>

<span data-ttu-id="07b6d-446">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-446">value</span></span>  
<span data-ttu-id="07b6d-447">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-447">The value to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-448">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-448">Return Value</span></span>

<span data-ttu-id="07b6d-449">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-449">An integer between zero and two, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-450">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-450">Remarks</span></span>

<span data-ttu-id="07b6d-451">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-451">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="07b6d-452">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-452">Value.</span></span> | <span data-ttu-id="07b6d-453">スタイル。</span><span class="sxs-lookup"><span data-stu-id="07b6d-453">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="07b6d-454">0</span><span class="sxs-lookup"><span data-stu-id="07b6d-454">0</span></span>      | <span data-ttu-id="07b6d-455">既定。</span><span class="sxs-lookup"><span data-stu-id="07b6d-455">Default.</span></span>               |
| <span data-ttu-id="07b6d-456">1</span><span class="sxs-lookup"><span data-stu-id="07b6d-456">1</span></span>      | <span data-ttu-id="07b6d-457">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="07b6d-457">The Windows palette.</span></span>   |
| <span data-ttu-id="07b6d-458">2</span><span class="sxs-lookup"><span data-stu-id="07b6d-458">2</span></span>      | <span data-ttu-id="07b6d-459">真の配色。</span><span class="sxs-lookup"><span data-stu-id="07b6d-459">The true-color scheme.</span></span> |

### <a name="method-configurationkey"></a><span data-ttu-id="07b6d-460">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="07b6d-460">Method configurationKey</span></span>

<span data-ttu-id="07b6d-461">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-461">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-462">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-462">Parameters</span></span>

<span data-ttu-id="07b6d-463">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-463">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-464">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-464">Return Value</span></span>

<span data-ttu-id="07b6d-465">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-465">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-466">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-466">Remarks</span></span>

<span data-ttu-id="07b6d-467">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-467">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="07b6d-468">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-468">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="07b6d-469">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-469">Method configurationKeyEx</span></span>

<span data-ttu-id="07b6d-470">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-470">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="07b6d-471">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-471">Return Value</span></span>

<span data-ttu-id="07b6d-472">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="07b6d-472">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-473">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-473">Remarks</span></span>

<span data-ttu-id="07b6d-474">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-474">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="07b6d-475">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-475">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="07b6d-476">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-476">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="07b6d-477">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="07b6d-477">Method countryRegionCodes</span></span>

<span data-ttu-id="07b6d-478">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-478">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-479">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-479">Parameters</span></span>

<span data-ttu-id="07b6d-480">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-480">value</span></span>  
<span data-ttu-id="07b6d-481">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-481">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-482">Return Value</span></span>

<span data-ttu-id="07b6d-483">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-483">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="07b6d-484">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="07b6d-484">Method dataRelationPath</span></span>

<span data-ttu-id="07b6d-485">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-485">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-486">Parameters</span></span>

<span data-ttu-id="07b6d-487">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-487">value</span></span>  
<span data-ttu-id="07b6d-488">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-488">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-489">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-489">Return Value</span></span>

<span data-ttu-id="07b6d-490">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="07b6d-490">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-491">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-491">Remarks</span></span>

<span data-ttu-id="07b6d-492">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-492">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="07b6d-493">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="07b6d-493">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="07b6d-494">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="07b6d-494">Method displayTarget</span></span>

<span data-ttu-id="07b6d-495">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-495">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, Finance and Operations, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-496">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-496">Parameters</span></span>

<span data-ttu-id="07b6d-497">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-497">value</span></span>  
<span data-ttu-id="07b6d-498">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-498">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-499">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-499">Return Value</span></span>

<span data-ttu-id="07b6d-500">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-500">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="07b6d-501">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="07b6d-501">Method dragDrop</span></span>

<span data-ttu-id="07b6d-502">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-502">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-503">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-503">Parameters</span></span>

<span data-ttu-id="07b6d-504">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-504">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-505">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-505">Return Value</span></span>

<span data-ttu-id="07b6d-506">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-506">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="07b6d-507">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="07b6d-507">Method dragOver</span></span>

<span data-ttu-id="07b6d-508">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-508">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-509">Parameters</span></span>

<span data-ttu-id="07b6d-510">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-510">dragSource</span></span>  
<span data-ttu-id="07b6d-511">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-511">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-512">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-512">dragMode</span></span>  
<span data-ttu-id="07b6d-513">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-513">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-514">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-514">x</span></span>  
<span data-ttu-id="07b6d-515">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-515">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-516">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-516">y</span></span>  
<span data-ttu-id="07b6d-517">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-517">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-518">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-518">Return Value</span></span>

<span data-ttu-id="07b6d-519">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-519">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="07b6d-520">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-520">Method dragOverEx</span></span>

<span data-ttu-id="07b6d-521">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-521">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-522">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-522">Parameters</span></span>

<span data-ttu-id="07b6d-523">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-523">dragSource</span></span>  
<span data-ttu-id="07b6d-524">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-524">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-525">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-525">dragMode</span></span>  
<span data-ttu-id="07b6d-526">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-526">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-527">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-527">x</span></span>  
<span data-ttu-id="07b6d-528">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-528">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-529">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-529">y</span></span>  
<span data-ttu-id="07b6d-530">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-530">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-531">Return Value</span></span>

<span data-ttu-id="07b6d-532">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-532">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="07b6d-533">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="07b6d-533">Method dragText</span></span>

<span data-ttu-id="07b6d-534">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-534">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="07b6d-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-535">Return Value</span></span>

<span data-ttu-id="07b6d-536">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-536">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="07b6d-537">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="07b6d-537">Method enabled</span></span>

<span data-ttu-id="07b6d-538">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-538">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-539">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-539">Parameters</span></span>

<span data-ttu-id="07b6d-540">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-540">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-541">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-541">Return Value</span></span>

<span data-ttu-id="07b6d-542">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-542">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-543">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-543">Remarks</span></span>

<span data-ttu-id="07b6d-544">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-544">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="07b6d-545">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-545">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="07b6d-546">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-546">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-font"></a><span data-ttu-id="07b6d-547">メソッド font</span><span class="sxs-lookup"><span data-stu-id="07b6d-547">Method font</span></span>

<span data-ttu-id="07b6d-548">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-548">Gets or sets the name of the font for the control to use.</span></span>

    public str font([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-549">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-549">Parameters</span></span>

<span data-ttu-id="07b6d-550">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-550">value</span></span>  
<span data-ttu-id="07b6d-551">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-551">The value to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-552">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-552">Return Value</span></span>

<span data-ttu-id="07b6d-553">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-553">The name of the font to use, such as Tahoma or Verdana.</span></span>

### <a name="method-fontsize"></a><span data-ttu-id="07b6d-554">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-554">Method fontSize</span></span>

<span data-ttu-id="07b6d-555">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-555">Gets or sets the size of the font for the control to use.</span></span>

    public int fontSize([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-556">Parameters</span></span>

<span data-ttu-id="07b6d-557">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-557">value</span></span>  
<span data-ttu-id="07b6d-558">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-558">The value to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-559">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-559">Return Value</span></span>

<span data-ttu-id="07b6d-560">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-560">The height of the font in points.</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="07b6d-561">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="07b6d-561">Method hasChanged</span></span>

<span data-ttu-id="07b6d-562">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-562">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="07b6d-563">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-563">Parameters</span></span>

<span data-ttu-id="07b6d-564">val</span><span class="sxs-lookup"><span data-stu-id="07b6d-564">val</span></span>  
<span data-ttu-id="07b6d-565">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-565">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-566">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-566">Return Value</span></span>

<span data-ttu-id="07b6d-567">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-567">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="07b6d-568">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="07b6d-568">Method hasUserSetting</span></span>

<span data-ttu-id="07b6d-569">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-569">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="07b6d-570">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-570">Return Value</span></span>

<span data-ttu-id="07b6d-571">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-571">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="07b6d-572">メソッド height</span><span class="sxs-lookup"><span data-stu-id="07b6d-572">Method height</span></span>

<span data-ttu-id="07b6d-573">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-573">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-574">Parameters</span></span>

<span data-ttu-id="07b6d-575">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-575">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-576">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-576">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-577">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-577">Return Value</span></span>

<span data-ttu-id="07b6d-578">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-578">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-579">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-579">Remarks</span></span>

<span data-ttu-id="07b6d-580">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-580">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="07b6d-581">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-581">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="07b6d-582">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-582">Mode.</span></span>            | <span data-ttu-id="07b6d-583">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-583">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-584">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-584">-1 Exact.</span></span>        | <span data-ttu-id="07b6d-585">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-585">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-586">0 自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-586">0 Auto.</span></span>          | <span data-ttu-id="07b6d-587">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-587">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-588">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-588">1 Column height.</span></span> | <span data-ttu-id="07b6d-589">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-589">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="07b6d-590">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-590">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="07b6d-591">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-591">Method heightMode</span></span>

<span data-ttu-id="07b6d-592">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-592">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-593">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-593">Parameters</span></span>

<span data-ttu-id="07b6d-594">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-594">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-595">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-595">Return Value</span></span>

<span data-ttu-id="07b6d-596">計算モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-596">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-597">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-597">Remarks</span></span>

<span data-ttu-id="07b6d-598">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-598">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="07b6d-599">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-599">Mode.</span></span>          | <span data-ttu-id="07b6d-600">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-600">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-601">正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-601">Exact.</span></span>         | <span data-ttu-id="07b6d-602">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-602">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-603">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-603">Auto.</span></span>          | <span data-ttu-id="07b6d-604">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-604">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-605">列の高さ</span><span class="sxs-lookup"><span data-stu-id="07b6d-605">Column height.</span></span> | <span data-ttu-id="07b6d-606">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-606">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="07b6d-607">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-607">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="07b6d-608">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-608">Method heightValue</span></span>

<span data-ttu-id="07b6d-609">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-609">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-610">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-610">Parameters</span></span>

<span data-ttu-id="07b6d-611">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-611">value</span></span>  
<span data-ttu-id="07b6d-612">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-612">The value to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-613">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-613">Return Value</span></span>

<span data-ttu-id="07b6d-614">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-614">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-615">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-615">Remarks</span></span>

<span data-ttu-id="07b6d-616">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-616">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="07b6d-617">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="07b6d-617">Method helpField</span></span>

<span data-ttu-id="07b6d-618">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-618">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="07b6d-619">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-619">Return Value</span></span>

<span data-ttu-id="07b6d-620">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-620">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-621">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-621">Remarks</span></span>

<span data-ttu-id="07b6d-622">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-622">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="07b6d-623">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-623">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="07b6d-624">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="07b6d-624">Method helpText</span></span>

<span data-ttu-id="07b6d-625">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-625">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-626">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-626">Parameters</span></span>

<span data-ttu-id="07b6d-627">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-627">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-628">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-628">Return Value</span></span>

<span data-ttu-id="07b6d-629">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-629">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-630">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-630">Remarks</span></span>

<span data-ttu-id="07b6d-631">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-631">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="07b6d-632">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-632">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="07b6d-633">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="07b6d-633">Method hierarchyParent</span></span>

<span data-ttu-id="07b6d-634">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-634">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-635">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-635">Parameters</span></span>

<span data-ttu-id="07b6d-636">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-636">value</span></span>  
<span data-ttu-id="07b6d-637">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-637">The value to assign the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-638">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-638">Return Value</span></span>

<span data-ttu-id="07b6d-639">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-639">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="07b6d-640">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="07b6d-640">Method hWnd</span></span>

<span data-ttu-id="07b6d-641">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-641">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="07b6d-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-642">Return Value</span></span>

<span data-ttu-id="07b6d-643">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-643">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-644">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-644">Remarks</span></span>

<span data-ttu-id="07b6d-645">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-645">The handle can be used with the Windows API.</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="07b6d-646">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="07b6d-646">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="07b6d-647">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-647">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="07b6d-648">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="07b6d-648">Method isDisplayed</span></span>

<span data-ttu-id="07b6d-649">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-649">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="07b6d-650">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-650">Return Value</span></span>

<span data-ttu-id="07b6d-651">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-651">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-652">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-652">Remarks</span></span>

<span data-ttu-id="07b6d-653">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-653">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="07b6d-654">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="07b6d-654">Method isRestricted</span></span>

<span data-ttu-id="07b6d-655">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-655">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="07b6d-656">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-656">Return Value</span></span>

<span data-ttu-id="07b6d-657">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-657">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="07b6d-658">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="07b6d-658">Method isUserSetupEnabled</span></span>

<span data-ttu-id="07b6d-659">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-659">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="07b6d-660">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-660">Parameters</span></span>

<span data-ttu-id="07b6d-661">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="07b6d-661">neededSetupRights</span></span>  
<span data-ttu-id="07b6d-662">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-662">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-663">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-663">Return Value</span></span>

<span data-ttu-id="07b6d-664">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-664">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-665">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-665">Remarks</span></span>

<span data-ttu-id="07b6d-666">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-666">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-667">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="07b6d-667">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="07b6d-668">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-668">No changes can be made to the control.</span></span> <span data-ttu-id="07b6d-669">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-669">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="07b6d-670">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="07b6d-670">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="07b6d-671">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-671">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="07b6d-672">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-672">The user cannot move the control.</span></span>   |
| <span data-ttu-id="07b6d-673">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="07b6d-673">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="07b6d-674">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-674">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="07b6d-675">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-675">The user can also move the control.</span></span> |

<span data-ttu-id="07b6d-676">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-676">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="method-italic"></a><span data-ttu-id="07b6d-677">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="07b6d-677">Method italic</span></span>

    public boolean italic([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-678">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-678">Parameters</span></span>

<span data-ttu-id="07b6d-679">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-679">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-680">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-680">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="07b6d-681">メソッド left</span><span class="sxs-lookup"><span data-stu-id="07b6d-681">Method left</span></span>

<span data-ttu-id="07b6d-682">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-682">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-683">Parameters</span></span>

<span data-ttu-id="07b6d-684">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-684">value</span></span>  
<span data-ttu-id="07b6d-685">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-685">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-686">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-686">mode</span></span>  
<span data-ttu-id="07b6d-687">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-687">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-688">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-688">Return Value</span></span>

<span data-ttu-id="07b6d-689">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-689">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="07b6d-690">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-690">Method leftMode</span></span>

<span data-ttu-id="07b6d-691">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-691">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-692">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-692">Parameters</span></span>

<span data-ttu-id="07b6d-693">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-693">value</span></span>  
<span data-ttu-id="07b6d-694">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-694">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-695">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-695">Return Value</span></span>

<span data-ttu-id="07b6d-696">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-696">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="07b6d-697">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-697">Method leftValue</span></span>

<span data-ttu-id="07b6d-698">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-698">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-699">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-699">Parameters</span></span>

<span data-ttu-id="07b6d-700">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-700">value</span></span>  
<span data-ttu-id="07b6d-701">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-701">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-702">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-702">Return Value</span></span>

<span data-ttu-id="07b6d-703">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-703">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="07b6d-704">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="07b6d-704">Method markAsUserAdd</span></span>

<span data-ttu-id="07b6d-705">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-705">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-706">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-706">Parameters</span></span>

<span data-ttu-id="07b6d-707">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-707">value</span></span>  
<span data-ttu-id="07b6d-708">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-708">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-709">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-709">Return Value</span></span>

<span data-ttu-id="07b6d-710">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-710">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="07b6d-711">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="07b6d-711">Method mouseDblClick</span></span>

<span data-ttu-id="07b6d-712">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-712">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-713">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-713">Parameters</span></span>

<span data-ttu-id="07b6d-714">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-714">x</span></span>  
<span data-ttu-id="07b6d-715">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-715">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-716">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-716">y</span></span>  
<span data-ttu-id="07b6d-717">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-717">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-718">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-718">button</span></span>  
<span data-ttu-id="07b6d-719">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-719">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-720">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-720">Ctrl</span></span>  
<span data-ttu-id="07b6d-721">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-721">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-722">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-722">Shift</span></span>  
<span data-ttu-id="07b6d-723">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-723">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-724">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-724">Return Value</span></span>

<span data-ttu-id="07b6d-725">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-725">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-726">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-726">Remarks</span></span>

<span data-ttu-id="07b6d-727">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-727">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="07b6d-728">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="07b6d-728">Method mouseDown</span></span>

<span data-ttu-id="07b6d-729">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-729">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-730">Parameters</span></span>

<span data-ttu-id="07b6d-731">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-731">x</span></span>  
<span data-ttu-id="07b6d-732">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-732">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-733">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-733">y</span></span>  
<span data-ttu-id="07b6d-734">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-734">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-735">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-735">button</span></span>  
<span data-ttu-id="07b6d-736">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-736">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-737">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-737">Ctrl</span></span>  
<span data-ttu-id="07b6d-738">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-738">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-739">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-739">Shift</span></span>  
<span data-ttu-id="07b6d-740">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-740">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-741">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-741">Return Value</span></span>

<span data-ttu-id="07b6d-742">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-742">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-743">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-743">Remarks</span></span>

<span data-ttu-id="07b6d-744">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-744">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="07b6d-745">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-745">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="07b6d-746">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="07b6d-746">Method mouseMove</span></span>

<span data-ttu-id="07b6d-747">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-747">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-748">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-748">Parameters</span></span>

<span data-ttu-id="07b6d-749">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-749">x</span></span>  
<span data-ttu-id="07b6d-750">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-750">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-751">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-751">y</span></span>  
<span data-ttu-id="07b6d-752">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-752">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-753">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-753">button</span></span>  
<span data-ttu-id="07b6d-754">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-754">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-755">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-755">Ctrl</span></span>  
<span data-ttu-id="07b6d-756">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-756">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-757">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-757">Shift</span></span>  
<span data-ttu-id="07b6d-758">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-758">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-759">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-759">Return Value</span></span>

<span data-ttu-id="07b6d-760">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-760">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-761">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-761">Remarks</span></span>

<span data-ttu-id="07b6d-762">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-762">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="07b6d-763">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="07b6d-763">Method mouseUp</span></span>

<span data-ttu-id="07b6d-764">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-764">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-765">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-765">Parameters</span></span>

<span data-ttu-id="07b6d-766">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-766">x</span></span>  
<span data-ttu-id="07b6d-767">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-767">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-768">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-768">y</span></span>  
<span data-ttu-id="07b6d-769">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-769">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-770">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-770">button</span></span>  
<span data-ttu-id="07b6d-771">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-771">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-772">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-772">Ctrl</span></span>  
<span data-ttu-id="07b6d-773">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-773">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-774">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-774">Shift</span></span>  
<span data-ttu-id="07b6d-775">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-775">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-776">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-776">Return Value</span></span>

<span data-ttu-id="07b6d-777">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-777">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-778">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-778">Remarks</span></span>

<span data-ttu-id="07b6d-779">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-779">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="07b6d-780">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-780">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-name"></a><span data-ttu-id="07b6d-781">メソッド名</span><span class="sxs-lookup"><span data-stu-id="07b6d-781">Method name</span></span>

<span data-ttu-id="07b6d-782">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-782">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-783">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-783">Parameters</span></span>

<span data-ttu-id="07b6d-784">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-784">value</span></span>  
<span data-ttu-id="07b6d-785">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-785">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-786">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-786">Return Value</span></span>

<span data-ttu-id="07b6d-787">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-787">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-788">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-788">Remarks</span></span>

<span data-ttu-id="07b6d-789">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-789">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="07b6d-790">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-790">It must begin with a letter.</span></span>
-   <span data-ttu-id="07b6d-791">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-791">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="07b6d-792">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-792">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="07b6d-793">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-793">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="07b6d-794">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-794">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="07b6d-795">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="07b6d-795">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-796">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-796">Parameters</span></span>

<span data-ttu-id="07b6d-797">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-797">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-798">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-798">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="07b6d-799">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="07b6d-799">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="07b6d-800">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-800">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="07b6d-801">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-801">Method parentControl</span></span>

<span data-ttu-id="07b6d-802">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-802">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="07b6d-803">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-803">Return Value</span></span>

<span data-ttu-id="07b6d-804">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="07b6d-804">The parent control for the control.</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="07b6d-805">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="07b6d-805">Method securityKey</span></span>

<span data-ttu-id="07b6d-806">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-806">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-807">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-807">Parameters</span></span>

<span data-ttu-id="07b6d-808">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-808">value</span></span>  
<span data-ttu-id="07b6d-809">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-809">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-810">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-810">Return Value</span></span>

<span data-ttu-id="07b6d-811">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-811">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="07b6d-812">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="07b6d-812">Method showContextMenu</span></span>

<span data-ttu-id="07b6d-813">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-813">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="07b6d-814">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-814">Parameters</span></span>

<span data-ttu-id="07b6d-815">menuHandle</span><span class="sxs-lookup"><span data-stu-id="07b6d-815">menuHandle</span></span>  
<span data-ttu-id="07b6d-816">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-816">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-817">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-817">Return Value</span></span>

<span data-ttu-id="07b6d-818">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-818">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-skip"></a><span data-ttu-id="07b6d-819">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="07b6d-819">Method skip</span></span>

<span data-ttu-id="07b6d-820">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-820">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-821">Parameters</span></span>

<span data-ttu-id="07b6d-822">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-822">value</span></span>  
<span data-ttu-id="07b6d-823">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-823">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-824">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-824">Return Value</span></span>

<span data-ttu-id="07b6d-825">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-825">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-826">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-826">Remarks</span></span>

<span data-ttu-id="07b6d-827">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-827">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="07b6d-828">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="07b6d-828">Method toolTip</span></span>

<span data-ttu-id="07b6d-829">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-829">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="07b6d-830">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-830">Return Value</span></span>

<span data-ttu-id="07b6d-831">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-831">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-832">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-832">Remarks</span></span>

<span data-ttu-id="07b6d-833">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-833">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="07b6d-834">メソッド top</span><span class="sxs-lookup"><span data-stu-id="07b6d-834">Method top</span></span>

<span data-ttu-id="07b6d-835">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-835">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-836">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-836">Parameters</span></span>

<span data-ttu-id="07b6d-837">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-837">value</span></span>  
<span data-ttu-id="07b6d-838">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-838">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-839">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-839">mode</span></span>  
<span data-ttu-id="07b6d-840">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-840">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-841">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-841">Return Value</span></span>

<span data-ttu-id="07b6d-842">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-842">The vertical position of the control in the form.</span></span>

### <a name="method-topmode"></a><span data-ttu-id="07b6d-843">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-843">Method topMode</span></span>

<span data-ttu-id="07b6d-844">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-844">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-845">Parameters</span></span>

<span data-ttu-id="07b6d-846">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-846">value</span></span>  
<span data-ttu-id="07b6d-847">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-847">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-848">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-848">Return Value</span></span>

<span data-ttu-id="07b6d-849">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-849">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="07b6d-850">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-850">Method topValue</span></span>

<span data-ttu-id="07b6d-851">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-851">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-852">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-852">Parameters</span></span>

<span data-ttu-id="07b6d-853">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-853">value</span></span>  
<span data-ttu-id="07b6d-854">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-854">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-855">Return Value</span></span>

<span data-ttu-id="07b6d-856">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-856">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="07b6d-857">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="07b6d-857">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-858">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-858">Parameters</span></span>

<span data-ttu-id="07b6d-859">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-859">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-860">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-860">Return Value</span></span>

### <a name="method-underline"></a><span data-ttu-id="07b6d-861">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="07b6d-861">Method underline</span></span>

    public boolean underline([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-862">Parameters</span></span>

<span data-ttu-id="07b6d-863">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-863">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-864">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-864">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="07b6d-865">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="07b6d-865">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="07b6d-866">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-866">Parameters</span></span>

<span data-ttu-id="07b6d-867">データ</span><span class="sxs-lookup"><span data-stu-id="07b6d-867">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-868">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-868">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="07b6d-869">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="07b6d-869">Method userData</span></span>

<span data-ttu-id="07b6d-870">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-870">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-871">Parameters</span></span>

<span data-ttu-id="07b6d-872">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-872">value</span></span>  
<span data-ttu-id="07b6d-873">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-873">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-874">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-874">Return Value</span></span>

<span data-ttu-id="07b6d-875">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-875">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="07b6d-876">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="07b6d-876">Method userDataItem</span></span>

<span data-ttu-id="07b6d-877">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-877">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-878">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-878">Parameters</span></span>

<span data-ttu-id="07b6d-879">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-879">value</span></span>  
<span data-ttu-id="07b6d-880">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-880">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-881">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-881">Return Value</span></span>

<span data-ttu-id="07b6d-882">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="07b6d-882">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="07b6d-883">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="07b6d-883">Method userDataItems</span></span>

<span data-ttu-id="07b6d-884">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-884">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-885">Parameters</span></span>

<span data-ttu-id="07b6d-886">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-886">value</span></span>  
<span data-ttu-id="07b6d-887">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-887">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-888">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-888">Return Value</span></span>

<span data-ttu-id="07b6d-889">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-889">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="07b6d-890">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="07b6d-890">Method userDisable</span></span>

<span data-ttu-id="07b6d-891">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-891">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-892">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-892">Parameters</span></span>

<span data-ttu-id="07b6d-893">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-893">value</span></span>  
<span data-ttu-id="07b6d-894">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-894">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-895">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-895">Return Value</span></span>

<span data-ttu-id="07b6d-896">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-896">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="07b6d-897">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="07b6d-897">Method userHeight</span></span>

<span data-ttu-id="07b6d-898">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-898">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-899">Parameters</span></span>

<span data-ttu-id="07b6d-900">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-900">value</span></span>  
<span data-ttu-id="07b6d-901">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-901">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-902">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-902">Return Value</span></span>

<span data-ttu-id="07b6d-903">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-903">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="07b6d-904">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="07b6d-904">Method userHide</span></span>

<span data-ttu-id="07b6d-905">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-905">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-906">Parameters</span></span>

<span data-ttu-id="07b6d-907">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-907">value</span></span>  
<span data-ttu-id="07b6d-908">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-908">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-909">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-909">Return Value</span></span>

<span data-ttu-id="07b6d-910">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-910">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-911">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-911">Remarks</span></span>

<span data-ttu-id="07b6d-912">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-912">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="07b6d-913">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-913">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="07b6d-914">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-914">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="07b6d-915">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="07b6d-915">Method userOrgContainer</span></span>

<span data-ttu-id="07b6d-916">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-916">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-917">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-917">Parameters</span></span>

<span data-ttu-id="07b6d-918">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-918">value</span></span>  
<span data-ttu-id="07b6d-919">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-919">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-920">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-920">Return Value</span></span>

<span data-ttu-id="07b6d-921">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-921">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="07b6d-922">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="07b6d-922">Method userOrgSibling</span></span>

<span data-ttu-id="07b6d-923">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-923">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-924">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-924">Parameters</span></span>

<span data-ttu-id="07b6d-925">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-925">value</span></span>  
<span data-ttu-id="07b6d-926">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-926">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-927">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-927">Return Value</span></span>

<span data-ttu-id="07b6d-928">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="07b6d-928">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="07b6d-929">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="07b6d-929">Method userPromptText</span></span>

<span data-ttu-id="07b6d-930">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-930">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-931">Parameters</span></span>

<span data-ttu-id="07b6d-932">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-932">value</span></span>  
<span data-ttu-id="07b6d-933">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-933">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-934">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-934">Return Value</span></span>

<span data-ttu-id="07b6d-935">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-935">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="07b6d-936">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="07b6d-936">Method userSecurityLevel</span></span>

<span data-ttu-id="07b6d-937">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-937">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-938">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-938">Parameters</span></span>

<span data-ttu-id="07b6d-939">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-939">value</span></span>  
<span data-ttu-id="07b6d-940">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-940">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-941">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-941">Return Value</span></span>

<span data-ttu-id="07b6d-942">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="07b6d-942">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="07b6d-943">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="07b6d-943">Method userSkip</span></span>

<span data-ttu-id="07b6d-944">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-944">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-945">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-945">Parameters</span></span>

<span data-ttu-id="07b6d-946">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-946">value</span></span>  
<span data-ttu-id="07b6d-947">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-947">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="07b6d-948">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-948">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-949">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-949">Return Value</span></span>

<span data-ttu-id="07b6d-950">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-950">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="07b6d-951">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="07b6d-951">Method userWidth</span></span>

<span data-ttu-id="07b6d-952">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-952">Sets or returns the width of the control in pixels.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-953">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-953">Parameters</span></span>

<span data-ttu-id="07b6d-954">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-954">value</span></span>  
<span data-ttu-id="07b6d-955">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-955">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-956">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-956">Return Value</span></span>

<span data-ttu-id="07b6d-957">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-957">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-958">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-958">Remarks</span></span>

<span data-ttu-id="07b6d-959">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-959">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="07b6d-960">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-960">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="07b6d-961">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-961">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="07b6d-962">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="07b6d-962">Method verticalSpacing</span></span>

<span data-ttu-id="07b6d-963">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-963">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-964">Parameters</span></span>

<span data-ttu-id="07b6d-965">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-965">value</span></span>  
<span data-ttu-id="07b6d-966">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-966">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-967">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-967">mode</span></span>  
<span data-ttu-id="07b6d-968">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-968">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-969">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-969">Return Value</span></span>

<span data-ttu-id="07b6d-970">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="07b6d-970">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="07b6d-971">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-971">Method verticalSpacingMode</span></span>

<span data-ttu-id="07b6d-972">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-972">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-973">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-973">Parameters</span></span>

<span data-ttu-id="07b6d-974">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-974">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-975">Return Value</span></span>

<span data-ttu-id="07b6d-976">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-976">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="07b6d-977">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-977">Method verticalSpacingValue</span></span>

<span data-ttu-id="07b6d-978">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-978">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-979">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-979">Parameters</span></span>

<span data-ttu-id="07b6d-980">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-980">value</span></span>  
<span data-ttu-id="07b6d-981">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-981">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-982">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-982">Return Value</span></span>

<span data-ttu-id="07b6d-983">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="07b6d-983">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="07b6d-984">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="07b6d-984">Method visible</span></span>

<span data-ttu-id="07b6d-985">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-985">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-986">Parameters</span></span>

<span data-ttu-id="07b6d-987">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-987">value</span></span>  
<span data-ttu-id="07b6d-988">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-988">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-989">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-989">Return Value</span></span>

<span data-ttu-id="07b6d-990">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-990">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="07b6d-991">メソッド width</span><span class="sxs-lookup"><span data-stu-id="07b6d-991">Method width</span></span>

<span data-ttu-id="07b6d-992">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-992">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-993">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-993">Parameters</span></span>

<span data-ttu-id="07b6d-994">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-994">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-995">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-995">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-996">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-996">Return Value</span></span>

<span data-ttu-id="07b6d-997">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-997">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-998">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-998">Remarks</span></span>

<span data-ttu-id="07b6d-999">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-999">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="07b6d-1000">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-1000">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="07b6d-1001">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1001">Mode.</span></span>           | <span data-ttu-id="07b6d-1002">幅計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1002">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-1003">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1003">-1 Exact.</span></span>       | <span data-ttu-id="07b6d-1004">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1004">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-1005">0 自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1005">0 Auto.</span></span>         | <span data-ttu-id="07b6d-1006">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1006">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-1007">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1007">1 Column width.</span></span> | <span data-ttu-id="07b6d-1008">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1008">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="07b6d-1009">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1009">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="07b6d-1010">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1010">Method widthMode</span></span>

<span data-ttu-id="07b6d-1011">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1011">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1012">Parameters</span></span>

<span data-ttu-id="07b6d-1013">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1013">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1014">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1014">Return Value</span></span>

<span data-ttu-id="07b6d-1015">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1015">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1016">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1016">Remarks</span></span>

<span data-ttu-id="07b6d-1017">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-1017">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="07b6d-1018">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1018">Mode.</span></span>         | <span data-ttu-id="07b6d-1019">幅計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1019">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-1020">正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1020">Exact.</span></span>        | <span data-ttu-id="07b6d-1021">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1021">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-1022">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1022">Auto.</span></span>         | <span data-ttu-id="07b6d-1023">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1023">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-1024">列の幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1024">Column width.</span></span> | <span data-ttu-id="07b6d-1025">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1025">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="07b6d-1026">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1026">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="07b6d-1027">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1027">Method widthValue</span></span>

<span data-ttu-id="07b6d-1028">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1028">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1029">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1029">Parameters</span></span>

<span data-ttu-id="07b6d-1030">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1030">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1031">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1031">Return Value</span></span>

<span data-ttu-id="07b6d-1032">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1032">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1033">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1033">Remarks</span></span>

<span data-ttu-id="07b6d-1034">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1034">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-drop"></a><span data-ttu-id="07b6d-1035">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="07b6d-1035">Method drop</span></span>

<span data-ttu-id="07b6d-1036">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1036">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1037">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1037">Parameters</span></span>

<span data-ttu-id="07b6d-1038">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-1038">dragSource</span></span>  
<span data-ttu-id="07b6d-1039">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1039">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1040">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1040">dragMode</span></span>  
<span data-ttu-id="07b6d-1041">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1041">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1042">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1042">x</span></span>  
<span data-ttu-id="07b6d-1043">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1043">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1044">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1044">y</span></span>  
<span data-ttu-id="07b6d-1045">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1045">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-copy"></a><span data-ttu-id="07b6d-1046">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="07b6d-1046">Method copy</span></span>

<span data-ttu-id="07b6d-1047">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1047">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-cut"></a><span data-ttu-id="07b6d-1048">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="07b6d-1048">Method cut</span></span>

<span data-ttu-id="07b6d-1049">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1049">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-setfocus"></a><span data-ttu-id="07b6d-1050">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-1050">Method setFocus</span></span>

<span data-ttu-id="07b6d-1051">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1051">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-mouseleave"></a><span data-ttu-id="07b6d-1052">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="07b6d-1052">Method mouseLeave</span></span>

<span data-ttu-id="07b6d-1053">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1053">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-enddrag"></a><span data-ttu-id="07b6d-1054">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="07b6d-1054">Method endDrag</span></span>

<span data-ttu-id="07b6d-1055">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1055">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="07b6d-1056">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1056">Remarks</span></span>

<span data-ttu-id="07b6d-1057">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1057">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="07b6d-1058">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1058">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-context"></a><span data-ttu-id="07b6d-1059">メソッド context</span><span class="sxs-lookup"><span data-stu-id="07b6d-1059">Method context</span></span>

<span data-ttu-id="07b6d-1060">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1060">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-gotfocus"></a><span data-ttu-id="07b6d-1061">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-1061">Method gotFocus</span></span>

<span data-ttu-id="07b6d-1062">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1062">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-prefcolumnsize"></a><span data-ttu-id="07b6d-1063">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-1063">Method prefColumnSize</span></span>

<span data-ttu-id="07b6d-1064">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1064">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1065">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1065">Parameters</span></span>

<span data-ttu-id="07b6d-1066">width</span><span class="sxs-lookup"><span data-stu-id="07b6d-1066">width</span></span>  
<span data-ttu-id="07b6d-1067">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1067">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1068">height</span><span class="sxs-lookup"><span data-stu-id="07b6d-1068">height</span></span>  
<span data-ttu-id="07b6d-1069">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1069">The preferred height of the control.</span></span>

### <a name="method-lostfocus"></a><span data-ttu-id="07b6d-1070">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-1070">Method lostFocus</span></span>

<span data-ttu-id="07b6d-1071">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1071">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-displaycontrol"></a><span data-ttu-id="07b6d-1072">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1072">Method displayControl</span></span>

<span data-ttu-id="07b6d-1073">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1073">Displays the control.</span></span>

    public void displayControl()

### <a name="method-registeroverridemethod"></a><span data-ttu-id="07b6d-1074">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="07b6d-1074">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1075">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1075">Parameters</span></span>

<span data-ttu-id="07b6d-1076">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="07b6d-1076">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="07b6d-1077">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="07b6d-1077">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="07b6d-1078">overrideObject</span><span class="sxs-lookup"><span data-stu-id="07b6d-1078">overrideObject</span></span>  

### <a name="method-paste"></a><span data-ttu-id="07b6d-1079">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="07b6d-1079">Method paste</span></span>

<span data-ttu-id="07b6d-1080">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1080">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-resetusersetting"></a><span data-ttu-id="07b6d-1081">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="07b6d-1081">Method resetUserSetting</span></span>

<span data-ttu-id="07b6d-1082">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1082">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-dropex"></a><span data-ttu-id="07b6d-1083">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-1083">Method dropEx</span></span>

<span data-ttu-id="07b6d-1084">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1084">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1085">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1085">Parameters</span></span>

<span data-ttu-id="07b6d-1086">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-1086">dragSource</span></span>  
<span data-ttu-id="07b6d-1087">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1087">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1088">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1088">dragMode</span></span>  
<span data-ttu-id="07b6d-1089">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1089">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1090">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1090">x</span></span>  
<span data-ttu-id="07b6d-1091">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1091">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1092">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1092">y</span></span>  
<span data-ttu-id="07b6d-1093">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1093">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-mouseenter"></a><span data-ttu-id="07b6d-1094">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="07b6d-1094">Method mouseEnter</span></span>

<span data-ttu-id="07b6d-1095">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1095">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1096">Parameters</span></span>

<span data-ttu-id="07b6d-1097">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1097">x</span></span>  
<span data-ttu-id="07b6d-1098">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1098">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1099">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1099">y</span></span>  
<span data-ttu-id="07b6d-1100">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1100">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1101">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-1101">button</span></span>  
<span data-ttu-id="07b6d-1102">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1102">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1103">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1103">Ctrl</span></span>  
<span data-ttu-id="07b6d-1104">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1104">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1105">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-1105">Shift</span></span>  
<span data-ttu-id="07b6d-1106">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1106">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-inputsearch"></a><span data-ttu-id="07b6d-1107">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="07b6d-1107">Method inputSearch</span></span>

<span data-ttu-id="07b6d-1108">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1108">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1109">Parameters</span></span>

<span data-ttu-id="07b6d-1110">searchStr</span><span class="sxs-lookup"><span data-stu-id="07b6d-1110">searchStr</span></span>  
<span data-ttu-id="07b6d-1111">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1111">The string value to use to filter data; optional.</span></span>

### <a name="method-dragleave"></a><span data-ttu-id="07b6d-1112">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="07b6d-1112">Method dragLeave</span></span>

<span data-ttu-id="07b6d-1113">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1113">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

## <a name="class-formfilterpanecontrol"></a><span data-ttu-id="07b6d-1114">クラス FormFilterPaneControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1114">Class FormFilterPaneControl</span></span>
    class FormFilterPaneControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="07b6d-1115">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1115">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="07b6d-1116">例</span><span class="sxs-lookup"><span data-stu-id="07b6d-1116">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="07b6d-1117">メソッド</span><span class="sxs-lookup"><span data-stu-id="07b6d-1117">Methods</span></span>

| <span data-ttu-id="07b6d-1118">方法</span><span class="sxs-lookup"><span data-stu-id="07b6d-1118">Method</span></span>                                                                                                      | <span data-ttu-id="07b6d-1119">説明</span><span class="sxs-lookup"><span data-stu-id="07b6d-1119">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-1120">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1120">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1121">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1121">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1122">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1122">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="07b6d-1123">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1123">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-1124">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1124">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="07b6d-1125">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1125">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-1126">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1126">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="07b6d-1127">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1127">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="07b6d-1128">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1128">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1129">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1129">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1130">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1130">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1131">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1131">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1132">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1132">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="07b6d-1133">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1133">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="07b6d-1134">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1134">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="07b6d-1135">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1135">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-1136">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1136">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1137">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1137">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1138">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1138">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1139">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1139">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="07b6d-1140">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1140">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="07b6d-1141">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1141">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="07b6d-1142">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1142">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-1143">public int columns(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1143">public int columns(\[int value\], \[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1144">public AutoMode columnsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1144">public AutoMode columnsMode(\[AutoMode mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1145">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1145">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1146">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1146">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1147">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1147">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1148">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1148">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1149">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1149">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="07b6d-1150">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1150">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-1151">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1151">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="07b6d-1152">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1152">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-1153">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1153">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="07b6d-1154">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1154">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="07b6d-1155">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1155">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1156">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1156">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="07b6d-1157">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1157">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="07b6d-1158">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1158">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="07b6d-1159">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1159">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-1160">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1160">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="07b6d-1161">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1161">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span> |
| <span data-ttu-id="07b6d-1162">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1162">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-1163">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1163">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="07b6d-1164">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1164">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="07b6d-1165">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1165">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="07b6d-1166">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1166">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="07b6d-1167">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1167">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-1168">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1168">public str dragText()</span></span>                                                                                       | <span data-ttu-id="07b6d-1169">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1169">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-1170">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1170">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="07b6d-1171">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1171">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-1172">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1172">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="07b6d-1173">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1173">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="07b6d-1174">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1174">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="07b6d-1175">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1175">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="07b6d-1176">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1176">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="07b6d-1177">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1177">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-1178">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1178">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-1179">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1179">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-1180">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1180">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="07b6d-1181">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1181">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-1182">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1182">public str helpField()</span></span>                                                                                      | <span data-ttu-id="07b6d-1183">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1183">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-1184">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1184">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="07b6d-1185">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1185">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="07b6d-1186">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1186">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1187">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1187">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="07b6d-1188">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1188">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="07b6d-1189">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1189">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="07b6d-1190">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1190">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-1191">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1191">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1192">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1192">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="07b6d-1193">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1193">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="07b6d-1194">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1194">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="07b6d-1195">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1195">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-1196">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1196">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="07b6d-1197">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1197">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="07b6d-1198">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1198">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1199">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1199">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="07b6d-1200">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1200">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="07b6d-1201">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1201">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1202">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1202">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1203">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1203">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1204">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1204">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-1205">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1205">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-1206">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1206">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-1207">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1207">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="07b6d-1208">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1208">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="07b6d-1209">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1209">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="07b6d-1210">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1210">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="07b6d-1211">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1211">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="07b6d-1212">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1212">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="07b6d-1213">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1213">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-1214">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1214">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="07b6d-1215">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1215">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-1216">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1216">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="07b6d-1217">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1217">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="07b6d-1218">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1218">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="07b6d-1219">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1219">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="07b6d-1220">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1220">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1221">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1221">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1222">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1222">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="07b6d-1223">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1223">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-1224">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1224">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1225">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1225">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1226">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1226">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1227">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1227">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="07b6d-1228">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1228">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-1229">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1229">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="07b6d-1230">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1230">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-1231">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1231">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="07b6d-1232">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1232">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="07b6d-1233">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1233">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1234">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1234">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="07b6d-1235">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1235">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-1236">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1236">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="07b6d-1237">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1237">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-1238">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1238">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1239">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1239">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1240">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1240">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1241">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1241">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="07b6d-1242">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1242">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-1243">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1243">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-1244">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1244">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-1245">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1245">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1246">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1246">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1247">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1247">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-1248">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1248">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-1249">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1249">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="07b6d-1250">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1250">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="07b6d-1251">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1251">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="07b6d-1252">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1252">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-1253">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1253">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="07b6d-1254">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1254">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="07b6d-1255">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1255">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-1256">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1256">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="07b6d-1257">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1257">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-1258">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1258">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="07b6d-1259">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1259">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="07b6d-1260">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1260">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="07b6d-1261">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1261">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="07b6d-1262">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1262">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-1263">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1263">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="07b6d-1264">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1264">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="07b6d-1265">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1265">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="07b6d-1266">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1266">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="07b6d-1267">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1267">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-1268">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1268">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="07b6d-1269">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1269">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-1270">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1270">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-1271">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1271">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="07b6d-1272">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1272">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-1273">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1273">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="07b6d-1274">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1274">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-1275">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1275">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="07b6d-1276">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1276">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-1277">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1277">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="07b6d-1278">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1278">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-1279">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1279">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="07b6d-1280">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1280">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="07b6d-1281">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1281">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-1282">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1282">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-1283">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1283">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-1284">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1284">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="07b6d-1285">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1285">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1286">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1286">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="07b6d-1287">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1287">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="07b6d-1288">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1288">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="07b6d-1289">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1289">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="07b6d-1290">public void paste()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1290">public void paste()</span></span>                                                                                         | <span data-ttu-id="07b6d-1291">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1291">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-1292">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1292">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="07b6d-1293">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1293">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="07b6d-1294">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1294">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1295">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1295">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="07b6d-1296">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1296">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-1297">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1297">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="07b6d-1298">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1298">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="07b6d-1299">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1299">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="07b6d-1300">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1300">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-1301">public void enter()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1301">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1302">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1302">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="07b6d-1303">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1303">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="07b6d-1304">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1304">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="07b6d-1305">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1305">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-1306">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1306">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1307">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1307">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1308">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1308">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1309">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1309">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="07b6d-1310">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1310">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="07b6d-1311">public void cut()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1311">public void cut()</span></span>                                                                                           | <span data-ttu-id="07b6d-1312">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1312">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="07b6d-1313">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1313">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1314">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1314">public void displayControl()</span></span>                                                                                | <span data-ttu-id="07b6d-1315">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1315">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="07b6d-1316">public void copy()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1316">public void copy()</span></span>                                                                                          | <span data-ttu-id="07b6d-1317">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1317">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="07b6d-1318">public void context()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1318">public void context()</span></span>                                                                                       | <span data-ttu-id="07b6d-1319">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1319">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-1320">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1320">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="07b6d-1321">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1321">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="07b6d-1322">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="07b6d-1322">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="07b6d-1323">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1323">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="07b6d-1324">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-1324">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-1325">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="07b6d-1325">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="07b6d-1326">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1326">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |

### <a name="method-alignchild"></a><span data-ttu-id="07b6d-1327">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="07b6d-1327">Method alignChild</span></span>

    public boolean alignChild([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1328">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1328">Parameters</span></span>

<span data-ttu-id="07b6d-1329">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1329">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1330">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1330">Return Value</span></span>

### <a name="method-alignchildren"></a><span data-ttu-id="07b6d-1331">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="07b6d-1331">Method alignChildren</span></span>

    public boolean alignChildren([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1332">Parameters</span></span>

<span data-ttu-id="07b6d-1333">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1333">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1334">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1334">Return Value</span></span>

### <a name="method-aligncontrol"></a><span data-ttu-id="07b6d-1335">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1335">Method alignControl</span></span>

<span data-ttu-id="07b6d-1336">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1336">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1337">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1337">Parameters</span></span>

<span data-ttu-id="07b6d-1338">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1338">value</span></span>  
<span data-ttu-id="07b6d-1339">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1339">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1340">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1340">Return Value</span></span>

<span data-ttu-id="07b6d-1341">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1341">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1342">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1342">Remarks</span></span>

<span data-ttu-id="07b6d-1343">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1343">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="07b6d-1344">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="07b6d-1344">Method allowEdit</span></span>

<span data-ttu-id="07b6d-1345">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1345">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1346">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1346">Parameters</span></span>

<span data-ttu-id="07b6d-1347">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1347">value</span></span>  
<span data-ttu-id="07b6d-1348">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1348">The value to assign to the allowEdit property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1349">Return Value</span></span>

<span data-ttu-id="07b6d-1350">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1350">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1351">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1351">Remarks</span></span>

<span data-ttu-id="07b6d-1352">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1352">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="07b6d-1353">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="07b6d-1353">Method allowSysSetup</span></span>

<span data-ttu-id="07b6d-1354">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1354">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1355">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1355">Return Value</span></span>

<span data-ttu-id="07b6d-1356">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1356">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-allowusersetup"></a><span data-ttu-id="07b6d-1357">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="07b6d-1357">Method allowUserSetup</span></span>

    public int allowUserSetup([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1358">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1358">Parameters</span></span>

<span data-ttu-id="07b6d-1359">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1359">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1360">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1360">Return Value</span></span>

### <a name="method-arrangeguide"></a><span data-ttu-id="07b6d-1361">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="07b6d-1361">Method arrangeGuide</span></span>

    public int arrangeGuide([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1362">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1362">Parameters</span></span>

<span data-ttu-id="07b6d-1363">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1363">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1364">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1364">Return Value</span></span>

### <a name="method-arrangemethod"></a><span data-ttu-id="07b6d-1365">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="07b6d-1365">Method arrangeMethod</span></span>

    public int arrangeMethod([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1366">Parameters</span></span>

<span data-ttu-id="07b6d-1367">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1368">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1368">Return Value</span></span>

### <a name="method-arrangewhen"></a><span data-ttu-id="07b6d-1369">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="07b6d-1369">Method arrangeWhen</span></span>

    public int arrangeWhen([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1370">Parameters</span></span>

<span data-ttu-id="07b6d-1371">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1371">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1372">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1372">Return Value</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="07b6d-1373">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="07b6d-1373">Method autoDeclaration</span></span>

<span data-ttu-id="07b6d-1374">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1374">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1375">Parameters</span></span>

<span data-ttu-id="07b6d-1376">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1376">value</span></span>  
<span data-ttu-id="07b6d-1377">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1377">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1378">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1378">Return Value</span></span>

<span data-ttu-id="07b6d-1379">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1379">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1380">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1380">Remarks</span></span>

<span data-ttu-id="07b6d-1381">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1381">Controls cannot have identical names.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="07b6d-1382">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="07b6d-1382">Method beginDrag</span></span>

<span data-ttu-id="07b6d-1383">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1383">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1384">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1384">Parameters</span></span>

<span data-ttu-id="07b6d-1385">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1385">x</span></span>  
<span data-ttu-id="07b6d-1386">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1386">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="07b6d-1387">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1387">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1388">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1388">y</span></span>  
<span data-ttu-id="07b6d-1389">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1389">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="07b6d-1390">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1390">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1391">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1391">Return Value</span></span>

<span data-ttu-id="07b6d-1392">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1392">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1393">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1393">Remarks</span></span>

<span data-ttu-id="07b6d-1394">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1394">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="07b6d-1395">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1395">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-bottommargin"></a><span data-ttu-id="07b6d-1396">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="07b6d-1396">Method bottomMargin</span></span>

    public int bottomMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1397">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1397">Parameters</span></span>

<span data-ttu-id="07b6d-1398">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1398">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-1399">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1399">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1400">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1400">Return Value</span></span>

### <a name="method-bottommarginmode"></a><span data-ttu-id="07b6d-1401">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1401">Method bottomMarginMode</span></span>

    public AutoMode bottomMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1402">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1402">Parameters</span></span>

<span data-ttu-id="07b6d-1403">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1403">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1404">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1404">Return Value</span></span>

### <a name="method-bottommarginvalue"></a><span data-ttu-id="07b6d-1405">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1405">Method bottomMarginValue</span></span>

    public int bottomMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1406">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1406">Parameters</span></span>

<span data-ttu-id="07b6d-1407">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1407">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1408">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1408">Return Value</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="07b6d-1409">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-1409">Method calcControlSize</span></span>

<span data-ttu-id="07b6d-1410">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1410">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1411">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1411">Parameters</span></span>

<span data-ttu-id="07b6d-1412">chars</span><span class="sxs-lookup"><span data-stu-id="07b6d-1412">chars</span></span>  
<span data-ttu-id="07b6d-1413">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1413">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1414">明細行</span><span class="sxs-lookup"><span data-stu-id="07b6d-1414">lines</span></span>  
<span data-ttu-id="07b6d-1415">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1415">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1416">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1416">Return Value</span></span>

<span data-ttu-id="07b6d-1417">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1417">The container that holds the width and height.</span></span>

### <a name="method-caption"></a><span data-ttu-id="07b6d-1418">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="07b6d-1418">Method caption</span></span>

<span data-ttu-id="07b6d-1419">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1419">Gets or set the caption of the control.</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1420">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1420">Parameters</span></span>

<span data-ttu-id="07b6d-1421">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1421">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1422">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1422">Return Value</span></span>

<span data-ttu-id="07b6d-1423">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1423">The string that is used as the caption of the control.</span></span>

### <a name="method-columns"></a><span data-ttu-id="07b6d-1424">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="07b6d-1424">Method columns</span></span>

    public int columns([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1425">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1425">Parameters</span></span>

<span data-ttu-id="07b6d-1426">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1426">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-1427">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1427">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1428">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1428">Return Value</span></span>

### <a name="method-columnsmode"></a><span data-ttu-id="07b6d-1429">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1429">Method columnsMode</span></span>

    public AutoMode columnsMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1430">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1430">Parameters</span></span>

<span data-ttu-id="07b6d-1431">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1431">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1432">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1432">Return Value</span></span>

### <a name="method-columnspace"></a><span data-ttu-id="07b6d-1433">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="07b6d-1433">Method columnspace</span></span>

    public int columnspace([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1434">Parameters</span></span>

<span data-ttu-id="07b6d-1435">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1435">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-1436">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1436">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1437">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1437">Return Value</span></span>

### <a name="method-columnspacemode"></a><span data-ttu-id="07b6d-1438">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1438">Method columnspaceMode</span></span>

    public AutoMode columnspaceMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1439">Parameters</span></span>

<span data-ttu-id="07b6d-1440">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1440">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1441">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1441">Return Value</span></span>

### <a name="method-columnspacevalue"></a><span data-ttu-id="07b6d-1442">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1442">Method columnspaceValue</span></span>

    public int columnspaceValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1443">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1443">Parameters</span></span>

<span data-ttu-id="07b6d-1444">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1444">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1445">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1445">Return Value</span></span>

### <a name="method-columnsvalue"></a><span data-ttu-id="07b6d-1446">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1446">Method columnsValue</span></span>

    public int columnsValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1447">Parameters</span></span>

<span data-ttu-id="07b6d-1448">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1448">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1449">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1449">Return Value</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="07b6d-1450">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="07b6d-1450">Method configurationKey</span></span>

<span data-ttu-id="07b6d-1451">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1451">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1452">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1452">Parameters</span></span>

<span data-ttu-id="07b6d-1453">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1453">value</span></span>  
<span data-ttu-id="07b6d-1454">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1454">The ID of the configuration key being assigned to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1455">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1455">Return Value</span></span>

<span data-ttu-id="07b6d-1456">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1456">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1457">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1457">Remarks</span></span>

<span data-ttu-id="07b6d-1458">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1458">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="07b6d-1459">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1459">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="07b6d-1460">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-1460">Method configurationKeyEx</span></span>

<span data-ttu-id="07b6d-1461">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1461">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1462">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1462">Return Value</span></span>

<span data-ttu-id="07b6d-1463">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1463">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1464">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1464">Remarks</span></span>

<span data-ttu-id="07b6d-1465">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1465">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="07b6d-1466">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1466">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="07b6d-1467">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1467">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="07b6d-1468">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="07b6d-1468">Method countryRegionCodes</span></span>

<span data-ttu-id="07b6d-1469">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1469">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1470">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1470">Parameters</span></span>

<span data-ttu-id="07b6d-1471">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1471">value</span></span>  
<span data-ttu-id="07b6d-1472">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1472">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1473">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1473">Return Value</span></span>

<span data-ttu-id="07b6d-1474">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1474">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-countryregioncontextfield"></a><span data-ttu-id="07b6d-1475">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="07b6d-1475">Method countryRegionContextField</span></span>

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1476">Parameters</span></span>

<span data-ttu-id="07b6d-1477">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1477">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1478">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1478">Return Value</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="07b6d-1479">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="07b6d-1479">Method dataRelationPath</span></span>

<span data-ttu-id="07b6d-1480">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1480">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1481">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1481">Parameters</span></span>

<span data-ttu-id="07b6d-1482">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1482">value</span></span>  
<span data-ttu-id="07b6d-1483">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1483">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1484">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1484">Return Value</span></span>

<span data-ttu-id="07b6d-1485">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1485">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1486">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1486">Remarks</span></span>

<span data-ttu-id="07b6d-1487">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1487">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="07b6d-1488">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1488">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-datasource"></a><span data-ttu-id="07b6d-1489">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-1489">Method dataSource</span></span>

<span data-ttu-id="07b6d-1490">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1490">Gets or sets a data source to be used by the control or the form.</span></span>

    public int dataSource([AnyType value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1491">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1491">Parameters</span></span>

<span data-ttu-id="07b6d-1492">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1492">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1493">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1493">Return Value</span></span>

<span data-ttu-id="07b6d-1494">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1494">The identifier of the data source to be used.</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="07b6d-1495">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="07b6d-1495">Method displayTarget</span></span>

<span data-ttu-id="07b6d-1496">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1496">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1497">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1497">Parameters</span></span>

<span data-ttu-id="07b6d-1498">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1498">value</span></span>  
<span data-ttu-id="07b6d-1499">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1499">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1500">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1500">Return Value</span></span>

<span data-ttu-id="07b6d-1501">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1501">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="07b6d-1502">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="07b6d-1502">Method dragDrop</span></span>

<span data-ttu-id="07b6d-1503">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1503">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1504">Parameters</span></span>

<span data-ttu-id="07b6d-1505">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1505">value</span></span>  
<span data-ttu-id="07b6d-1506">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1506">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1507">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1507">Return Value</span></span>

<span data-ttu-id="07b6d-1508">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1508">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1509">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1509">Remarks</span></span>

<span data-ttu-id="07b6d-1510">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1510">Use the dragLeave , the dragOver, and the dragOverEx to specify the behavior.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="07b6d-1511">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="07b6d-1511">Method dragOver</span></span>

<span data-ttu-id="07b6d-1512">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1512">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1513">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1513">Parameters</span></span>

<span data-ttu-id="07b6d-1514">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-1514">dragSource</span></span>  
<span data-ttu-id="07b6d-1515">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1515">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1516">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1516">dragMode</span></span>  
<span data-ttu-id="07b6d-1517">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1517">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1518">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1518">x</span></span>  
<span data-ttu-id="07b6d-1519">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1519">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1520">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1520">y</span></span>  
<span data-ttu-id="07b6d-1521">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1521">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1522">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1522">Return Value</span></span>

<span data-ttu-id="07b6d-1523">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1523">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="07b6d-1524">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-1524">Method dragOverEx</span></span>

<span data-ttu-id="07b6d-1525">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1525">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1526">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1526">Parameters</span></span>

<span data-ttu-id="07b6d-1527">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-1527">dragSource</span></span>  
<span data-ttu-id="07b6d-1528">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1528">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1529">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1529">dragMode</span></span>  
<span data-ttu-id="07b6d-1530">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1530">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1531">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1531">x</span></span>  
<span data-ttu-id="07b6d-1532">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1532">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1533">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1533">y</span></span>  
<span data-ttu-id="07b6d-1534">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1534">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1535">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1535">Return Value</span></span>

<span data-ttu-id="07b6d-1536">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1536">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="07b6d-1537">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="07b6d-1537">Method dragText</span></span>

<span data-ttu-id="07b6d-1538">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1538">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1539">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1539">Return Value</span></span>

<span data-ttu-id="07b6d-1540">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1540">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="07b6d-1541">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="07b6d-1541">Method enabled</span></span>

<span data-ttu-id="07b6d-1542">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1542">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1543">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1543">Parameters</span></span>

<span data-ttu-id="07b6d-1544">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1544">value</span></span>  
<span data-ttu-id="07b6d-1545">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1545">A Boolean value that indicates whether the control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1546">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1546">Return Value</span></span>

<span data-ttu-id="07b6d-1547">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1547">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1548">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1548">Remarks</span></span>

<span data-ttu-id="07b6d-1549">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1549">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="07b6d-1550">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1550">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="07b6d-1551">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1551">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="07b6d-1552">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="07b6d-1552">Method hasChanged</span></span>

<span data-ttu-id="07b6d-1553">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1553">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1554">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1554">Parameters</span></span>

<span data-ttu-id="07b6d-1555">val</span><span class="sxs-lookup"><span data-stu-id="07b6d-1555">val</span></span>  
<span data-ttu-id="07b6d-1556">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1556">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1557">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1557">Return Value</span></span>

<span data-ttu-id="07b6d-1558">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1558">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="07b6d-1559">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="07b6d-1559">Method hasUserSetting</span></span>

<span data-ttu-id="07b6d-1560">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1560">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1561">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1561">Return Value</span></span>

<span data-ttu-id="07b6d-1562">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1562">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="07b6d-1563">メソッド height</span><span class="sxs-lookup"><span data-stu-id="07b6d-1563">Method height</span></span>

<span data-ttu-id="07b6d-1564">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1564">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1565">Parameters</span></span>

<span data-ttu-id="07b6d-1566">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1566">value</span></span>  
<span data-ttu-id="07b6d-1567">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1567">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1568">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1568">mode</span></span>  
<span data-ttu-id="07b6d-1569">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1569">An Integer that indicates how the height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1570">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1570">Return Value</span></span>

<span data-ttu-id="07b6d-1571">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1571">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1572">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1572">Remarks</span></span>

<span data-ttu-id="07b6d-1573">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1573">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="07b6d-1574">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-1574">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="07b6d-1575">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1575">Mode.</span></span>            | <span data-ttu-id="07b6d-1576">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1576">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-1577">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1577">-1 Exact.</span></span>        | <span data-ttu-id="07b6d-1578">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1578">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-1579">0 自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1579">0 Auto.</span></span>          | <span data-ttu-id="07b6d-1580">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1580">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-1581">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1581">1 Column height.</span></span> | <span data-ttu-id="07b6d-1582">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1582">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="07b6d-1583">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1583">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="07b6d-1584">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1584">Method heightMode</span></span>

<span data-ttu-id="07b6d-1585">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1585">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1586">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1586">Parameters</span></span>

<span data-ttu-id="07b6d-1587">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1587">value</span></span>  
<span data-ttu-id="07b6d-1588">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1588">An integer value that indicates how control height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1589">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1589">Return Value</span></span>

<span data-ttu-id="07b6d-1590">計算モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1590">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1591">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1591">Remarks</span></span>

<span data-ttu-id="07b6d-1592">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-1592">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="07b6d-1593">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1593">Mode.</span></span>          | <span data-ttu-id="07b6d-1594">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1594">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-1595">正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1595">Exact.</span></span>         | <span data-ttu-id="07b6d-1596">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1596">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-1597">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1597">Auto.</span></span>          | <span data-ttu-id="07b6d-1598">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1598">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-1599">列の高さ</span><span class="sxs-lookup"><span data-stu-id="07b6d-1599">Column height.</span></span> | <span data-ttu-id="07b6d-1600">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1600">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="07b6d-1601">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1601">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="07b6d-1602">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1602">Method heightValue</span></span>

<span data-ttu-id="07b6d-1603">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1603">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1604">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1604">Parameters</span></span>

<span data-ttu-id="07b6d-1605">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1605">value</span></span>  
<span data-ttu-id="07b6d-1606">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1606">An Integer that specifies the height in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1607">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1607">Return Value</span></span>

<span data-ttu-id="07b6d-1608">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1608">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1609">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1609">Remarks</span></span>

<span data-ttu-id="07b6d-1610">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1610">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="07b6d-1611">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="07b6d-1611">Method helpField</span></span>

<span data-ttu-id="07b6d-1612">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1612">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1613">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1613">Return Value</span></span>

<span data-ttu-id="07b6d-1614">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1614">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1615">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1615">Remarks</span></span>

<span data-ttu-id="07b6d-1616">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1616">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="07b6d-1617">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1617">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="07b6d-1618">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="07b6d-1618">Method helpText</span></span>

<span data-ttu-id="07b6d-1619">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1619">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1620">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1620">Parameters</span></span>

<span data-ttu-id="07b6d-1621">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1621">value</span></span>  
<span data-ttu-id="07b6d-1622">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1622">The value that is assigned as the Help text for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1623">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1623">Return Value</span></span>

<span data-ttu-id="07b6d-1624">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1624">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1625">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1625">Remarks</span></span>

<span data-ttu-id="07b6d-1626">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1626">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="07b6d-1627">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1627">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hideifempty"></a><span data-ttu-id="07b6d-1628">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="07b6d-1628">Method hideIfEmpty</span></span>

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1629">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1629">Parameters</span></span>

<span data-ttu-id="07b6d-1630">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1630">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1631">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1631">Return Value</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="07b6d-1632">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="07b6d-1632">Method hierarchyParent</span></span>

<span data-ttu-id="07b6d-1633">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1633">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1634">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1634">Parameters</span></span>

<span data-ttu-id="07b6d-1635">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1635">value</span></span>  
<span data-ttu-id="07b6d-1636">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1636">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1637">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1637">Return Value</span></span>

<span data-ttu-id="07b6d-1638">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1638">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="07b6d-1639">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="07b6d-1639">Method hWnd</span></span>

<span data-ttu-id="07b6d-1640">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1640">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1641">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1641">Return Value</span></span>

<span data-ttu-id="07b6d-1642">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1642">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1643">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1643">Remarks</span></span>

<span data-ttu-id="07b6d-1644">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1644">The handle can be used with the Windows API.</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="07b6d-1645">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="07b6d-1645">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1646">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1646">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="07b6d-1647">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="07b6d-1647">Method isDisplayed</span></span>

<span data-ttu-id="07b6d-1648">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1648">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1649">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1649">Return Value</span></span>

<span data-ttu-id="07b6d-1650">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1650">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1651">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1651">Remarks</span></span>

<span data-ttu-id="07b6d-1652">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1652">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="07b6d-1653">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="07b6d-1653">Method isRestricted</span></span>

<span data-ttu-id="07b6d-1654">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1654">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1655">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1655">Return Value</span></span>

<span data-ttu-id="07b6d-1656">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1656">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="07b6d-1657">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="07b6d-1657">Method isUserSetupEnabled</span></span>

<span data-ttu-id="07b6d-1658">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1658">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1659">Parameters</span></span>

<span data-ttu-id="07b6d-1660">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="07b6d-1660">neededSetupRights</span></span>  
<span data-ttu-id="07b6d-1661">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1661">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1662">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1662">Return Value</span></span>

<span data-ttu-id="07b6d-1663">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1663">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1664">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1664">Remarks</span></span>

<span data-ttu-id="07b6d-1665">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1665">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-1666">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="07b6d-1666">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="07b6d-1667">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1667">No changes can be made to the control.</span></span> <span data-ttu-id="07b6d-1668">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1668">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="07b6d-1669">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="07b6d-1669">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="07b6d-1670">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1670">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="07b6d-1671">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1671">The user cannot move the control.</span></span>   |
| <span data-ttu-id="07b6d-1672">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="07b6d-1672">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="07b6d-1673">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1673">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="07b6d-1674">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1674">The user can also move the control.</span></span> |

<span data-ttu-id="07b6d-1675">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1675">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="method-leave"></a><span data-ttu-id="07b6d-1676">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="07b6d-1676">Method leave</span></span>

    public boolean leave()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1677">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1677">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="07b6d-1678">メソッド left</span><span class="sxs-lookup"><span data-stu-id="07b6d-1678">Method left</span></span>

<span data-ttu-id="07b6d-1679">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1679">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1680">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1680">Parameters</span></span>

<span data-ttu-id="07b6d-1681">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1681">value</span></span>  
<span data-ttu-id="07b6d-1682">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1682">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1683">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1683">mode</span></span>  
<span data-ttu-id="07b6d-1684">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1684">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1685">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1685">Return Value</span></span>

<span data-ttu-id="07b6d-1686">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1686">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="07b6d-1687">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="07b6d-1687">Method leftMargin</span></span>

    public int leftMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1688">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1688">Parameters</span></span>

<span data-ttu-id="07b6d-1689">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1689">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-1690">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1690">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1691">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1691">Return Value</span></span>

### <a name="method-leftmarginmode"></a><span data-ttu-id="07b6d-1692">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1692">Method leftMarginMode</span></span>

    public AutoMode leftMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1693">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1693">Parameters</span></span>

<span data-ttu-id="07b6d-1694">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1694">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1695">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1695">Return Value</span></span>

### <a name="method-leftmarginvalue"></a><span data-ttu-id="07b6d-1696">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1696">Method leftMarginValue</span></span>

    public int leftMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1697">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1697">Parameters</span></span>

<span data-ttu-id="07b6d-1698">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1698">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1699">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1699">Return Value</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="07b6d-1700">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1700">Method leftMode</span></span>

<span data-ttu-id="07b6d-1701">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1701">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1702">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1702">Parameters</span></span>

<span data-ttu-id="07b6d-1703">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1703">value</span></span>  
<span data-ttu-id="07b6d-1704">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1704">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1705">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1705">Return Value</span></span>

<span data-ttu-id="07b6d-1706">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1706">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="07b6d-1707">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1707">Method leftValue</span></span>

<span data-ttu-id="07b6d-1708">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1708">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1709">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1709">Parameters</span></span>

<span data-ttu-id="07b6d-1710">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1710">value</span></span>  
<span data-ttu-id="07b6d-1711">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1711">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1712">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1712">Return Value</span></span>

<span data-ttu-id="07b6d-1713">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1713">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="07b6d-1714">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="07b6d-1714">Method markAsUserAdd</span></span>

<span data-ttu-id="07b6d-1715">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1715">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1716">Parameters</span></span>

<span data-ttu-id="07b6d-1717">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1717">value</span></span>  
<span data-ttu-id="07b6d-1718">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1718">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1719">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1719">Return Value</span></span>

<span data-ttu-id="07b6d-1720">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1720">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="07b6d-1721">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="07b6d-1721">Method mouseDblClick</span></span>

<span data-ttu-id="07b6d-1722">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1722">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1723">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1723">Parameters</span></span>

<span data-ttu-id="07b6d-1724">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1724">x</span></span>  
<span data-ttu-id="07b6d-1725">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1725">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1726">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1726">y</span></span>  
<span data-ttu-id="07b6d-1727">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1727">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1728">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-1728">button</span></span>  
<span data-ttu-id="07b6d-1729">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1729">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1730">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1730">Ctrl</span></span>  
<span data-ttu-id="07b6d-1731">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1731">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1732">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-1732">Shift</span></span>  
<span data-ttu-id="07b6d-1733">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1733">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1734">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1734">Return Value</span></span>

<span data-ttu-id="07b6d-1735">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1735">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1736">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1736">Remarks</span></span>

<span data-ttu-id="07b6d-1737">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1737">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="07b6d-1738">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="07b6d-1738">Method mouseDown</span></span>

<span data-ttu-id="07b6d-1739">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1739">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1740">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1740">Parameters</span></span>

<span data-ttu-id="07b6d-1741">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1741">x</span></span>  
<span data-ttu-id="07b6d-1742">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1742">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1743">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1743">y</span></span>  
<span data-ttu-id="07b6d-1744">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1744">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1745">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-1745">button</span></span>  
<span data-ttu-id="07b6d-1746">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1746">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1747">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1747">Ctrl</span></span>  
<span data-ttu-id="07b6d-1748">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1748">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1749">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-1749">Shift</span></span>  
<span data-ttu-id="07b6d-1750">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1750">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1751">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1751">Return Value</span></span>

<span data-ttu-id="07b6d-1752">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1752">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1753">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1753">Remarks</span></span>

<span data-ttu-id="07b6d-1754">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1754">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="07b6d-1755">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1755">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="07b6d-1756">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="07b6d-1756">Method mouseMove</span></span>

<span data-ttu-id="07b6d-1757">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1757">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1758">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1758">Parameters</span></span>

<span data-ttu-id="07b6d-1759">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1759">x</span></span>  
<span data-ttu-id="07b6d-1760">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1760">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1761">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1761">y</span></span>  
<span data-ttu-id="07b6d-1762">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1762">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1763">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-1763">button</span></span>  
<span data-ttu-id="07b6d-1764">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1764">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1765">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1765">Ctrl</span></span>  
<span data-ttu-id="07b6d-1766">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1766">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1767">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-1767">Shift</span></span>  
<span data-ttu-id="07b6d-1768">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1768">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1769">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1769">Return Value</span></span>

<span data-ttu-id="07b6d-1770">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1770">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1771">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1771">Remarks</span></span>

<span data-ttu-id="07b6d-1772">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1772">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="07b6d-1773">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="07b6d-1773">Method mouseUp</span></span>

<span data-ttu-id="07b6d-1774">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1774">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1775">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1775">Parameters</span></span>

<span data-ttu-id="07b6d-1776">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-1776">x</span></span>  
<span data-ttu-id="07b6d-1777">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1777">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1778">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-1778">y</span></span>  
<span data-ttu-id="07b6d-1779">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1779">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1780">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-1780">button</span></span>  
<span data-ttu-id="07b6d-1781">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1781">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1782">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1782">Ctrl</span></span>  
<span data-ttu-id="07b6d-1783">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1783">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1784">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-1784">Shift</span></span>  
<span data-ttu-id="07b6d-1785">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1785">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1786">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1786">Return Value</span></span>

<span data-ttu-id="07b6d-1787">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1787">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1788">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1788">Remarks</span></span>

<span data-ttu-id="07b6d-1789">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1789">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="07b6d-1790">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1790">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-name"></a><span data-ttu-id="07b6d-1791">メソッド名</span><span class="sxs-lookup"><span data-stu-id="07b6d-1791">Method name</span></span>

<span data-ttu-id="07b6d-1792">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1792">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1793">Parameters</span></span>

<span data-ttu-id="07b6d-1794">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1794">value</span></span>  
<span data-ttu-id="07b6d-1795">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1795">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1796">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1796">Return Value</span></span>

<span data-ttu-id="07b6d-1797">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1797">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1798">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1798">Remarks</span></span>

<span data-ttu-id="07b6d-1799">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1799">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="07b6d-1800">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1800">It must begin with a letter.</span></span>
-   <span data-ttu-id="07b6d-1801">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1801">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="07b6d-1802">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1802">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="07b6d-1803">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1803">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="07b6d-1804">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1804">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="07b6d-1805">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="07b6d-1805">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1806">Parameters</span></span>

<span data-ttu-id="07b6d-1807">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1808">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1808">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="07b6d-1809">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="07b6d-1809">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1810">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1810">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="07b6d-1811">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-1811">Method parentControl</span></span>

<span data-ttu-id="07b6d-1812">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1812">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1813">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1813">Return Value</span></span>

<span data-ttu-id="07b6d-1814">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1814">The parent control for the control.</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="07b6d-1815">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="07b6d-1815">Method rightMargin</span></span>

    public int rightMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1816">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1816">Parameters</span></span>

<span data-ttu-id="07b6d-1817">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1817">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-1818">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1818">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1819">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1819">Return Value</span></span>

### <a name="method-rightmarginmode"></a><span data-ttu-id="07b6d-1820">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1820">Method rightMarginMode</span></span>

    public AutoMode rightMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1821">Parameters</span></span>

<span data-ttu-id="07b6d-1822">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1822">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1823">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1823">Return Value</span></span>

### <a name="method-rightmarginvalue"></a><span data-ttu-id="07b6d-1824">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1824">Method rightMarginValue</span></span>

    public int rightMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1825">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1825">Parameters</span></span>

<span data-ttu-id="07b6d-1826">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1826">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1827">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1827">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="07b6d-1828">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="07b6d-1828">Method securityKey</span></span>

<span data-ttu-id="07b6d-1829">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1829">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1830">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1830">Parameters</span></span>

<span data-ttu-id="07b6d-1831">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1831">value</span></span>  
<span data-ttu-id="07b6d-1832">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1832">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1833">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1833">Return Value</span></span>

<span data-ttu-id="07b6d-1834">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1834">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="07b6d-1835">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="07b6d-1835">Method showContextMenu</span></span>

<span data-ttu-id="07b6d-1836">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1836">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1837">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1837">Parameters</span></span>

<span data-ttu-id="07b6d-1838">menuHandle</span><span class="sxs-lookup"><span data-stu-id="07b6d-1838">menuHandle</span></span>  
<span data-ttu-id="07b6d-1839">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1839">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1840">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1840">Return Value</span></span>

<span data-ttu-id="07b6d-1841">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1841">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-skip"></a><span data-ttu-id="07b6d-1842">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="07b6d-1842">Method skip</span></span>

<span data-ttu-id="07b6d-1843">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1843">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1844">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1844">Parameters</span></span>

<span data-ttu-id="07b6d-1845">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1845">value</span></span>  
<span data-ttu-id="07b6d-1846">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1846">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1847">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1847">Return Value</span></span>

<span data-ttu-id="07b6d-1848">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1848">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1849">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1849">Remarks</span></span>

<span data-ttu-id="07b6d-1850">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1850">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="method-sort"></a><span data-ttu-id="07b6d-1851">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="07b6d-1851">Method sort</span></span>

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1852">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1852">Parameters</span></span>

<span data-ttu-id="07b6d-1853">sortDirection</span><span class="sxs-lookup"><span data-stu-id="07b6d-1853">sortDirection</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1854">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1854">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="07b6d-1855">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="07b6d-1855">Method toolTip</span></span>

<span data-ttu-id="07b6d-1856">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1856">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="07b6d-1857">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1857">Return Value</span></span>

<span data-ttu-id="07b6d-1858">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1858">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1859">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1859">Remarks</span></span>

<span data-ttu-id="07b6d-1860">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1860">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="07b6d-1861">メソッド top</span><span class="sxs-lookup"><span data-stu-id="07b6d-1861">Method top</span></span>

<span data-ttu-id="07b6d-1862">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1862">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1863">Parameters</span></span>

<span data-ttu-id="07b6d-1864">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1864">value</span></span>  
<span data-ttu-id="07b6d-1865">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1865">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-1866">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1866">mode</span></span>  
<span data-ttu-id="07b6d-1867">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1867">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1868">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1868">Return Value</span></span>

<span data-ttu-id="07b6d-1869">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1869">The vertical position of the control in the form.</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="07b6d-1870">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="07b6d-1870">Method topMargin</span></span>

    public int topMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1871">Parameters</span></span>

<span data-ttu-id="07b6d-1872">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1872">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-1873">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1873">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1874">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1874">Return Value</span></span>

### <a name="method-topmarginmode"></a><span data-ttu-id="07b6d-1875">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1875">Method topMarginMode</span></span>

    public AutoMode topMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1876">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1876">Parameters</span></span>

<span data-ttu-id="07b6d-1877">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-1877">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1878">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1878">Return Value</span></span>

### <a name="method-topmarginvalue"></a><span data-ttu-id="07b6d-1879">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1879">Method topMarginValue</span></span>

    public int topMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1880">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1880">Parameters</span></span>

<span data-ttu-id="07b6d-1881">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1881">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1882">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1882">Return Value</span></span>

### <a name="method-topmode"></a><span data-ttu-id="07b6d-1883">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-1883">Method topMode</span></span>

<span data-ttu-id="07b6d-1884">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1884">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1885">Parameters</span></span>

<span data-ttu-id="07b6d-1886">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1886">value</span></span>  
<span data-ttu-id="07b6d-1887">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1887">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1888">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1888">Return Value</span></span>

<span data-ttu-id="07b6d-1889">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1889">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="07b6d-1890">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-1890">Method topValue</span></span>

<span data-ttu-id="07b6d-1891">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1891">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1892">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1892">Parameters</span></span>

<span data-ttu-id="07b6d-1893">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1893">value</span></span>  
<span data-ttu-id="07b6d-1894">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1894">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1895">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1895">Return Value</span></span>

<span data-ttu-id="07b6d-1896">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1896">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="07b6d-1897">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="07b6d-1897">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1898">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1898">Parameters</span></span>

<span data-ttu-id="07b6d-1899">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1899">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1900">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1900">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="07b6d-1901">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="07b6d-1901">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="07b6d-1902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1902">Parameters</span></span>

<span data-ttu-id="07b6d-1903">データ</span><span class="sxs-lookup"><span data-stu-id="07b6d-1903">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-1904">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1904">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="07b6d-1905">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="07b6d-1905">Method userData</span></span>

<span data-ttu-id="07b6d-1906">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1906">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1907">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1907">Parameters</span></span>

<span data-ttu-id="07b6d-1908">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1908">value</span></span>  
<span data-ttu-id="07b6d-1909">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1909">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1910">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1910">Return Value</span></span>

<span data-ttu-id="07b6d-1911">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1911">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="07b6d-1912">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="07b6d-1912">Method userDataItem</span></span>

<span data-ttu-id="07b6d-1913">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1913">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1914">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1914">Parameters</span></span>

<span data-ttu-id="07b6d-1915">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1915">value</span></span>  
<span data-ttu-id="07b6d-1916">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1916">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1917">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1917">Return Value</span></span>

<span data-ttu-id="07b6d-1918">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1918">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="07b6d-1919">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="07b6d-1919">Method userDataItems</span></span>

<span data-ttu-id="07b6d-1920">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1920">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1921">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1921">Parameters</span></span>

<span data-ttu-id="07b6d-1922">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1922">value</span></span>  
<span data-ttu-id="07b6d-1923">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1923">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1924">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1924">Return Value</span></span>

<span data-ttu-id="07b6d-1925">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1925">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="07b6d-1926">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="07b6d-1926">Method userDisable</span></span>

<span data-ttu-id="07b6d-1927">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1927">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1928">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1928">Parameters</span></span>

<span data-ttu-id="07b6d-1929">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1929">value</span></span>  
<span data-ttu-id="07b6d-1930">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1930">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1931">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1931">Return Value</span></span>

<span data-ttu-id="07b6d-1932">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1932">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="07b6d-1933">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="07b6d-1933">Method userHeight</span></span>

<span data-ttu-id="07b6d-1934">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1934">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1935">Parameters</span></span>

<span data-ttu-id="07b6d-1936">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1936">value</span></span>  
<span data-ttu-id="07b6d-1937">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1937">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1938">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1938">Return Value</span></span>

<span data-ttu-id="07b6d-1939">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1939">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="07b6d-1940">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="07b6d-1940">Method userHide</span></span>

<span data-ttu-id="07b6d-1941">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1941">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1942">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1942">Parameters</span></span>

<span data-ttu-id="07b6d-1943">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1943">value</span></span>  
<span data-ttu-id="07b6d-1944">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1944">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1945">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1945">Return Value</span></span>

<span data-ttu-id="07b6d-1946">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1946">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1947">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1947">Remarks</span></span>

<span data-ttu-id="07b6d-1948">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1948">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="07b6d-1949">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1949">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="07b6d-1950">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1950">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="07b6d-1951">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="07b6d-1951">Method userOrgContainer</span></span>

<span data-ttu-id="07b6d-1952">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1952">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1953">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1953">Parameters</span></span>

<span data-ttu-id="07b6d-1954">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1954">value</span></span>  
<span data-ttu-id="07b6d-1955">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1955">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1956">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1956">Return Value</span></span>

<span data-ttu-id="07b6d-1957">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1957">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="07b6d-1958">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="07b6d-1958">Method userOrgSibling</span></span>

<span data-ttu-id="07b6d-1959">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1959">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1960">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1960">Parameters</span></span>

<span data-ttu-id="07b6d-1961">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1961">value</span></span>  
<span data-ttu-id="07b6d-1962">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1962">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1963">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1963">Return Value</span></span>

<span data-ttu-id="07b6d-1964">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1964">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="07b6d-1965">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="07b6d-1965">Method userPromptText</span></span>

<span data-ttu-id="07b6d-1966">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1966">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1967">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1967">Parameters</span></span>

<span data-ttu-id="07b6d-1968">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1968">value</span></span>  
<span data-ttu-id="07b6d-1969">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1969">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1970">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1970">Return Value</span></span>

<span data-ttu-id="07b6d-1971">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1971">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="07b6d-1972">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="07b6d-1972">Method userSecurityLevel</span></span>

<span data-ttu-id="07b6d-1973">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1973">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1974">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1974">Parameters</span></span>

<span data-ttu-id="07b6d-1975">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1975">value</span></span>  
<span data-ttu-id="07b6d-1976">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1976">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1977">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1977">Return Value</span></span>

<span data-ttu-id="07b6d-1978">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1978">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="07b6d-1979">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="07b6d-1979">Method userSkip</span></span>

<span data-ttu-id="07b6d-1980">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1980">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1981">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1981">Parameters</span></span>

<span data-ttu-id="07b6d-1982">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1982">value</span></span>  
<span data-ttu-id="07b6d-1983">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1983">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="07b6d-1984">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1984">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1985">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1985">Return Value</span></span>

<span data-ttu-id="07b6d-1986">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1986">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="07b6d-1987">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="07b6d-1987">Method userWidth</span></span>

<span data-ttu-id="07b6d-1988">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1988">Sets or returns the width of the control in pixels.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-1989">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-1989">Parameters</span></span>

<span data-ttu-id="07b6d-1990">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1990">value</span></span>  
<span data-ttu-id="07b6d-1991">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1991">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-1992">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-1992">Return Value</span></span>

<span data-ttu-id="07b6d-1993">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1993">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-1994">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-1994">Remarks</span></span>

<span data-ttu-id="07b6d-1995">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1995">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="07b6d-1996">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1996">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="07b6d-1997">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1997">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="07b6d-1998">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="07b6d-1998">Method verticalSpacing</span></span>

<span data-ttu-id="07b6d-1999">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-1999">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2000">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2000">Parameters</span></span>

<span data-ttu-id="07b6d-2001">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2001">value</span></span>  
<span data-ttu-id="07b6d-2002">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2002">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2003">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-2003">mode</span></span>  
<span data-ttu-id="07b6d-2004">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2004">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2005">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2005">Return Value</span></span>

<span data-ttu-id="07b6d-2006">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2006">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="07b6d-2007">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-2007">Method verticalSpacingMode</span></span>

<span data-ttu-id="07b6d-2008">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2008">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2009">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2009">Parameters</span></span>

<span data-ttu-id="07b6d-2010">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-2010">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2011">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2011">Return Value</span></span>

<span data-ttu-id="07b6d-2012">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2012">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="07b6d-2013">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-2013">Method verticalSpacingValue</span></span>

<span data-ttu-id="07b6d-2014">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2014">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2015">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2015">Parameters</span></span>

<span data-ttu-id="07b6d-2016">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2016">value</span></span>  
<span data-ttu-id="07b6d-2017">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2017">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2018">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2018">Return Value</span></span>

<span data-ttu-id="07b6d-2019">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2019">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="07b6d-2020">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="07b6d-2020">Method visible</span></span>

<span data-ttu-id="07b6d-2021">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2021">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2022">Parameters</span></span>

<span data-ttu-id="07b6d-2023">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2023">value</span></span>  
<span data-ttu-id="07b6d-2024">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2024">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2025">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2025">Return Value</span></span>

<span data-ttu-id="07b6d-2026">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2026">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="07b6d-2027">メソッド width</span><span class="sxs-lookup"><span data-stu-id="07b6d-2027">Method width</span></span>

<span data-ttu-id="07b6d-2028">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2028">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2029">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2029">Parameters</span></span>

<span data-ttu-id="07b6d-2030">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2030">value</span></span>  
<span data-ttu-id="07b6d-2031">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2031">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2032">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-2032">mode</span></span>  
<span data-ttu-id="07b6d-2033">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2033">An Integer that indicates how the width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2034">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2034">Return Value</span></span>

<span data-ttu-id="07b6d-2035">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2035">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2036">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2036">Remarks</span></span>

<span data-ttu-id="07b6d-2037">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2037">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="07b6d-2038">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-2038">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="07b6d-2039">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2039">Mode.</span></span>           | <span data-ttu-id="07b6d-2040">幅計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2040">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-2041">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2041">-1 Exact.</span></span>       | <span data-ttu-id="07b6d-2042">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2042">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-2043">0 自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2043">0 Auto.</span></span>         | <span data-ttu-id="07b6d-2044">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2044">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-2045">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2045">1 Column width.</span></span> | <span data-ttu-id="07b6d-2046">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2046">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="07b6d-2047">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2047">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="07b6d-2048">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-2048">Method widthMode</span></span>

<span data-ttu-id="07b6d-2049">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2049">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2050">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2050">Parameters</span></span>

<span data-ttu-id="07b6d-2051">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2051">value</span></span>  
<span data-ttu-id="07b6d-2052">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2052">An integer value that indicates how control width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2053">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2053">Return Value</span></span>

<span data-ttu-id="07b6d-2054">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2054">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2055">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2055">Remarks</span></span>

<span data-ttu-id="07b6d-2056">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-2056">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="07b6d-2057">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2057">Mode.</span></span>         | <span data-ttu-id="07b6d-2058">幅計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2058">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-2059">正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2059">Exact.</span></span>        | <span data-ttu-id="07b6d-2060">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2060">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-2061">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2061">Auto.</span></span>         | <span data-ttu-id="07b6d-2062">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2062">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-2063">列の幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2063">Column width.</span></span> | <span data-ttu-id="07b6d-2064">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2064">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="07b6d-2065">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2065">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="07b6d-2066">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-2066">Method widthValue</span></span>

<span data-ttu-id="07b6d-2067">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2067">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2068">Parameters</span></span>

<span data-ttu-id="07b6d-2069">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2069">value</span></span>  
<span data-ttu-id="07b6d-2070">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2070">An Integer that specifies the width in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2071">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2071">Return Value</span></span>

<span data-ttu-id="07b6d-2072">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2072">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2073">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2073">Remarks</span></span>

<span data-ttu-id="07b6d-2074">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2074">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-onenter"></a><span data-ttu-id="07b6d-2075">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="07b6d-2075">Method OnEnter</span></span>

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2076">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2076">Parameters</span></span>

<span data-ttu-id="07b6d-2077">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-2077">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-2078">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-2078">e</span></span>  

### <a name="method-lostfocus"></a><span data-ttu-id="07b6d-2079">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-2079">Method lostFocus</span></span>

<span data-ttu-id="07b6d-2080">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2080">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-drop"></a><span data-ttu-id="07b6d-2081">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="07b6d-2081">Method drop</span></span>

<span data-ttu-id="07b6d-2082">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2082">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2083">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2083">Parameters</span></span>

<span data-ttu-id="07b6d-2084">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-2084">dragSource</span></span>  
<span data-ttu-id="07b6d-2085">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2085">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2086">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-2086">dragMode</span></span>  
<span data-ttu-id="07b6d-2087">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2087">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2088">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-2088">x</span></span>  
<span data-ttu-id="07b6d-2089">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2089">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2090">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-2090">y</span></span>  
<span data-ttu-id="07b6d-2091">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2091">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-paste"></a><span data-ttu-id="07b6d-2092">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="07b6d-2092">Method paste</span></span>

<span data-ttu-id="07b6d-2093">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2093">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-setfocus"></a><span data-ttu-id="07b6d-2094">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-2094">Method setFocus</span></span>

<span data-ttu-id="07b6d-2095">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2095">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-onleaving"></a><span data-ttu-id="07b6d-2096">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="07b6d-2096">Method OnLeaving</span></span>

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2097">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2097">Parameters</span></span>

<span data-ttu-id="07b6d-2098">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-2098">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-2099">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-2099">e</span></span>  

### <a name="method-mouseleave"></a><span data-ttu-id="07b6d-2100">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="07b6d-2100">Method mouseLeave</span></span>

<span data-ttu-id="07b6d-2101">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2101">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-gotfocus"></a><span data-ttu-id="07b6d-2102">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-2102">Method gotFocus</span></span>

<span data-ttu-id="07b6d-2103">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2103">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-dragleave"></a><span data-ttu-id="07b6d-2104">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="07b6d-2104">Method dragLeave</span></span>

<span data-ttu-id="07b6d-2105">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2105">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-enter"></a><span data-ttu-id="07b6d-2106">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="07b6d-2106">Method enter</span></span>

    public void enter()

### <a name="method-dropex"></a><span data-ttu-id="07b6d-2107">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-2107">Method dropEx</span></span>

<span data-ttu-id="07b6d-2108">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2108">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2109">Parameters</span></span>

<span data-ttu-id="07b6d-2110">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-2110">dragSource</span></span>  
<span data-ttu-id="07b6d-2111">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2111">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2112">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-2112">dragMode</span></span>  
<span data-ttu-id="07b6d-2113">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2113">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2114">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-2114">x</span></span>  
<span data-ttu-id="07b6d-2115">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2115">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2116">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-2116">y</span></span>  
<span data-ttu-id="07b6d-2117">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2117">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-mouseenter"></a><span data-ttu-id="07b6d-2118">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="07b6d-2118">Method mouseEnter</span></span>

<span data-ttu-id="07b6d-2119">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2119">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2120">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2120">Parameters</span></span>

<span data-ttu-id="07b6d-2121">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-2121">x</span></span>  
<span data-ttu-id="07b6d-2122">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2122">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2123">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-2123">y</span></span>  
<span data-ttu-id="07b6d-2124">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2124">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2125">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-2125">button</span></span>  
<span data-ttu-id="07b6d-2126">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2126">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2127">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-2127">Ctrl</span></span>  
<span data-ttu-id="07b6d-2128">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2128">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2129">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-2129">Shift</span></span>  
<span data-ttu-id="07b6d-2130">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2130">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-jumpref"></a><span data-ttu-id="07b6d-2131">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="07b6d-2131">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-onlostfocus"></a><span data-ttu-id="07b6d-2132">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-2132">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2133">Parameters</span></span>

<span data-ttu-id="07b6d-2134">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-2134">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-2135">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-2135">e</span></span>  

### <a name="method-ongotfocus"></a><span data-ttu-id="07b6d-2136">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-2136">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2137">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2137">Parameters</span></span>

<span data-ttu-id="07b6d-2138">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-2138">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-2139">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-2139">e</span></span>  

### <a name="method-prefcolumnsize"></a><span data-ttu-id="07b6d-2140">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-2140">Method prefColumnSize</span></span>

<span data-ttu-id="07b6d-2141">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2141">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2142">Parameters</span></span>

<span data-ttu-id="07b6d-2143">width</span><span class="sxs-lookup"><span data-stu-id="07b6d-2143">width</span></span>  
<span data-ttu-id="07b6d-2144">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2144">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2145">height</span><span class="sxs-lookup"><span data-stu-id="07b6d-2145">height</span></span>  
<span data-ttu-id="07b6d-2146">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2146">The preferred height of the control.</span></span>

### <a name="method-cut"></a><span data-ttu-id="07b6d-2147">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="07b6d-2147">Method cut</span></span>

<span data-ttu-id="07b6d-2148">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2148">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-registeroverridemethod"></a><span data-ttu-id="07b6d-2149">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="07b6d-2149">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2150">Parameters</span></span>

<span data-ttu-id="07b6d-2151">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="07b6d-2151">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="07b6d-2152">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="07b6d-2152">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="07b6d-2153">overrideObject</span><span class="sxs-lookup"><span data-stu-id="07b6d-2153">overrideObject</span></span>  

### <a name="method-displaycontrol"></a><span data-ttu-id="07b6d-2154">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-2154">Method displayControl</span></span>

<span data-ttu-id="07b6d-2155">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2155">Displays the control.</span></span>

    public void displayControl()

### <a name="method-copy"></a><span data-ttu-id="07b6d-2156">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="07b6d-2156">Method copy</span></span>

<span data-ttu-id="07b6d-2157">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2157">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-context"></a><span data-ttu-id="07b6d-2158">メソッド context</span><span class="sxs-lookup"><span data-stu-id="07b6d-2158">Method context</span></span>

<span data-ttu-id="07b6d-2159">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2159">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-resetusersetting"></a><span data-ttu-id="07b6d-2160">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="07b6d-2160">Method resetUserSetting</span></span>

<span data-ttu-id="07b6d-2161">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2161">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-inputsearch"></a><span data-ttu-id="07b6d-2162">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="07b6d-2162">Method inputSearch</span></span>

<span data-ttu-id="07b6d-2163">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2163">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2164">Parameters</span></span>

<span data-ttu-id="07b6d-2165">searchStr</span><span class="sxs-lookup"><span data-stu-id="07b6d-2165">searchStr</span></span>  
<span data-ttu-id="07b6d-2166">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2166">The string value to use to filter data; optional.</span></span>

### <a name="method-filter"></a><span data-ttu-id="07b6d-2167">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="07b6d-2167">Method filter</span></span>

    public void filter([str filterStr])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2168">Parameters</span></span>

<span data-ttu-id="07b6d-2169">filterStr</span><span class="sxs-lookup"><span data-stu-id="07b6d-2169">filterStr</span></span>  

### <a name="method-enddrag"></a><span data-ttu-id="07b6d-2170">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="07b6d-2170">Method endDrag</span></span>

<span data-ttu-id="07b6d-2171">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2171">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="07b6d-2172">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2172">Remarks</span></span>

<span data-ttu-id="07b6d-2173">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2173">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="07b6d-2174">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2174">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="class-formfunctionbuttoncontrol"></a><span data-ttu-id="07b6d-2175">クラス FormFunctionButtonControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-2175">Class FormFunctionButtonControl</span></span>
    class FormFunctionButtonControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="07b6d-2176">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2176">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="07b6d-2177">例</span><span class="sxs-lookup"><span data-stu-id="07b6d-2177">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="07b6d-2178">メソッド</span><span class="sxs-lookup"><span data-stu-id="07b6d-2178">Methods</span></span>

| <span data-ttu-id="07b6d-2179">方法</span><span class="sxs-lookup"><span data-stu-id="07b6d-2179">Method</span></span>                                                                                                      | <span data-ttu-id="07b6d-2180">説明</span><span class="sxs-lookup"><span data-stu-id="07b6d-2180">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-2181">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2181">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="07b6d-2182">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2182">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-2183">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2183">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2184">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2184">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="07b6d-2185">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2185">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-2186">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2186">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="07b6d-2187">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2187">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="07b6d-2188">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2188">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="07b6d-2189">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2189">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="07b6d-2190">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2190">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2191">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2191">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="07b6d-2192">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2192">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="07b6d-2193">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2193">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-2194">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2194">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-2195">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2195">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="07b6d-2196">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2196">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-2197">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2197">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2198">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2198">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="07b6d-2199">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2199">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-2200">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2200">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="07b6d-2201">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2201">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="07b6d-2202">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2202">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="07b6d-2203">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2203">Gets or sets the appearance of the button control.</span></span>                                                                                                                      |
| <span data-ttu-id="07b6d-2204">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2204">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="07b6d-2205">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2205">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="07b6d-2206">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2206">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="07b6d-2207">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2207">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-2208">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2208">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="07b6d-2209">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2209">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-2210">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2210">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="07b6d-2211">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2211">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-2212">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2212">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="07b6d-2213">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2213">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-2214">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2214">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="07b6d-2215">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2215">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-2216">public int copyCallerQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2216">public int copyCallerQuery(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2217">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2217">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="07b6d-2218">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2218">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="07b6d-2219">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2219">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2220">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2220">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="07b6d-2221">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2221">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="07b6d-2222">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2222">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="07b6d-2223">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2223">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-2224">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2224">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="07b6d-2225">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2225">Determines whether the button should be the default button in the form.</span></span>                                                                                                 |
| <span data-ttu-id="07b6d-2226">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2226">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="07b6d-2227">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2227">Gets or sets the disabled image of the button.</span></span>                                                                                                                          |
| <span data-ttu-id="07b6d-2228">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2228">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2229">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2229">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="07b6d-2230">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2230">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                                                          |
| <span data-ttu-id="07b6d-2231">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2231">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="07b6d-2232">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2232">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, Finance and Operations, or in both.</span></span> |
| <span data-ttu-id="07b6d-2233">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2233">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-2234">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2234">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="07b6d-2235">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2235">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="07b6d-2236">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2236">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="07b6d-2237">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2237">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="07b6d-2238">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2238">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-2239">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2239">public str dragText()</span></span>                                                                                       | <span data-ttu-id="07b6d-2240">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2240">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-2241">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2241">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="07b6d-2242">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2242">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-2243">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2243">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="07b6d-2244">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2244">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="07b6d-2245">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2245">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-2246">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2246">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="07b6d-2247">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2247">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2248">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2248">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="07b6d-2249">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2249">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-2250">public int formViewOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2250">public int formViewOption(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2251">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2251">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="07b6d-2252">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2252">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="07b6d-2253">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2253">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="07b6d-2254">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2254">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="07b6d-2255">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2255">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="07b6d-2256">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2256">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-2257">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2257">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-2258">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2258">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-2259">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2259">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="07b6d-2260">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2260">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-2261">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2261">public str helpField()</span></span>                                                                                      | <span data-ttu-id="07b6d-2262">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2262">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-2263">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2263">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="07b6d-2264">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2264">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="07b6d-2265">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2265">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="07b6d-2266">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2266">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="07b6d-2267">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2267">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="07b6d-2268">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2268">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-2269">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2269">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2270">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2270">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2271">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2271">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="07b6d-2272">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2272">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="07b6d-2273">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2273">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="07b6d-2274">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2274">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-2275">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2275">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="07b6d-2276">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2276">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="07b6d-2277">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2277">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2278">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2278">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2279">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2279">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="07b6d-2280">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2280">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="07b6d-2281">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2281">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-2282">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2282">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-2283">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2283">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-2284">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2284">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="07b6d-2285">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2285">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="07b6d-2286">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2286">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="07b6d-2287">public xMenuFunction menufunction()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2287">public xMenuFunction menufunction()</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2288">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2288">public str menuItemName(\[str value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2289">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2289">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2290">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2290">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="07b6d-2291">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2291">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="07b6d-2292">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2292">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="07b6d-2293">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2293">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-2294">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2294">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="07b6d-2295">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2295">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-2296">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2296">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="07b6d-2297">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2297">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="07b6d-2298">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2298">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2299">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2299">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="07b6d-2300">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2300">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="07b6d-2301">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2301">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2302">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2302">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2303">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2303">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2304">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2304">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2305">public int openMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2305">public int openMode(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2306">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2306">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2307">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2307">public str parameters(\[str value\])</span></span>                                                                        | <span data-ttu-id="07b6d-2308">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2308">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                                                  |
| <span data-ttu-id="07b6d-2309">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2309">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="07b6d-2310">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2310">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-2311">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2311">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2312">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2312">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2313">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2313">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="07b6d-2314">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2314">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-2315">public boolean sendExternalContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2315">public boolean sendExternalContext(\[boolean value\])</span></span>                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2316">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2316">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2317">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2317">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="07b6d-2318">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2318">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-2319">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2319">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2320">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2320">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="07b6d-2321">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2321">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="07b6d-2322">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2322">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2323">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2323">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2324">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2324">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2325">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2325">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="07b6d-2326">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2326">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-2327">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2327">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="07b6d-2328">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2328">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-2329">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2329">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="07b6d-2330">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2330">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-2331">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2331">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-2332">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2332">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-2333">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2333">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2334">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2334">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2335">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2335">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2336">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2336">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-2337">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2337">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-2338">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2338">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="07b6d-2339">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2339">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="07b6d-2340">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2340">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="07b6d-2341">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2341">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-2342">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2342">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="07b6d-2343">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2343">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="07b6d-2344">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2344">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-2345">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2345">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="07b6d-2346">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2346">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-2347">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2347">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="07b6d-2348">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2348">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="07b6d-2349">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2349">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="07b6d-2350">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2350">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="07b6d-2351">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2351">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-2352">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2352">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="07b6d-2353">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2353">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="07b6d-2354">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2354">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="07b6d-2355">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2355">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="07b6d-2356">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2356">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-2357">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2357">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="07b6d-2358">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2358">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-2359">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2359">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-2360">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2360">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2361">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2361">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="07b6d-2362">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2362">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-2363">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2363">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="07b6d-2364">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2364">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-2365">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2365">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="07b6d-2366">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2366">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-2367">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2367">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="07b6d-2368">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2368">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-2369">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2369">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="07b6d-2370">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2370">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="07b6d-2371">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2371">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-2372">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2372">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-2373">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2373">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="07b6d-2374">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2374">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="07b6d-2375">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2375">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="07b6d-2376">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2376">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="07b6d-2377">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2377">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="07b6d-2378">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2378">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="07b6d-2379">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2379">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="07b6d-2380">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2380">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="07b6d-2381">public void context()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2381">public void context()</span></span>                                                                                       | <span data-ttu-id="07b6d-2382">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2382">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-2383">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2383">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="07b6d-2384">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2384">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="07b6d-2385">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2385">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2386">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2386">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="07b6d-2387">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2387">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="07b6d-2388">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2388">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="07b6d-2389">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2389">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-2390">public void paste()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2390">public void paste()</span></span>                                                                                         | <span data-ttu-id="07b6d-2391">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2391">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-2392">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2392">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2393">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2393">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="07b6d-2394">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2394">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-2395">public void cut()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2395">public void cut()</span></span>                                                                                           | <span data-ttu-id="07b6d-2396">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2396">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="07b6d-2397">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2397">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2398">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2398">public void displayControl()</span></span>                                                                                | <span data-ttu-id="07b6d-2399">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2399">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="07b6d-2400">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2400">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="07b6d-2401">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2401">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="07b6d-2402">public void copy()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2402">public void copy()</span></span>                                                                                          | <span data-ttu-id="07b6d-2403">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2403">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="07b6d-2404">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2404">public void clicked()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2405">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2405">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2406">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-2406">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="07b6d-2407">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2407">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="07b6d-2408">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2408">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="07b6d-2409">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2409">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-2410">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2410">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="07b6d-2411">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2411">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="07b6d-2412">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2412">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="07b6d-2413">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2413">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-2414">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="07b6d-2414">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-2415">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-2415">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |

### <a name="method-aligncontrol"></a><span data-ttu-id="07b6d-2416">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-2416">Method alignControl</span></span>

<span data-ttu-id="07b6d-2417">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2417">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2418">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2418">Parameters</span></span>

<span data-ttu-id="07b6d-2419">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2419">value</span></span>  
<span data-ttu-id="07b6d-2420">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2420">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2421">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2421">Return Value</span></span>

<span data-ttu-id="07b6d-2422">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2422">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2423">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2423">Remarks</span></span>

<span data-ttu-id="07b6d-2424">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2424">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-alignment"></a><span data-ttu-id="07b6d-2425">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="07b6d-2425">Method alignment</span></span>

    public int alignment([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2426">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2426">Parameters</span></span>

<span data-ttu-id="07b6d-2427">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2427">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2428">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2428">Return Value</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="07b6d-2429">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="07b6d-2429">Method allowEdit</span></span>

<span data-ttu-id="07b6d-2430">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2430">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2431">Parameters</span></span>

<span data-ttu-id="07b6d-2432">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2432">value</span></span>  
<span data-ttu-id="07b6d-2433">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2433">The value to assign to the allowEdit property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2434">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2434">Return Value</span></span>

<span data-ttu-id="07b6d-2435">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2435">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2436">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2436">Remarks</span></span>

<span data-ttu-id="07b6d-2437">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2437">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="07b6d-2438">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="07b6d-2438">Method allowSysSetup</span></span>

<span data-ttu-id="07b6d-2439">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2439">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2440">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2440">Return Value</span></span>

<span data-ttu-id="07b6d-2441">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2441">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="07b6d-2442">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="07b6d-2442">Method autoDeclaration</span></span>

<span data-ttu-id="07b6d-2443">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2443">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2444">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2444">Parameters</span></span>

<span data-ttu-id="07b6d-2445">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2445">value</span></span>  
<span data-ttu-id="07b6d-2446">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2446">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2447">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2447">Return Value</span></span>

<span data-ttu-id="07b6d-2448">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2448">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2449">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2449">Remarks</span></span>

<span data-ttu-id="07b6d-2450">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2450">Controls cannot have identical names.</span></span>

### <a name="method-autorefreshdata"></a><span data-ttu-id="07b6d-2451">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="07b6d-2451">Method autoRefreshData</span></span>

    public boolean autoRefreshData([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2452">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2452">Parameters</span></span>

<span data-ttu-id="07b6d-2453">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2453">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2454">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2454">Return Value</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="07b6d-2455">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="07b6d-2455">Method backgroundColor</span></span>

<span data-ttu-id="07b6d-2456">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2456">Gets or sets the background color of the control.</span></span>

    public int backgroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2457">Parameters</span></span>

<span data-ttu-id="07b6d-2458">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2458">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2459">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2459">Return Value</span></span>

<span data-ttu-id="07b6d-2460">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2460">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2461">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2461">Remarks</span></span>

<span data-ttu-id="07b6d-2462">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2462">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="07b6d-2463">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2463">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="07b6d-2464">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2464">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="07b6d-2465">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2465">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="07b6d-2466">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2466">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="07b6d-2467">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2467">The maximum value for a single byte is 255.</span></span>

### <a name="method-backstyle"></a><span data-ttu-id="07b6d-2468">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="07b6d-2468">Method backStyle</span></span>

<span data-ttu-id="07b6d-2469">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2469">Determines whether the control background can be transparent.</span></span>

    public int backStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2470">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2470">Parameters</span></span>

<span data-ttu-id="07b6d-2471">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2471">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2472">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2472">Return Value</span></span>

<span data-ttu-id="07b6d-2473">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2473">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="07b6d-2474">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="07b6d-2474">Method beginDrag</span></span>

<span data-ttu-id="07b6d-2475">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2475">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2476">Parameters</span></span>

<span data-ttu-id="07b6d-2477">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-2477">x</span></span>  
<span data-ttu-id="07b6d-2478">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2478">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="07b6d-2479">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2479">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2480">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-2480">y</span></span>  
<span data-ttu-id="07b6d-2481">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2481">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="07b6d-2482">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2482">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2483">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2483">Return Value</span></span>

<span data-ttu-id="07b6d-2484">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2484">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2485">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2485">Remarks</span></span>

<span data-ttu-id="07b6d-2486">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2486">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="07b6d-2487">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2487">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-big"></a><span data-ttu-id="07b6d-2488">メソッド big</span><span class="sxs-lookup"><span data-stu-id="07b6d-2488">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2489">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2489">Parameters</span></span>

<span data-ttu-id="07b6d-2490">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2490">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2491">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2491">Return Value</span></span>

### <a name="method-bold"></a><span data-ttu-id="07b6d-2492">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="07b6d-2492">Method bold</span></span>

<span data-ttu-id="07b6d-2493">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2493">Gets or sets the weight of font used to output text in the control.</span></span>

    public int bold([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2494">Parameters</span></span>

<span data-ttu-id="07b6d-2495">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2495">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2496">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2496">Return Value</span></span>

<span data-ttu-id="07b6d-2497">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2497">An integer value between zero and nine, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2498">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2498">Remarks</span></span>

<span data-ttu-id="07b6d-2499">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2499">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="07b6d-2500">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2500">0 Use the default font weight.</span></span>
-   <span data-ttu-id="07b6d-2501">1 シン。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2501">1 Thin.</span></span>
-   <span data-ttu-id="07b6d-2502">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2502">2 Extra-light.</span></span>
-   <span data-ttu-id="07b6d-2503">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2503">3 Light.</span></span>
-   <span data-ttu-id="07b6d-2504">4 標準。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2504">4 Normal.</span></span>
-   <span data-ttu-id="07b6d-2505">5 中。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2505">5 Medium.</span></span>
-   <span data-ttu-id="07b6d-2506">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2506">6 Semibold.</span></span>
-   <span data-ttu-id="07b6d-2507">7 太字。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2507">7 Bold.</span></span>
-   <span data-ttu-id="07b6d-2508">8 極太。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2508">8 Extra-bold.</span></span>
-   <span data-ttu-id="07b6d-2509">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2509">9 Heavy.</span></span>

### <a name="method-border"></a><span data-ttu-id="07b6d-2510">メソッド border</span><span class="sxs-lookup"><span data-stu-id="07b6d-2510">Method border</span></span>

<span data-ttu-id="07b6d-2511">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2511">Gets or sets the style of the borderline of the control.</span></span>

    public int border([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2512">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2512">Parameters</span></span>

<span data-ttu-id="07b6d-2513">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2513">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2514">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2514">Return Value</span></span>

<span data-ttu-id="07b6d-2515">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2515">An integer between zero and four, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2516">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2516">Remarks</span></span>

<span data-ttu-id="07b6d-2517">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2517">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="07b6d-2518">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2518">Value.</span></span> | <span data-ttu-id="07b6d-2519">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2519">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="07b6d-2520">0</span><span class="sxs-lookup"><span data-stu-id="07b6d-2520">0</span></span>      | <span data-ttu-id="07b6d-2521">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2521">Auto.</span></span>        |
| <span data-ttu-id="07b6d-2522">1</span><span class="sxs-lookup"><span data-stu-id="07b6d-2522">1</span></span>      | <span data-ttu-id="07b6d-2523">3D。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2523">3D.</span></span>          |
| <span data-ttu-id="07b6d-2524">2</span><span class="sxs-lookup"><span data-stu-id="07b6d-2524">2</span></span>      | <span data-ttu-id="07b6d-2525">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2525">Single line.</span></span> |
| <span data-ttu-id="07b6d-2526">3</span><span class="sxs-lookup"><span data-stu-id="07b6d-2526">3</span></span>      | <span data-ttu-id="07b6d-2527">均一。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2527">Flat.</span></span>        |
| <span data-ttu-id="07b6d-2528">4</span><span class="sxs-lookup"><span data-stu-id="07b6d-2528">4</span></span>      | <span data-ttu-id="07b6d-2529">なし。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2529">None.</span></span>        |

### <a name="method-buttondisplay"></a><span data-ttu-id="07b6d-2530">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="07b6d-2530">Method buttonDisplay</span></span>

<span data-ttu-id="07b6d-2531">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2531">Gets or sets the appearance of the button control.</span></span>

    public int buttonDisplay([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2532">Parameters</span></span>

<span data-ttu-id="07b6d-2533">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2533">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2534">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2534">Return Value</span></span>

<span data-ttu-id="07b6d-2535">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2535">An integer between zero and five, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2536">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2536">Remarks</span></span>

<span data-ttu-id="07b6d-2537">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2537">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="07b6d-2538">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2538">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="07b6d-2539">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2539">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="07b6d-2540">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2540">Value.</span></span> | <span data-ttu-id="07b6d-2541">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2541">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="07b6d-2542">0</span><span class="sxs-lookup"><span data-stu-id="07b6d-2542">0</span></span>      | <span data-ttu-id="07b6d-2543">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2543">Text only.</span></span>                                                       |
| <span data-ttu-id="07b6d-2544">1</span><span class="sxs-lookup"><span data-stu-id="07b6d-2544">1</span></span>      | <span data-ttu-id="07b6d-2545">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2545">Image Only.</span></span>                                                      |
| <span data-ttu-id="07b6d-2546">2</span><span class="sxs-lookup"><span data-stu-id="07b6d-2546">2</span></span>      | <span data-ttu-id="07b6d-2547">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2547">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="07b6d-2548">3</span><span class="sxs-lookup"><span data-stu-id="07b6d-2548">3</span></span>      | <span data-ttu-id="07b6d-2549">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2549">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="07b6d-2550">4</span><span class="sxs-lookup"><span data-stu-id="07b6d-2550">4</span></span>      | <span data-ttu-id="07b6d-2551">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2551">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="07b6d-2552">5</span><span class="sxs-lookup"><span data-stu-id="07b6d-2552">5</span></span>      | <span data-ttu-id="07b6d-2553">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2553">Text and image; the image is displayed to the right of the text.</span></span> |

### <a name="method-calccontrolsize"></a><span data-ttu-id="07b6d-2554">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-2554">Method calcControlSize</span></span>

<span data-ttu-id="07b6d-2555">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2555">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2556">Parameters</span></span>

<span data-ttu-id="07b6d-2557">chars</span><span class="sxs-lookup"><span data-stu-id="07b6d-2557">chars</span></span>  
<span data-ttu-id="07b6d-2558">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2558">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2559">明細行</span><span class="sxs-lookup"><span data-stu-id="07b6d-2559">lines</span></span>  
<span data-ttu-id="07b6d-2560">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2560">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2561">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2561">Return Value</span></span>

<span data-ttu-id="07b6d-2562">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2562">The container that holds the width and height.</span></span>

### <a name="method-caption"></a><span data-ttu-id="07b6d-2563">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="07b6d-2563">Method caption</span></span>

<span data-ttu-id="07b6d-2564">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2564">Gets or set the caption of the control.</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2565">Parameters</span></span>

<span data-ttu-id="07b6d-2566">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2566">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2567">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2567">Return Value</span></span>

<span data-ttu-id="07b6d-2568">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2568">The string that is used as the caption of the control.</span></span>

### <a name="method-characterset"></a><span data-ttu-id="07b6d-2569">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="07b6d-2569">Method characterSet</span></span>

<span data-ttu-id="07b6d-2570">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2570">Gets or sets the character set of the font.</span></span>

    public int characterSet([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2571">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2571">Parameters</span></span>

<span data-ttu-id="07b6d-2572">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2572">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2573">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2573">Return Value</span></span>

<span data-ttu-id="07b6d-2574">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2574">An integer value that indicates the character set of the font.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2575">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2575">Remarks</span></span>

<span data-ttu-id="07b6d-2576">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2576">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="07b6d-2577">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2577">Value.</span></span> | <span data-ttu-id="07b6d-2578">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2578">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="07b6d-2579">0</span><span class="sxs-lookup"><span data-stu-id="07b6d-2579">0</span></span>      | <span data-ttu-id="07b6d-2580">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2580">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="07b6d-2581">1</span><span class="sxs-lookup"><span data-stu-id="07b6d-2581">1</span></span>      | <span data-ttu-id="07b6d-2582">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2582">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="07b6d-2583">2</span><span class="sxs-lookup"><span data-stu-id="07b6d-2583">2</span></span>      | <span data-ttu-id="07b6d-2584">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2584">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="07b6d-2585">77</span><span class="sxs-lookup"><span data-stu-id="07b6d-2585">77</span></span>     | <span data-ttu-id="07b6d-2586">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2586">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="07b6d-2587">128</span><span class="sxs-lookup"><span data-stu-id="07b6d-2587">128</span></span>    | <span data-ttu-id="07b6d-2588">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2588">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="07b6d-2589">129</span><span class="sxs-lookup"><span data-stu-id="07b6d-2589">129</span></span>    | <span data-ttu-id="07b6d-2590">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2590">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="07b6d-2591">134</span><span class="sxs-lookup"><span data-stu-id="07b6d-2591">134</span></span>    | <span data-ttu-id="07b6d-2592">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2592">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="07b6d-2593">136</span><span class="sxs-lookup"><span data-stu-id="07b6d-2593">136</span></span>    | <span data-ttu-id="07b6d-2594">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2594">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="07b6d-2595">161</span><span class="sxs-lookup"><span data-stu-id="07b6d-2595">161</span></span>    | <span data-ttu-id="07b6d-2596">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2596">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="07b6d-2597">162</span><span class="sxs-lookup"><span data-stu-id="07b6d-2597">162</span></span>    | <span data-ttu-id="07b6d-2598">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2598">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="07b6d-2599">163</span><span class="sxs-lookup"><span data-stu-id="07b6d-2599">163</span></span>    | <span data-ttu-id="07b6d-2600">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2600">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="07b6d-2601">186</span><span class="sxs-lookup"><span data-stu-id="07b6d-2601">186</span></span>    | <span data-ttu-id="07b6d-2602">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2602">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="07b6d-2603">204</span><span class="sxs-lookup"><span data-stu-id="07b6d-2603">204</span></span>    | <span data-ttu-id="07b6d-2604">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2604">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="07b6d-2605">238</span><span class="sxs-lookup"><span data-stu-id="07b6d-2605">238</span></span>    | <span data-ttu-id="07b6d-2606">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2606">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="07b6d-2607">255</span><span class="sxs-lookup"><span data-stu-id="07b6d-2607">255</span></span>    | <span data-ttu-id="07b6d-2608">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2608">OEM\_CHARSET</span></span>         |

<span data-ttu-id="07b6d-2609">次のテーブルの値は、韓国語版 msCoNameWindows の値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2609">The value in the following table is for the Korean language edition of msCoNameWindows.</span></span>

| <span data-ttu-id="07b6d-2610">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2610">Value.</span></span> | <span data-ttu-id="07b6d-2611">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2611">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="07b6d-2612">130</span><span class="sxs-lookup"><span data-stu-id="07b6d-2612">130</span></span>    | <span data-ttu-id="07b6d-2613">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2613">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="07b6d-2614">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2614">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="07b6d-2615">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2615">Value.</span></span> | <span data-ttu-id="07b6d-2616">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2616">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="07b6d-2617">177</span><span class="sxs-lookup"><span data-stu-id="07b6d-2617">177</span></span>    | <span data-ttu-id="07b6d-2618">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2618">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="07b6d-2619">178</span><span class="sxs-lookup"><span data-stu-id="07b6d-2619">178</span></span>    | <span data-ttu-id="07b6d-2620">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2620">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="07b6d-2621">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2621">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="07b6d-2622">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2622">Value.</span></span> | <span data-ttu-id="07b6d-2623">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2623">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="07b6d-2624">222</span><span class="sxs-lookup"><span data-stu-id="07b6d-2624">222</span></span>    | <span data-ttu-id="07b6d-2625">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="07b6d-2625">THAI\_CHARSET</span></span> |

<span data-ttu-id="07b6d-2626">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2626">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="07b6d-2627">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2627">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="07b6d-2628">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2628">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

### <a name="method-colorscheme"></a><span data-ttu-id="07b6d-2629">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="07b6d-2629">Method colorScheme</span></span>

<span data-ttu-id="07b6d-2630">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2630">Gets or sets the color scheme of the control.</span></span>

    public int colorScheme([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2631">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2631">Parameters</span></span>

<span data-ttu-id="07b6d-2632">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2632">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2633">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2633">Return Value</span></span>

<span data-ttu-id="07b6d-2634">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2634">An integer between zero and two, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2635">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2635">Remarks</span></span>

<span data-ttu-id="07b6d-2636">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2636">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="07b6d-2637">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2637">Value.</span></span> | <span data-ttu-id="07b6d-2638">スタイル。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2638">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="07b6d-2639">0</span><span class="sxs-lookup"><span data-stu-id="07b6d-2639">0</span></span>      | <span data-ttu-id="07b6d-2640">既定。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2640">Default.</span></span>               |
| <span data-ttu-id="07b6d-2641">1</span><span class="sxs-lookup"><span data-stu-id="07b6d-2641">1</span></span>      | <span data-ttu-id="07b6d-2642">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2642">The Windows palette.</span></span>   |
| <span data-ttu-id="07b6d-2643">2</span><span class="sxs-lookup"><span data-stu-id="07b6d-2643">2</span></span>      | <span data-ttu-id="07b6d-2644">真の配色。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2644">The true-color scheme.</span></span> |

### <a name="method-configurationkey"></a><span data-ttu-id="07b6d-2645">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="07b6d-2645">Method configurationKey</span></span>

<span data-ttu-id="07b6d-2646">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2646">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2647">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2647">Parameters</span></span>

<span data-ttu-id="07b6d-2648">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2648">value</span></span>  
<span data-ttu-id="07b6d-2649">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2649">The ID of the configuration key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2650">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2650">Return Value</span></span>

<span data-ttu-id="07b6d-2651">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2651">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2652">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2652">Remarks</span></span>

<span data-ttu-id="07b6d-2653">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2653">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="07b6d-2654">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2654">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="07b6d-2655">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-2655">Method configurationKeyEx</span></span>

<span data-ttu-id="07b6d-2656">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2656">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2657">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2657">Return Value</span></span>

<span data-ttu-id="07b6d-2658">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2658">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2659">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2659">Remarks</span></span>

<span data-ttu-id="07b6d-2660">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2660">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="07b6d-2661">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2661">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="07b6d-2662">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2662">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-copycallerquery"></a><span data-ttu-id="07b6d-2663">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="07b6d-2663">Method copyCallerQuery</span></span>

    public int copyCallerQuery([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2664">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2664">Parameters</span></span>

<span data-ttu-id="07b6d-2665">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2665">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2666">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2666">Return Value</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="07b6d-2667">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="07b6d-2667">Method countryRegionCodes</span></span>

<span data-ttu-id="07b6d-2668">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2668">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2669">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2669">Parameters</span></span>

<span data-ttu-id="07b6d-2670">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2670">value</span></span>  
<span data-ttu-id="07b6d-2671">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2671">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2672">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2672">Return Value</span></span>

<span data-ttu-id="07b6d-2673">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2673">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-countryregioncontextfield"></a><span data-ttu-id="07b6d-2674">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="07b6d-2674">Method countryRegionContextField</span></span>

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2675">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2675">Parameters</span></span>

<span data-ttu-id="07b6d-2676">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2676">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2677">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2677">Return Value</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="07b6d-2678">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="07b6d-2678">Method dataRelationPath</span></span>

<span data-ttu-id="07b6d-2679">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2679">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2680">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2680">Parameters</span></span>

<span data-ttu-id="07b6d-2681">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2681">value</span></span>  
<span data-ttu-id="07b6d-2682">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2682">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2683">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2683">Return Value</span></span>

<span data-ttu-id="07b6d-2684">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2684">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2685">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2685">Remarks</span></span>

<span data-ttu-id="07b6d-2686">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2686">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="07b6d-2687">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2687">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-datasource"></a><span data-ttu-id="07b6d-2688">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-2688">Method dataSource</span></span>

<span data-ttu-id="07b6d-2689">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2689">Gets or sets a data source to be used by the control or the form.</span></span>

    public int dataSource([AnyType value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2690">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2690">Parameters</span></span>

<span data-ttu-id="07b6d-2691">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2691">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2692">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2692">Return Value</span></span>

<span data-ttu-id="07b6d-2693">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2693">The identifier of the data source to be used.</span></span>

### <a name="method-defaultbutton"></a><span data-ttu-id="07b6d-2694">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="07b6d-2694">Method defaultButton</span></span>

<span data-ttu-id="07b6d-2695">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2695">Determines whether the button should be the default button in the form.</span></span>

    public boolean defaultButton([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2696">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2696">Parameters</span></span>

<span data-ttu-id="07b6d-2697">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2697">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2698">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2698">Return Value</span></span>

<span data-ttu-id="07b6d-2699">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2699">true if the button should be the default button; otherwise, false.</span></span>

### <a name="method-disabledimage"></a><span data-ttu-id="07b6d-2700">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="07b6d-2700">Method disabledImage</span></span>

<span data-ttu-id="07b6d-2701">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2701">Gets or sets the disabled image of the button.</span></span>

    public str disabledImage([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2702">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2702">Parameters</span></span>

<span data-ttu-id="07b6d-2703">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2703">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2704">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2704">Return Value</span></span>

<span data-ttu-id="07b6d-2705">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2705">The full name of an image file.</span></span> <span data-ttu-id="07b6d-2706">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2706">The system supports all of the GDI-supported image formats.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2707">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2707">Remarks</span></span>

<span data-ttu-id="07b6d-2708">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2708">This property has precedence over the disabledResource property.</span></span> <span data-ttu-id="07b6d-2709">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2709">It is used if both of these properties are set.</span></span>

### <a name="method-disabledimagelocation"></a><span data-ttu-id="07b6d-2710">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="07b6d-2710">Method disabledImageLocation</span></span>

    public int disabledImageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2711">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2711">Parameters</span></span>

<span data-ttu-id="07b6d-2712">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2712">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2713">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2713">Return Value</span></span>

### <a name="method-disabledresource"></a><span data-ttu-id="07b6d-2714">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="07b6d-2714">Method disabledResource</span></span>

<span data-ttu-id="07b6d-2715">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2715">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

    public int disabledResource([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2716">Parameters</span></span>

<span data-ttu-id="07b6d-2717">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2717">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2718">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2718">Return Value</span></span>

<span data-ttu-id="07b6d-2719">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2719">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="07b6d-2720">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2720">Both icon and bitmap images are supported.</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="07b6d-2721">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="07b6d-2721">Method displayTarget</span></span>

<span data-ttu-id="07b6d-2722">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2722">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2723">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2723">Parameters</span></span>

<span data-ttu-id="07b6d-2724">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2724">value</span></span>  
<span data-ttu-id="07b6d-2725">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2725">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2726">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2726">Return Value</span></span>

<span data-ttu-id="07b6d-2727">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2727">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="07b6d-2728">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="07b6d-2728">Method dragDrop</span></span>

<span data-ttu-id="07b6d-2729">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2729">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2730">Parameters</span></span>

<span data-ttu-id="07b6d-2731">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2731">value</span></span>  
<span data-ttu-id="07b6d-2732">ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2732">An Integer data type that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2733">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2733">Return Value</span></span>

<span data-ttu-id="07b6d-2734">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2734">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2735">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2735">Remarks</span></span>

<span data-ttu-id="07b6d-2736">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2736">Use the dragLeave , the dragOver, and the dragOverEx to specify the behavior.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="07b6d-2737">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="07b6d-2737">Method dragOver</span></span>

<span data-ttu-id="07b6d-2738">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2738">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2739">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2739">Parameters</span></span>

<span data-ttu-id="07b6d-2740">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-2740">dragSource</span></span>  
<span data-ttu-id="07b6d-2741">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2741">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2742">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-2742">dragMode</span></span>  
<span data-ttu-id="07b6d-2743">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2743">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2744">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-2744">x</span></span>  
<span data-ttu-id="07b6d-2745">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2745">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2746">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-2746">y</span></span>  
<span data-ttu-id="07b6d-2747">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2747">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2748">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2748">Return Value</span></span>

<span data-ttu-id="07b6d-2749">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2749">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="07b6d-2750">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-2750">Method dragOverEx</span></span>

<span data-ttu-id="07b6d-2751">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2751">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2752">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2752">Parameters</span></span>

<span data-ttu-id="07b6d-2753">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-2753">dragSource</span></span>  
<span data-ttu-id="07b6d-2754">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2754">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2755">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-2755">dragMode</span></span>  
<span data-ttu-id="07b6d-2756">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2756">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2757">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-2757">x</span></span>  
<span data-ttu-id="07b6d-2758">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2758">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2759">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-2759">y</span></span>  
<span data-ttu-id="07b6d-2760">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2760">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2761">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2761">Return Value</span></span>

<span data-ttu-id="07b6d-2762">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2762">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="07b6d-2763">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="07b6d-2763">Method dragText</span></span>

<span data-ttu-id="07b6d-2764">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2764">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2765">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2765">Return Value</span></span>

<span data-ttu-id="07b6d-2766">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2766">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="07b6d-2767">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="07b6d-2767">Method enabled</span></span>

<span data-ttu-id="07b6d-2768">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2768">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2769">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2769">Parameters</span></span>

<span data-ttu-id="07b6d-2770">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2770">value</span></span>  
<span data-ttu-id="07b6d-2771">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2771">A Boolean value that specifies whether the control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2772">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2772">Return Value</span></span>

<span data-ttu-id="07b6d-2773">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2773">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2774">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2774">Remarks</span></span>

<span data-ttu-id="07b6d-2775">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2775">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="07b6d-2776">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2776">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="07b6d-2777">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2777">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-font"></a><span data-ttu-id="07b6d-2778">メソッド font</span><span class="sxs-lookup"><span data-stu-id="07b6d-2778">Method font</span></span>

<span data-ttu-id="07b6d-2779">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2779">Gets or sets the name of the font for the control to use.</span></span>

    public str font([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2780">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2780">Parameters</span></span>

<span data-ttu-id="07b6d-2781">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2781">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2782">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2782">Return Value</span></span>

<span data-ttu-id="07b6d-2783">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2783">The name of the font to use, such as Tahoma or Verdana.</span></span>

### <a name="method-fontsize"></a><span data-ttu-id="07b6d-2784">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-2784">Method fontSize</span></span>

<span data-ttu-id="07b6d-2785">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2785">Gets or sets the size of the font for the control to use.</span></span>

    public int fontSize([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2786">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2786">Parameters</span></span>

<span data-ttu-id="07b6d-2787">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2787">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2788">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2788">Return Value</span></span>

<span data-ttu-id="07b6d-2789">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2789">The height of the font in points.</span></span>

### <a name="method-forcedtooverflow"></a><span data-ttu-id="07b6d-2790">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="07b6d-2790">Method forcedToOverflow</span></span>

    public boolean forcedToOverflow([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2791">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2791">Parameters</span></span>

<span data-ttu-id="07b6d-2792">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2792">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2793">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2793">Return Value</span></span>

### <a name="method-foregroundcolor"></a><span data-ttu-id="07b6d-2794">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="07b6d-2794">Method foregroundColor</span></span>

<span data-ttu-id="07b6d-2795">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2795">Gets or sets the text color for the control to use.</span></span>

    public int foregroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2796">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2796">Parameters</span></span>

<span data-ttu-id="07b6d-2797">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2797">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2798">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2798">Return Value</span></span>

<span data-ttu-id="07b6d-2799">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2799">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2800">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2800">Remarks</span></span>

<span data-ttu-id="07b6d-2801">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2801">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="07b6d-2802">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2802">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="07b6d-2803">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2803">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="07b6d-2804">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2804">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="07b6d-2805">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2805">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="07b6d-2806">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2806">The maximum value for a single byte is 255.</span></span>

### <a name="method-formviewoption"></a><span data-ttu-id="07b6d-2807">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="07b6d-2807">Method formViewOption</span></span>

    public int formViewOption([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2808">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2808">Parameters</span></span>

<span data-ttu-id="07b6d-2809">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2809">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2810">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2810">Return Value</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="07b6d-2811">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="07b6d-2811">Method hasChanged</span></span>

<span data-ttu-id="07b6d-2812">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2812">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2813">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2813">Parameters</span></span>

<span data-ttu-id="07b6d-2814">val</span><span class="sxs-lookup"><span data-stu-id="07b6d-2814">val</span></span>  
<span data-ttu-id="07b6d-2815">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2815">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2816">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2816">Return Value</span></span>

<span data-ttu-id="07b6d-2817">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2817">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="07b6d-2818">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="07b6d-2818">Method hasUserSetting</span></span>

<span data-ttu-id="07b6d-2819">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2819">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2820">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2820">Return Value</span></span>

<span data-ttu-id="07b6d-2821">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2821">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="07b6d-2822">メソッド height</span><span class="sxs-lookup"><span data-stu-id="07b6d-2822">Method height</span></span>

<span data-ttu-id="07b6d-2823">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2823">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2824">Parameters</span></span>

<span data-ttu-id="07b6d-2825">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2825">value</span></span>  
<span data-ttu-id="07b6d-2826">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2826">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2827">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-2827">mode</span></span>  
<span data-ttu-id="07b6d-2828">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2828">An Integer that indicates how the height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2829">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2829">Return Value</span></span>

<span data-ttu-id="07b6d-2830">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2830">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2831">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2831">Remarks</span></span>

<span data-ttu-id="07b6d-2832">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2832">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="07b6d-2833">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-2833">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="07b6d-2834">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2834">Mode.</span></span>            | <span data-ttu-id="07b6d-2835">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2835">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-2836">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2836">-1 Exact.</span></span>        | <span data-ttu-id="07b6d-2837">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2837">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-2838">0 自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2838">0 Auto.</span></span>          | <span data-ttu-id="07b6d-2839">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2839">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-2840">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2840">1 Column height.</span></span> | <span data-ttu-id="07b6d-2841">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2841">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="07b6d-2842">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2842">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="07b6d-2843">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-2843">Method heightMode</span></span>

<span data-ttu-id="07b6d-2844">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2844">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2845">Parameters</span></span>

<span data-ttu-id="07b6d-2846">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2846">value</span></span>  
<span data-ttu-id="07b6d-2847">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2847">An integer value that indicates how control height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2848">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2848">Return Value</span></span>

<span data-ttu-id="07b6d-2849">計算モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2849">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2850">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2850">Remarks</span></span>

<span data-ttu-id="07b6d-2851">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-2851">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="07b6d-2852">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2852">Mode.</span></span>          | <span data-ttu-id="07b6d-2853">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2853">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-2854">正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2854">Exact.</span></span>         | <span data-ttu-id="07b6d-2855">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2855">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-2856">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2856">Auto.</span></span>          | <span data-ttu-id="07b6d-2857">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2857">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-2858">列の高さ</span><span class="sxs-lookup"><span data-stu-id="07b6d-2858">Column height.</span></span> | <span data-ttu-id="07b6d-2859">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2859">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="07b6d-2860">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2860">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="07b6d-2861">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-2861">Method heightValue</span></span>

<span data-ttu-id="07b6d-2862">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2862">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2863">Parameters</span></span>

<span data-ttu-id="07b6d-2864">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2864">value</span></span>  
<span data-ttu-id="07b6d-2865">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2865">An Integer that specifies the height in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2866">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2866">Return Value</span></span>

<span data-ttu-id="07b6d-2867">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2867">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2868">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2868">Remarks</span></span>

<span data-ttu-id="07b6d-2869">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2869">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="07b6d-2870">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="07b6d-2870">Method helpField</span></span>

<span data-ttu-id="07b6d-2871">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2871">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2872">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2872">Return Value</span></span>

<span data-ttu-id="07b6d-2873">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2873">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2874">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2874">Remarks</span></span>

<span data-ttu-id="07b6d-2875">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2875">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="07b6d-2876">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2876">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="07b6d-2877">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="07b6d-2877">Method helpText</span></span>

<span data-ttu-id="07b6d-2878">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2878">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2879">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2879">Parameters</span></span>

<span data-ttu-id="07b6d-2880">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2880">value</span></span>  
<span data-ttu-id="07b6d-2881">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2881">The value that is assigned as the Help text for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2882">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2882">Return Value</span></span>

<span data-ttu-id="07b6d-2883">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2883">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2884">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2884">Remarks</span></span>

<span data-ttu-id="07b6d-2885">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2885">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="07b6d-2886">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2886">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="07b6d-2887">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="07b6d-2887">Method hierarchyParent</span></span>

<span data-ttu-id="07b6d-2888">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2888">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2889">Parameters</span></span>

<span data-ttu-id="07b6d-2890">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2890">value</span></span>  
<span data-ttu-id="07b6d-2891">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2891">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2892">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2892">Return Value</span></span>

<span data-ttu-id="07b6d-2893">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2893">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="07b6d-2894">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="07b6d-2894">Method hWnd</span></span>

<span data-ttu-id="07b6d-2895">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2895">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2896">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2896">Return Value</span></span>

<span data-ttu-id="07b6d-2897">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2897">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2898">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2898">Remarks</span></span>

<span data-ttu-id="07b6d-2899">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2899">The handle can be used with the Windows API.</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="07b6d-2900">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="07b6d-2900">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2901">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2901">Parameters</span></span>

<span data-ttu-id="07b6d-2902">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2902">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2903">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2903">Return Value</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="07b6d-2904">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="07b6d-2904">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2905">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2905">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="07b6d-2906">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="07b6d-2906">Method isDisplayed</span></span>

<span data-ttu-id="07b6d-2907">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2907">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2908">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2908">Return Value</span></span>

<span data-ttu-id="07b6d-2909">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2909">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2910">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2910">Remarks</span></span>

<span data-ttu-id="07b6d-2911">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2911">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="07b6d-2912">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="07b6d-2912">Method isRestricted</span></span>

<span data-ttu-id="07b6d-2913">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2913">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2914">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2914">Return Value</span></span>

<span data-ttu-id="07b6d-2915">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2915">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="07b6d-2916">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="07b6d-2916">Method isUserSetupEnabled</span></span>

<span data-ttu-id="07b6d-2917">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2917">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2918">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2918">Parameters</span></span>

<span data-ttu-id="07b6d-2919">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="07b6d-2919">neededSetupRights</span></span>  
<span data-ttu-id="07b6d-2920">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2920">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2921">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2921">Return Value</span></span>

<span data-ttu-id="07b6d-2922">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2922">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2923">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2923">Remarks</span></span>

<span data-ttu-id="07b6d-2924">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2924">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-2925">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="07b6d-2925">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="07b6d-2926">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2926">No changes can be made to the control.</span></span> <span data-ttu-id="07b6d-2927">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2927">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="07b6d-2928">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="07b6d-2928">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="07b6d-2929">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2929">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="07b6d-2930">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2930">The user cannot move the control.</span></span>   |
| <span data-ttu-id="07b6d-2931">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="07b6d-2931">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="07b6d-2932">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2932">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="07b6d-2933">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2933">The user can also move the control.</span></span> |

<span data-ttu-id="07b6d-2934">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2934">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="method-italic"></a><span data-ttu-id="07b6d-2935">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="07b6d-2935">Method italic</span></span>

    public boolean italic([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2936">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2936">Parameters</span></span>

<span data-ttu-id="07b6d-2937">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2937">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2938">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2938">Return Value</span></span>

### <a name="method-keytip"></a><span data-ttu-id="07b6d-2939">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="07b6d-2939">Method keyTip</span></span>

    public str keyTip([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2940">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2940">Parameters</span></span>

<span data-ttu-id="07b6d-2941">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2941">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2942">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2942">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="07b6d-2943">メソッド left</span><span class="sxs-lookup"><span data-stu-id="07b6d-2943">Method left</span></span>

<span data-ttu-id="07b6d-2944">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2944">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2945">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2945">Parameters</span></span>

<span data-ttu-id="07b6d-2946">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2946">value</span></span>  
<span data-ttu-id="07b6d-2947">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2947">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2948">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-2948">mode</span></span>  
<span data-ttu-id="07b6d-2949">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2949">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2950">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2950">Return Value</span></span>

<span data-ttu-id="07b6d-2951">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2951">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="07b6d-2952">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-2952">Method leftMode</span></span>

<span data-ttu-id="07b6d-2953">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2953">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2954">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2954">Parameters</span></span>

<span data-ttu-id="07b6d-2955">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2955">value</span></span>  
<span data-ttu-id="07b6d-2956">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2956">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2957">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2957">Return Value</span></span>

<span data-ttu-id="07b6d-2958">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2958">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="07b6d-2959">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-2959">Method leftValue</span></span>

<span data-ttu-id="07b6d-2960">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2960">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2961">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2961">Parameters</span></span>

<span data-ttu-id="07b6d-2962">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2962">value</span></span>  
<span data-ttu-id="07b6d-2963">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2963">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2964">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2964">Return Value</span></span>

<span data-ttu-id="07b6d-2965">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2965">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="07b6d-2966">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="07b6d-2966">Method markAsUserAdd</span></span>

<span data-ttu-id="07b6d-2967">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2967">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2968">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2968">Parameters</span></span>

<span data-ttu-id="07b6d-2969">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2969">value</span></span>  
<span data-ttu-id="07b6d-2970">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2970">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2971">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2971">Return Value</span></span>

<span data-ttu-id="07b6d-2972">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2972">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-menufunction"></a><span data-ttu-id="07b6d-2973">メソッド menufunction</span><span class="sxs-lookup"><span data-stu-id="07b6d-2973">Method menufunction</span></span>

    public xMenuFunction menufunction()

#### <a name="return-value"></a><span data-ttu-id="07b6d-2974">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2974">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="07b6d-2975">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="07b6d-2975">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2976">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2976">Parameters</span></span>

<span data-ttu-id="07b6d-2977">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2977">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2978">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2978">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="07b6d-2979">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="07b6d-2979">Method menuItemType</span></span>

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-2980">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2980">Parameters</span></span>

<span data-ttu-id="07b6d-2981">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2981">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-2982">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2982">Return Value</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="07b6d-2983">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="07b6d-2983">Method mouseDblClick</span></span>

<span data-ttu-id="07b6d-2984">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2984">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-2985">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-2985">Parameters</span></span>

<span data-ttu-id="07b6d-2986">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-2986">x</span></span>  
<span data-ttu-id="07b6d-2987">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2987">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2988">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-2988">y</span></span>  
<span data-ttu-id="07b6d-2989">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2989">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2990">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-2990">button</span></span>  
<span data-ttu-id="07b6d-2991">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2991">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2992">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-2992">Ctrl</span></span>  
<span data-ttu-id="07b6d-2993">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2993">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-2994">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-2994">Shift</span></span>  
<span data-ttu-id="07b6d-2995">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2995">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-2996">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-2996">Return Value</span></span>

<span data-ttu-id="07b6d-2997">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2997">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-2998">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-2998">Remarks</span></span>

<span data-ttu-id="07b6d-2999">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-2999">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="07b6d-3000">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="07b6d-3000">Method mouseDown</span></span>

<span data-ttu-id="07b6d-3001">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3001">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3002">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3002">Parameters</span></span>

<span data-ttu-id="07b6d-3003">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3003">x</span></span>  
<span data-ttu-id="07b6d-3004">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3004">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3005">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3005">y</span></span>  
<span data-ttu-id="07b6d-3006">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3006">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3007">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-3007">button</span></span>  
<span data-ttu-id="07b6d-3008">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3008">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3009">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3009">Ctrl</span></span>  
<span data-ttu-id="07b6d-3010">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3010">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3011">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-3011">Shift</span></span>  
<span data-ttu-id="07b6d-3012">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3012">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3013">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3013">Return Value</span></span>

<span data-ttu-id="07b6d-3014">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3014">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3015">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3015">Remarks</span></span>

<span data-ttu-id="07b6d-3016">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3016">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="07b6d-3017">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3017">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="07b6d-3018">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="07b6d-3018">Method mouseMove</span></span>

<span data-ttu-id="07b6d-3019">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3019">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3020">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3020">Parameters</span></span>

<span data-ttu-id="07b6d-3021">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3021">x</span></span>  
<span data-ttu-id="07b6d-3022">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3022">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3023">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3023">y</span></span>  
<span data-ttu-id="07b6d-3024">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3024">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3025">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-3025">button</span></span>  
<span data-ttu-id="07b6d-3026">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3026">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3027">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3027">Ctrl</span></span>  
<span data-ttu-id="07b6d-3028">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3028">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3029">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-3029">Shift</span></span>  
<span data-ttu-id="07b6d-3030">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3030">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3031">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3031">Return Value</span></span>

<span data-ttu-id="07b6d-3032">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3032">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3033">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3033">Remarks</span></span>

<span data-ttu-id="07b6d-3034">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3034">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="07b6d-3035">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="07b6d-3035">Method mouseUp</span></span>

<span data-ttu-id="07b6d-3036">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3036">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3037">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3037">Parameters</span></span>

<span data-ttu-id="07b6d-3038">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3038">x</span></span>  
<span data-ttu-id="07b6d-3039">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3039">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3040">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3040">y</span></span>  
<span data-ttu-id="07b6d-3041">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3041">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3042">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-3042">button</span></span>  
<span data-ttu-id="07b6d-3043">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3043">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3044">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3044">Ctrl</span></span>  
<span data-ttu-id="07b6d-3045">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3045">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3046">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-3046">Shift</span></span>  
<span data-ttu-id="07b6d-3047">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3047">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3048">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3048">Return Value</span></span>

<span data-ttu-id="07b6d-3049">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3049">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3050">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3050">Remarks</span></span>

<span data-ttu-id="07b6d-3051">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3051">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="07b6d-3052">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3052">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="07b6d-3053">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="07b6d-3053">Method multiSelect</span></span>

    public int multiSelect([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3054">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3054">Parameters</span></span>

<span data-ttu-id="07b6d-3055">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3055">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3056">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3056">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="07b6d-3057">メソッド名</span><span class="sxs-lookup"><span data-stu-id="07b6d-3057">Method name</span></span>

<span data-ttu-id="07b6d-3058">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3058">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3059">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3059">Parameters</span></span>

<span data-ttu-id="07b6d-3060">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3060">value</span></span>  
<span data-ttu-id="07b6d-3061">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3061">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3062">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3062">Return Value</span></span>

<span data-ttu-id="07b6d-3063">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3063">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3064">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3064">Remarks</span></span>

<span data-ttu-id="07b6d-3065">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3065">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="07b6d-3066">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3066">It must begin with a letter.</span></span>
-   <span data-ttu-id="07b6d-3067">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3067">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="07b6d-3068">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3068">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="07b6d-3069">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3069">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="07b6d-3070">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3070">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="07b6d-3071">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="07b6d-3071">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3072">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3072">Parameters</span></span>

<span data-ttu-id="07b6d-3073">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3073">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3074">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3074">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="07b6d-3075">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="07b6d-3075">Method needsRecord</span></span>

    public int needsRecord([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3076">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3076">Parameters</span></span>

<span data-ttu-id="07b6d-3077">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3077">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3078">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3078">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="07b6d-3079">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="07b6d-3079">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3080">Parameters</span></span>

<span data-ttu-id="07b6d-3081">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3081">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3082">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3082">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="07b6d-3083">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="07b6d-3083">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3084">Parameters</span></span>

<span data-ttu-id="07b6d-3085">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3085">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3086">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3086">Return Value</span></span>

### <a name="method-openmode"></a><span data-ttu-id="07b6d-3087">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-3087">Method openMode</span></span>

    public int openMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3088">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3088">Parameters</span></span>

<span data-ttu-id="07b6d-3089">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3089">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3090">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3090">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="07b6d-3091">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="07b6d-3091">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="07b6d-3092">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3092">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="07b6d-3093">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="07b6d-3093">Method parameters</span></span>

<span data-ttu-id="07b6d-3094">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3094">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3095">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3095">Parameters</span></span>

<span data-ttu-id="07b6d-3096">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3096">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3097">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3097">Return Value</span></span>

<span data-ttu-id="07b6d-3098">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3098">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3099">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3099">Remarks</span></span>

<span data-ttu-id="07b6d-3100">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3100">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="07b6d-3101">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3101">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="07b6d-3102">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3102">Method parentControl</span></span>

<span data-ttu-id="07b6d-3103">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3103">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="07b6d-3104">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3104">Return Value</span></span>

<span data-ttu-id="07b6d-3105">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3105">The parent control for the control.</span></span>

### <a name="method-primary"></a><span data-ttu-id="07b6d-3106">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="07b6d-3106">Method primary</span></span>

    public boolean primary([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3107">Parameters</span></span>

<span data-ttu-id="07b6d-3108">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3108">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3109">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3109">Return Value</span></span>

### <a name="method-saverecord"></a><span data-ttu-id="07b6d-3110">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="07b6d-3110">Method saveRecord</span></span>

    public boolean saveRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3111">Parameters</span></span>

<span data-ttu-id="07b6d-3112">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3112">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3113">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3113">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="07b6d-3114">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="07b6d-3114">Method securityKey</span></span>

<span data-ttu-id="07b6d-3115">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3115">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3116">Parameters</span></span>

<span data-ttu-id="07b6d-3117">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3117">value</span></span>  
<span data-ttu-id="07b6d-3118">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3118">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3119">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3119">Return Value</span></span>

<span data-ttu-id="07b6d-3120">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3120">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-sendexternalcontext"></a><span data-ttu-id="07b6d-3121">メソッド sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="07b6d-3121">Method sendExternalContext</span></span>

    public boolean sendExternalContext([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3122">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3122">Parameters</span></span>

<span data-ttu-id="07b6d-3123">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3123">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3124">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3124">Return Value</span></span>

### <a name="method-shortkey"></a><span data-ttu-id="07b6d-3125">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="07b6d-3125">Method shortkey</span></span>

    public int shortkey([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3126">Parameters</span></span>

<span data-ttu-id="07b6d-3127">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3127">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3128">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3128">Return Value</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="07b6d-3129">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="07b6d-3129">Method showContextMenu</span></span>

<span data-ttu-id="07b6d-3130">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3130">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3131">Parameters</span></span>

<span data-ttu-id="07b6d-3132">menuHandle</span><span class="sxs-lookup"><span data-stu-id="07b6d-3132">menuHandle</span></span>  
<span data-ttu-id="07b6d-3133">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3133">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3134">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3134">Return Value</span></span>

<span data-ttu-id="07b6d-3135">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3135">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-showshortcut"></a><span data-ttu-id="07b6d-3136">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="07b6d-3136">Method showShortCut</span></span>

    public boolean showShortCut([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3137">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3137">Parameters</span></span>

<span data-ttu-id="07b6d-3138">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3138">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3139">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3139">Return Value</span></span>

### <a name="method-skip"></a><span data-ttu-id="07b6d-3140">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="07b6d-3140">Method skip</span></span>

<span data-ttu-id="07b6d-3141">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3141">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3142">Parameters</span></span>

<span data-ttu-id="07b6d-3143">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3143">value</span></span>  
<span data-ttu-id="07b6d-3144">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3144">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3145">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3145">Return Value</span></span>

<span data-ttu-id="07b6d-3146">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3146">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3147">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3147">Remarks</span></span>

<span data-ttu-id="07b6d-3148">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3148">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="method-sort"></a><span data-ttu-id="07b6d-3149">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="07b6d-3149">Method sort</span></span>

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3150">Parameters</span></span>

<span data-ttu-id="07b6d-3151">sortDirection</span><span class="sxs-lookup"><span data-stu-id="07b6d-3151">sortDirection</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3152">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3152">Return Value</span></span>

### <a name="method-style"></a><span data-ttu-id="07b6d-3153">メソッド style</span><span class="sxs-lookup"><span data-stu-id="07b6d-3153">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3154">Parameters</span></span>

<span data-ttu-id="07b6d-3155">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3155">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3156">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3156">Return Value</span></span>

### <a name="method-text"></a><span data-ttu-id="07b6d-3157">メソッド text</span><span class="sxs-lookup"><span data-stu-id="07b6d-3157">Method text</span></span>

    public str text([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3158">Parameters</span></span>

<span data-ttu-id="07b6d-3159">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3159">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3160">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3160">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="07b6d-3161">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="07b6d-3161">Method toolTip</span></span>

<span data-ttu-id="07b6d-3162">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3162">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="07b6d-3163">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3163">Return Value</span></span>

<span data-ttu-id="07b6d-3164">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3164">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3165">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3165">Remarks</span></span>

<span data-ttu-id="07b6d-3166">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3166">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="07b6d-3167">メソッド top</span><span class="sxs-lookup"><span data-stu-id="07b6d-3167">Method top</span></span>

<span data-ttu-id="07b6d-3168">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3168">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3169">Parameters</span></span>

<span data-ttu-id="07b6d-3170">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3170">value</span></span>  
<span data-ttu-id="07b6d-3171">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3171">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3172">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-3172">mode</span></span>  
<span data-ttu-id="07b6d-3173">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3173">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3174">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3174">Return Value</span></span>

<span data-ttu-id="07b6d-3175">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3175">The vertical position of the control in the form.</span></span>

### <a name="method-topmode"></a><span data-ttu-id="07b6d-3176">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-3176">Method topMode</span></span>

<span data-ttu-id="07b6d-3177">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3177">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3178">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3178">Parameters</span></span>

<span data-ttu-id="07b6d-3179">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3179">value</span></span>  
<span data-ttu-id="07b6d-3180">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3180">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3181">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3181">Return Value</span></span>

<span data-ttu-id="07b6d-3182">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3182">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="07b6d-3183">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-3183">Method topValue</span></span>

<span data-ttu-id="07b6d-3184">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3184">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3185">Parameters</span></span>

<span data-ttu-id="07b6d-3186">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3186">value</span></span>  
<span data-ttu-id="07b6d-3187">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3187">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3188">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3188">Return Value</span></span>

<span data-ttu-id="07b6d-3189">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3189">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="07b6d-3190">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="07b6d-3190">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3191">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3191">Parameters</span></span>

<span data-ttu-id="07b6d-3192">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3192">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3193">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3193">Return Value</span></span>

### <a name="method-underline"></a><span data-ttu-id="07b6d-3194">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="07b6d-3194">Method underline</span></span>

    public boolean underline([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3195">Parameters</span></span>

<span data-ttu-id="07b6d-3196">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3196">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3197">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3197">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="07b6d-3198">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="07b6d-3198">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3199">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3199">Parameters</span></span>

<span data-ttu-id="07b6d-3200">データ</span><span class="sxs-lookup"><span data-stu-id="07b6d-3200">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3201">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3201">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="07b6d-3202">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="07b6d-3202">Method userData</span></span>

<span data-ttu-id="07b6d-3203">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3203">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3204">Parameters</span></span>

<span data-ttu-id="07b6d-3205">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3205">value</span></span>  
<span data-ttu-id="07b6d-3206">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3206">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3207">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3207">Return Value</span></span>

<span data-ttu-id="07b6d-3208">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3208">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="07b6d-3209">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="07b6d-3209">Method userDataItem</span></span>

<span data-ttu-id="07b6d-3210">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3210">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3211">Parameters</span></span>

<span data-ttu-id="07b6d-3212">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3212">value</span></span>  
<span data-ttu-id="07b6d-3213">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3213">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3214">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3214">Return Value</span></span>

<span data-ttu-id="07b6d-3215">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3215">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="07b6d-3216">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="07b6d-3216">Method userDataItems</span></span>

<span data-ttu-id="07b6d-3217">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3217">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3218">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3218">Parameters</span></span>

<span data-ttu-id="07b6d-3219">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3219">value</span></span>  
<span data-ttu-id="07b6d-3220">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3220">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3221">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3221">Return Value</span></span>

<span data-ttu-id="07b6d-3222">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3222">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="07b6d-3223">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="07b6d-3223">Method userDisable</span></span>

<span data-ttu-id="07b6d-3224">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3224">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3225">Parameters</span></span>

<span data-ttu-id="07b6d-3226">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3226">value</span></span>  
<span data-ttu-id="07b6d-3227">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3227">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3228">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3228">Return Value</span></span>

<span data-ttu-id="07b6d-3229">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3229">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="07b6d-3230">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="07b6d-3230">Method userHeight</span></span>

<span data-ttu-id="07b6d-3231">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3231">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3232">Parameters</span></span>

<span data-ttu-id="07b6d-3233">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3233">value</span></span>  
<span data-ttu-id="07b6d-3234">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3234">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3235">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3235">Return Value</span></span>

<span data-ttu-id="07b6d-3236">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3236">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="07b6d-3237">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="07b6d-3237">Method userHide</span></span>

<span data-ttu-id="07b6d-3238">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3238">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3239">Parameters</span></span>

<span data-ttu-id="07b6d-3240">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3240">value</span></span>  
<span data-ttu-id="07b6d-3241">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3241">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3242">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3242">Return Value</span></span>

<span data-ttu-id="07b6d-3243">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3243">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3244">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3244">Remarks</span></span>

<span data-ttu-id="07b6d-3245">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3245">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="07b6d-3246">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3246">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="07b6d-3247">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3247">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="07b6d-3248">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="07b6d-3248">Method userOrgContainer</span></span>

<span data-ttu-id="07b6d-3249">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3249">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3250">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3250">Parameters</span></span>

<span data-ttu-id="07b6d-3251">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3251">value</span></span>  
<span data-ttu-id="07b6d-3252">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3252">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3253">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3253">Return Value</span></span>

<span data-ttu-id="07b6d-3254">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3254">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="07b6d-3255">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="07b6d-3255">Method userOrgSibling</span></span>

<span data-ttu-id="07b6d-3256">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3256">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3257">Parameters</span></span>

<span data-ttu-id="07b6d-3258">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3258">value</span></span>  
<span data-ttu-id="07b6d-3259">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3259">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3260">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3260">Return Value</span></span>

<span data-ttu-id="07b6d-3261">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3261">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="07b6d-3262">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="07b6d-3262">Method userPromptText</span></span>

<span data-ttu-id="07b6d-3263">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3263">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3264">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3264">Parameters</span></span>

<span data-ttu-id="07b6d-3265">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3265">value</span></span>  
<span data-ttu-id="07b6d-3266">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3266">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3267">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3267">Return Value</span></span>

<span data-ttu-id="07b6d-3268">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3268">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="07b6d-3269">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="07b6d-3269">Method userSecurityLevel</span></span>

<span data-ttu-id="07b6d-3270">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3270">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3271">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3271">Parameters</span></span>

<span data-ttu-id="07b6d-3272">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3272">value</span></span>  
<span data-ttu-id="07b6d-3273">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3273">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3274">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3274">Return Value</span></span>

<span data-ttu-id="07b6d-3275">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3275">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="07b6d-3276">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="07b6d-3276">Method userSkip</span></span>

<span data-ttu-id="07b6d-3277">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3277">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3278">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3278">Parameters</span></span>

<span data-ttu-id="07b6d-3279">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3279">value</span></span>  
<span data-ttu-id="07b6d-3280">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3280">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="07b6d-3281">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3281">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3282">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3282">Return Value</span></span>

<span data-ttu-id="07b6d-3283">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3283">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="07b6d-3284">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="07b6d-3284">Method userWidth</span></span>

<span data-ttu-id="07b6d-3285">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3285">Sets or returns the width of the control in pixels.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3286">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3286">Parameters</span></span>

<span data-ttu-id="07b6d-3287">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3287">value</span></span>  
<span data-ttu-id="07b6d-3288">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3288">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3289">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3289">Return Value</span></span>

<span data-ttu-id="07b6d-3290">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3290">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3291">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3291">Remarks</span></span>

<span data-ttu-id="07b6d-3292">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3292">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="07b6d-3293">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3293">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="07b6d-3294">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3294">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-value"></a><span data-ttu-id="07b6d-3295">メソッド value</span><span class="sxs-lookup"><span data-stu-id="07b6d-3295">Method value</span></span>

    public boolean value([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3296">Parameters</span></span>

<span data-ttu-id="07b6d-3297">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3297">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3298">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3298">Return Value</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="07b6d-3299">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="07b6d-3299">Method verticalSpacing</span></span>

<span data-ttu-id="07b6d-3300">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3300">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3301">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3301">Parameters</span></span>

<span data-ttu-id="07b6d-3302">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3302">value</span></span>  
<span data-ttu-id="07b6d-3303">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3303">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3304">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-3304">mode</span></span>  
<span data-ttu-id="07b6d-3305">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3305">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3306">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3306">Return Value</span></span>

<span data-ttu-id="07b6d-3307">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3307">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="07b6d-3308">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-3308">Method verticalSpacingMode</span></span>

<span data-ttu-id="07b6d-3309">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3309">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3310">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3310">Parameters</span></span>

<span data-ttu-id="07b6d-3311">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-3311">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3312">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3312">Return Value</span></span>

<span data-ttu-id="07b6d-3313">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3313">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="07b6d-3314">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-3314">Method verticalSpacingValue</span></span>

<span data-ttu-id="07b6d-3315">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3315">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3316">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3316">Parameters</span></span>

<span data-ttu-id="07b6d-3317">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3317">value</span></span>  
<span data-ttu-id="07b6d-3318">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3318">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3319">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3319">Return Value</span></span>

<span data-ttu-id="07b6d-3320">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3320">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="07b6d-3321">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="07b6d-3321">Method visible</span></span>

<span data-ttu-id="07b6d-3322">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3322">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3323">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3323">Parameters</span></span>

<span data-ttu-id="07b6d-3324">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3324">value</span></span>  
<span data-ttu-id="07b6d-3325">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3325">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3326">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3326">Return Value</span></span>

<span data-ttu-id="07b6d-3327">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3327">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="07b6d-3328">メソッド width</span><span class="sxs-lookup"><span data-stu-id="07b6d-3328">Method width</span></span>

<span data-ttu-id="07b6d-3329">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3329">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3330">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3330">Parameters</span></span>

<span data-ttu-id="07b6d-3331">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3331">value</span></span>  
<span data-ttu-id="07b6d-3332">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3332">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3333">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-3333">mode</span></span>  
<span data-ttu-id="07b6d-3334">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3334">An Integer that indicates how the width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3335">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3335">Return Value</span></span>

<span data-ttu-id="07b6d-3336">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3336">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3337">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3337">Remarks</span></span>

<span data-ttu-id="07b6d-3338">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3338">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="07b6d-3339">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-3339">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="07b6d-3340">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3340">Mode.</span></span>           | <span data-ttu-id="07b6d-3341">幅計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3341">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-3342">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3342">-1 Exact.</span></span>       | <span data-ttu-id="07b6d-3343">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3343">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-3344">0 自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3344">0 Auto.</span></span>         | <span data-ttu-id="07b6d-3345">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3345">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-3346">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3346">1 Column width.</span></span> | <span data-ttu-id="07b6d-3347">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3347">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="07b6d-3348">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3348">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="07b6d-3349">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-3349">Method widthMode</span></span>

<span data-ttu-id="07b6d-3350">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3350">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3351">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3351">Parameters</span></span>

<span data-ttu-id="07b6d-3352">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3352">value</span></span>  
<span data-ttu-id="07b6d-3353">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3353">An integer value that indicates how control width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3354">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3354">Return Value</span></span>

<span data-ttu-id="07b6d-3355">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3355">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3356">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3356">Remarks</span></span>

<span data-ttu-id="07b6d-3357">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-3357">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="07b6d-3358">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3358">Mode.</span></span>         | <span data-ttu-id="07b6d-3359">幅計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3359">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-3360">正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3360">Exact.</span></span>        | <span data-ttu-id="07b6d-3361">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3361">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-3362">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3362">Auto.</span></span>         | <span data-ttu-id="07b6d-3363">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3363">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-3364">列の幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3364">Column width.</span></span> | <span data-ttu-id="07b6d-3365">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3365">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="07b6d-3366">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3366">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="07b6d-3367">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-3367">Method widthValue</span></span>

<span data-ttu-id="07b6d-3368">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3368">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3369">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3369">Parameters</span></span>

<span data-ttu-id="07b6d-3370">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3370">value</span></span>  
<span data-ttu-id="07b6d-3371">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3371">An Integer that specifies the width in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3372">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3372">Return Value</span></span>

<span data-ttu-id="07b6d-3373">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3373">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3374">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3374">Remarks</span></span>

<span data-ttu-id="07b6d-3375">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3375">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-prefcolumnsize"></a><span data-ttu-id="07b6d-3376">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-3376">Method prefColumnSize</span></span>

<span data-ttu-id="07b6d-3377">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3377">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3378">Parameters</span></span>

<span data-ttu-id="07b6d-3379">width</span><span class="sxs-lookup"><span data-stu-id="07b6d-3379">width</span></span>  
<span data-ttu-id="07b6d-3380">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3380">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3381">height</span><span class="sxs-lookup"><span data-stu-id="07b6d-3381">height</span></span>  
<span data-ttu-id="07b6d-3382">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3382">The preferred height of the control.</span></span>

### <a name="method-lostfocus"></a><span data-ttu-id="07b6d-3383">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-3383">Method lostFocus</span></span>

<span data-ttu-id="07b6d-3384">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3384">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-resetusersetting"></a><span data-ttu-id="07b6d-3385">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="07b6d-3385">Method resetUserSetting</span></span>

<span data-ttu-id="07b6d-3386">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3386">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-context"></a><span data-ttu-id="07b6d-3387">メソッド context</span><span class="sxs-lookup"><span data-stu-id="07b6d-3387">Method context</span></span>

<span data-ttu-id="07b6d-3388">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3388">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-drop"></a><span data-ttu-id="07b6d-3389">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="07b6d-3389">Method drop</span></span>

<span data-ttu-id="07b6d-3390">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3390">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3391">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3391">Parameters</span></span>

<span data-ttu-id="07b6d-3392">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-3392">dragSource</span></span>  
<span data-ttu-id="07b6d-3393">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3393">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3394">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-3394">dragMode</span></span>  
<span data-ttu-id="07b6d-3395">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3395">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3396">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3396">x</span></span>  
<span data-ttu-id="07b6d-3397">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3397">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3398">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3398">y</span></span>  
<span data-ttu-id="07b6d-3399">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3399">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-onlostfocus"></a><span data-ttu-id="07b6d-3400">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-3400">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3401">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3401">Parameters</span></span>

<span data-ttu-id="07b6d-3402">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-3402">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3403">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-3403">e</span></span>  

### <a name="method-gotfocus"></a><span data-ttu-id="07b6d-3404">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-3404">Method gotFocus</span></span>

<span data-ttu-id="07b6d-3405">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3405">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-mouseenter"></a><span data-ttu-id="07b6d-3406">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="07b6d-3406">Method mouseEnter</span></span>

<span data-ttu-id="07b6d-3407">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3407">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3408">Parameters</span></span>

<span data-ttu-id="07b6d-3409">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3409">x</span></span>  
<span data-ttu-id="07b6d-3410">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3410">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3411">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3411">y</span></span>  
<span data-ttu-id="07b6d-3412">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3412">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3413">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-3413">button</span></span>  
<span data-ttu-id="07b6d-3414">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3414">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3415">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3415">Ctrl</span></span>  
<span data-ttu-id="07b6d-3416">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3416">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3417">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-3417">Shift</span></span>  
<span data-ttu-id="07b6d-3418">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3418">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-paste"></a><span data-ttu-id="07b6d-3419">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="07b6d-3419">Method paste</span></span>

<span data-ttu-id="07b6d-3420">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3420">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-ongotfocus"></a><span data-ttu-id="07b6d-3421">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-3421">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3422">Parameters</span></span>

<span data-ttu-id="07b6d-3423">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-3423">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3424">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-3424">e</span></span>  

### <a name="method-enddrag"></a><span data-ttu-id="07b6d-3425">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="07b6d-3425">Method endDrag</span></span>

<span data-ttu-id="07b6d-3426">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3426">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="07b6d-3427">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3427">Remarks</span></span>

<span data-ttu-id="07b6d-3428">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3428">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="07b6d-3429">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3429">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-cut"></a><span data-ttu-id="07b6d-3430">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="07b6d-3430">Method cut</span></span>

<span data-ttu-id="07b6d-3431">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3431">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-filter"></a><span data-ttu-id="07b6d-3432">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="07b6d-3432">Method filter</span></span>

    public void filter([str filterStr])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3433">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3433">Parameters</span></span>

<span data-ttu-id="07b6d-3434">filterStr</span><span class="sxs-lookup"><span data-stu-id="07b6d-3434">filterStr</span></span>  

### <a name="method-displaycontrol"></a><span data-ttu-id="07b6d-3435">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3435">Method displayControl</span></span>

<span data-ttu-id="07b6d-3436">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3436">Displays the control.</span></span>

    public void displayControl()

### <a name="method-inputsearch"></a><span data-ttu-id="07b6d-3437">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="07b6d-3437">Method inputSearch</span></span>

<span data-ttu-id="07b6d-3438">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3438">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3439">Parameters</span></span>

<span data-ttu-id="07b6d-3440">searchStr</span><span class="sxs-lookup"><span data-stu-id="07b6d-3440">searchStr</span></span>  
<span data-ttu-id="07b6d-3441">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3441">The string value to use to filter data; optional.</span></span>

### <a name="method-copy"></a><span data-ttu-id="07b6d-3442">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="07b6d-3442">Method copy</span></span>

<span data-ttu-id="07b6d-3443">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3443">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-clicked"></a><span data-ttu-id="07b6d-3444">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="07b6d-3444">Method clicked</span></span>

    public void clicked()

### <a name="method-onclicked"></a><span data-ttu-id="07b6d-3445">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="07b6d-3445">Method OnClicked</span></span>

    private void OnClicked([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3446">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3446">Parameters</span></span>

<span data-ttu-id="07b6d-3447">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-3447">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3448">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-3448">e</span></span>  

### <a name="method-dropex"></a><span data-ttu-id="07b6d-3449">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-3449">Method dropEx</span></span>

<span data-ttu-id="07b6d-3450">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3450">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3451">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3451">Parameters</span></span>

<span data-ttu-id="07b6d-3452">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-3452">dragSource</span></span>  
<span data-ttu-id="07b6d-3453">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3453">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3454">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-3454">dragMode</span></span>  
<span data-ttu-id="07b6d-3455">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3455">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3456">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3456">x</span></span>  
<span data-ttu-id="07b6d-3457">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3457">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3458">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3458">y</span></span>  
<span data-ttu-id="07b6d-3459">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3459">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-mouseleave"></a><span data-ttu-id="07b6d-3460">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="07b6d-3460">Method mouseLeave</span></span>

<span data-ttu-id="07b6d-3461">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3461">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-setfocus"></a><span data-ttu-id="07b6d-3462">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-3462">Method setFocus</span></span>

<span data-ttu-id="07b6d-3463">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3463">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-dragleave"></a><span data-ttu-id="07b6d-3464">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="07b6d-3464">Method dragLeave</span></span>

<span data-ttu-id="07b6d-3465">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3465">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-jumpref"></a><span data-ttu-id="07b6d-3466">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="07b6d-3466">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-registeroverridemethod"></a><span data-ttu-id="07b6d-3467">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="07b6d-3467">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3468">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3468">Parameters</span></span>

<span data-ttu-id="07b6d-3469">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="07b6d-3469">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3470">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="07b6d-3470">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3471">overrideObject</span><span class="sxs-lookup"><span data-stu-id="07b6d-3471">overrideObject</span></span>  

## <a name="class-formgridcontrol"></a><span data-ttu-id="07b6d-3472">クラス FormGridControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3472">Class FormGridControl</span></span>
    class FormGridControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="07b6d-3473">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3473">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="07b6d-3474">例</span><span class="sxs-lookup"><span data-stu-id="07b6d-3474">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="07b6d-3475">メソッド</span><span class="sxs-lookup"><span data-stu-id="07b6d-3475">Methods</span></span>

| <span data-ttu-id="07b6d-3476">方法</span><span class="sxs-lookup"><span data-stu-id="07b6d-3476">Method</span></span>                                                                                                              | <span data-ttu-id="07b6d-3477">説明</span><span class="sxs-lookup"><span data-stu-id="07b6d-3477">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-3478">public int activeBackColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3478">public int activeBackColor(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3479">public int activeForeColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3479">public int activeForeColor(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3480">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3480">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3481">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3481">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3482">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3482">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3483">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3483">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="07b6d-3484">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3484">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-3485">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3485">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="07b6d-3486">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3486">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-3487">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3487">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="07b6d-3488">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3488">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="07b6d-3489">public int alternateRowShading(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3489">public int alternateRowShading(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3490">public boolean autoDataGroup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3490">public boolean autoDataGroup(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3491">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3491">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="07b6d-3492">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3492">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="07b6d-3493">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3493">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="07b6d-3494">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3494">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="07b6d-3495">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3495">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="07b6d-3496">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3496">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-3497">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3497">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="07b6d-3498">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3498">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-3499">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3499">public int border(\[int value\])</span></span>                                                                                    | <span data-ttu-id="07b6d-3500">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3500">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="07b6d-3501">public int bottomMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3501">public int bottomMargin(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3502">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3502">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="07b6d-3503">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3503">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="07b6d-3504">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3504">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3505">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3505">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3506">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3506">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="07b6d-3507">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3507">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-3508">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3508">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="07b6d-3509">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3509">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-3510">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3510">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="07b6d-3511">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3511">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-3512">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3512">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3513">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3513">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3514">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3514">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3515">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3515">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="07b6d-3516">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3516">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="07b6d-3517">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3517">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3518">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3518">public str dataGroup(\[str value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3519">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3519">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="07b6d-3520">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3520">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="07b6d-3521">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3521">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="07b6d-3522">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3522">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-3523">public str defaultAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3523">public str defaultAction(\[str value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3524">public str defaultActionLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3524">public str defaultActionLabel(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3525">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3525">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="07b6d-3526">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3526">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span> |
| <span data-ttu-id="07b6d-3527">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3527">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="07b6d-3528">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3528">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="07b6d-3529">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3529">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="07b6d-3530">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3530">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="07b6d-3531">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3531">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="07b6d-3532">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3532">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-3533">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3533">public str dragText()</span></span>                                                                                               | <span data-ttu-id="07b6d-3534">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3534">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-3535">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3535">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="07b6d-3536">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3536">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-3537">public boolean exportAllowed(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3537">public boolean exportAllowed(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3538">public str exportLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3538">public str exportLabel(\[str value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3539">public Struct getLineData(int lineNumber)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3539">public Struct getLineData(int lineNumber)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3540">public Struct getSelectedData()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3540">public Struct getSelectedData()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3541">public boolean gridLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3541">public boolean gridLines(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3542">public int gridLinesStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3542">public int gridLinesStyle(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3543">public str groupBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3543">public str groupBy(\[str value\])</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3544">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3544">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="07b6d-3545">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3545">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="07b6d-3546">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3546">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="07b6d-3547">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3547">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="07b6d-3548">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3548">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="07b6d-3549">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3549">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-3550">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3550">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="07b6d-3551">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3551">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-3552">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3552">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="07b6d-3553">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3553">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="07b6d-3554">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3554">public str helpField()</span></span>                                                                                              | <span data-ttu-id="07b6d-3555">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3555">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-3556">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3556">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="07b6d-3557">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3557">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="07b6d-3558">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3558">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="07b6d-3559">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3559">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="07b6d-3560">public boolean highlightActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3560">public boolean highlightActive(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3561">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3561">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="07b6d-3562">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3562">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-3563">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3563">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3564">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3564">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="07b6d-3565">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3565">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="07b6d-3566">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3566">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="07b6d-3567">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3567">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="07b6d-3568">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3568">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="07b6d-3569">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3569">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="07b6d-3570">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3570">public boolean leave()</span></span>                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3571">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3571">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="07b6d-3572">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3572">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="07b6d-3573">public int leftMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3573">public int leftMargin(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3574">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3574">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="07b6d-3575">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3575">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-3576">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3576">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="07b6d-3577">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3577">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="07b6d-3578">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3578">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="07b6d-3579">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3579">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="07b6d-3580">public int moreRowsIndicator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3580">public int moreRowsIndicator(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3581">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3581">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="07b6d-3582">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3582">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="07b6d-3583">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3583">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="07b6d-3584">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3584">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-3585">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3585">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="07b6d-3586">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3586">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="07b6d-3587">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3587">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="07b6d-3588">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3588">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="07b6d-3589">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3589">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3590">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3590">public boolean multiSelect(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3591">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3591">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="07b6d-3592">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3592">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="07b6d-3593">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3593">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3594">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3594">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3595">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3595">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="07b6d-3596">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3596">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="07b6d-3597">public int rightMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3597">public int rightMargin(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3598">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3598">public int scrollbars(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3599">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3599">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="07b6d-3600">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3600">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-3601">public boolean showColLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3601">public boolean showColLabels(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3602">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3602">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="07b6d-3603">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3603">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-3604">public boolean showRowLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3604">public boolean showRowLabels(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3605">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3605">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="07b6d-3606">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3606">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="07b6d-3607">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3607">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3608">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3608">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3609">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3609">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="07b6d-3610">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3610">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-3611">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3611">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="07b6d-3612">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3612">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-3613">public int topMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3613">public int topMargin(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3614">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3614">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="07b6d-3615">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3615">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-3616">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3616">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="07b6d-3617">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3617">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-3618">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3618">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3619">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3619">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3620">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3620">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="07b6d-3621">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3621">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="07b6d-3622">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3622">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="07b6d-3623">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3623">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="07b6d-3624">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3624">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="07b6d-3625">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3625">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-3626">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3626">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="07b6d-3627">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3627">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="07b6d-3628">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3628">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="07b6d-3629">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3629">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="07b6d-3630">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3630">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="07b6d-3631">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3631">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="07b6d-3632">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3632">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="07b6d-3633">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3633">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="07b6d-3634">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3634">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="07b6d-3635">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3635">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-3636">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3636">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="07b6d-3637">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3637">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="07b6d-3638">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3638">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="07b6d-3639">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3639">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="07b6d-3640">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3640">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="07b6d-3641">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3641">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="07b6d-3642">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3642">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="07b6d-3643">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3643">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="07b6d-3644">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3644">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3645">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3645">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="07b6d-3646">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3646">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-3647">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3647">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="07b6d-3648">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3648">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="07b6d-3649">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3649">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="07b6d-3650">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3650">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-3651">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3651">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="07b6d-3652">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3652">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-3653">public int visibleCols(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3653">public int visibleCols(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3654">public AutoMode visibleColsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3654">public AutoMode visibleColsMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3655">public int visibleColsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3655">public int visibleColsValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3656">public int visibleRows(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3656">public int visibleRows(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3657">public AutoMode visibleRowsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3657">public AutoMode visibleRowsMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3658">public int visibleRowsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3658">public int visibleRowsValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3659">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3659">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="07b6d-3660">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3660">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="07b6d-3661">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3661">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="07b6d-3662">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3662">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="07b6d-3663">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3663">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="07b6d-3664">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3664">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="07b6d-3665">public void cut()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3665">public void cut()</span></span>                                                                                                   | <span data-ttu-id="07b6d-3666">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3666">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="07b6d-3667">public void applyQuickFilter(\[int controlId\], \[str filterValue\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3667">public void applyQuickFilter(\[int controlId\], \[str filterValue\])</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3668">public void autoSizeColumns(\[boolean autoSizeColumns\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3668">public void autoSizeColumns(\[boolean autoSizeColumns\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3669">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3669">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="07b6d-3670">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3670">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="07b6d-3671">public void context()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3671">public void context()</span></span>                                                                                               | <span data-ttu-id="07b6d-3672">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3672">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="07b6d-3673">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3673">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3674">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3674">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                           |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3675">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3675">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3676">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3676">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3677">public void copy()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3677">public void copy()</span></span>                                                                                                  | <span data-ttu-id="07b6d-3678">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3678">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="07b6d-3679">public void enter()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3679">public void enter()</span></span>                                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3680">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3680">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="07b6d-3681">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3681">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="07b6d-3682">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3682">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="07b6d-3683">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3683">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="07b6d-3684">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3684">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3685">public void paste()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3685">public void paste()</span></span>                                                                                                 | <span data-ttu-id="07b6d-3686">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3686">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-3687">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3687">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="07b6d-3688">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3688">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="07b6d-3689">public void quickFilterProvider(\[GridQuickFilterProvider quickFilterProvider\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3689">public void quickFilterProvider(\[GridQuickFilterProvider quickFilterProvider\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3690">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3690">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="07b6d-3691">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3691">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="07b6d-3692">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3692">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3693">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3693">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="07b6d-3694">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3694">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="07b6d-3695">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3695">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3696">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="07b6d-3696">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="07b6d-3697">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3697">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="07b6d-3698">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3698">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="07b6d-3699">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3699">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="07b6d-3700">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="07b6d-3700">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3701">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3701">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="07b6d-3702">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3702">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="07b6d-3703">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3703">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="07b6d-3704">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3704">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="07b6d-3705">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3705">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="07b6d-3706">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3706">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="07b6d-3707">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3707">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="07b6d-3708">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3708">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="07b6d-3709">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3709">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="07b6d-3710">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="07b6d-3710">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="07b6d-3711">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3711">Sets the focus on the control.</span></span>                                                                                                                                          |

### <a name="method-activebackcolor"></a><span data-ttu-id="07b6d-3712">メソッド activeBackColor</span><span class="sxs-lookup"><span data-stu-id="07b6d-3712">Method activeBackColor</span></span>

    public int activeBackColor([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3713">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3713">Parameters</span></span>

<span data-ttu-id="07b6d-3714">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3714">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3715">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3715">Return Value</span></span>

### <a name="method-activeforecolor"></a><span data-ttu-id="07b6d-3716">メソッド activeForeColor</span><span class="sxs-lookup"><span data-stu-id="07b6d-3716">Method activeForeColor</span></span>

    public int activeForeColor([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3717">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3717">Parameters</span></span>

<span data-ttu-id="07b6d-3718">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3718">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3719">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3719">Return Value</span></span>

### <a name="method-addcontrol"></a><span data-ttu-id="07b6d-3720">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3720">Method addControl</span></span>

    public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3721">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3721">Parameters</span></span>

<span data-ttu-id="07b6d-3722">controlType</span><span class="sxs-lookup"><span data-stu-id="07b6d-3722">controlType</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3723">controlName</span><span class="sxs-lookup"><span data-stu-id="07b6d-3723">controlName</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3724">insertAfter</span><span class="sxs-lookup"><span data-stu-id="07b6d-3724">insertAfter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3725">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3725">Return Value</span></span>

### <a name="method-addcontrolex"></a><span data-ttu-id="07b6d-3726">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-3726">Method addControlEx</span></span>

    public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3727">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3727">Parameters</span></span>

<span data-ttu-id="07b6d-3728">controlClass</span><span class="sxs-lookup"><span data-stu-id="07b6d-3728">controlClass</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3729">controlName</span><span class="sxs-lookup"><span data-stu-id="07b6d-3729">controlName</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3730">insertAfter</span><span class="sxs-lookup"><span data-stu-id="07b6d-3730">insertAfter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3731">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3731">Return Value</span></span>

### <a name="method-adddatafield"></a><span data-ttu-id="07b6d-3732">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="07b6d-3732">Method addDataField</span></span>

    public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3733">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3733">Parameters</span></span>

<span data-ttu-id="07b6d-3734">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="07b6d-3734">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3735">fieldId</span><span class="sxs-lookup"><span data-stu-id="07b6d-3735">fieldId</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3736">insertAfter</span><span class="sxs-lookup"><span data-stu-id="07b6d-3736">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3737">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="07b6d-3737">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3738">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3738">Return Value</span></span>

### <a name="method-aligncontrol"></a><span data-ttu-id="07b6d-3739">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-3739">Method alignControl</span></span>

<span data-ttu-id="07b6d-3740">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3740">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3741">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3741">Parameters</span></span>

<span data-ttu-id="07b6d-3742">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3742">value</span></span>  
<span data-ttu-id="07b6d-3743">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3743">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3744">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3744">Return Value</span></span>

<span data-ttu-id="07b6d-3745">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3745">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3746">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3746">Remarks</span></span>

<span data-ttu-id="07b6d-3747">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3747">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="07b6d-3748">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="07b6d-3748">Method allowEdit</span></span>

<span data-ttu-id="07b6d-3749">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3749">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3750">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3750">Parameters</span></span>

<span data-ttu-id="07b6d-3751">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3751">value</span></span>  
<span data-ttu-id="07b6d-3752">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3752">The value to assign to the allowEdit property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3753">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3753">Return Value</span></span>

<span data-ttu-id="07b6d-3754">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3754">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3755">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3755">Remarks</span></span>

<span data-ttu-id="07b6d-3756">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3756">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="07b6d-3757">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="07b6d-3757">Method allowSysSetup</span></span>

<span data-ttu-id="07b6d-3758">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3758">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="07b6d-3759">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3759">Return Value</span></span>

<span data-ttu-id="07b6d-3760">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3760">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-alternaterowshading"></a><span data-ttu-id="07b6d-3761">メソッド alternateRowShading</span><span class="sxs-lookup"><span data-stu-id="07b6d-3761">Method alternateRowShading</span></span>

    public int alternateRowShading([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3762">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3762">Parameters</span></span>

<span data-ttu-id="07b6d-3763">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3763">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3764">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3764">Return Value</span></span>

### <a name="method-autodatagroup"></a><span data-ttu-id="07b6d-3765">メソッド autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="07b6d-3765">Method autoDataGroup</span></span>

    public boolean autoDataGroup([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3766">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3766">Parameters</span></span>

<span data-ttu-id="07b6d-3767">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3767">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3768">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3768">Return Value</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="07b6d-3769">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="07b6d-3769">Method autoDeclaration</span></span>

<span data-ttu-id="07b6d-3770">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3770">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3771">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3771">Parameters</span></span>

<span data-ttu-id="07b6d-3772">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3772">value</span></span>  
<span data-ttu-id="07b6d-3773">プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3773">The value to assign to the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3774">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3774">Return Value</span></span>

<span data-ttu-id="07b6d-3775">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3775">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3776">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3776">Remarks</span></span>

<span data-ttu-id="07b6d-3777">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3777">Controls cannot have identical names.</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="07b6d-3778">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="07b6d-3778">Method backgroundColor</span></span>

<span data-ttu-id="07b6d-3779">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3779">Gets or sets the background color of the control.</span></span>

    public int backgroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3780">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3780">Parameters</span></span>

<span data-ttu-id="07b6d-3781">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3781">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3782">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3782">Return Value</span></span>

<span data-ttu-id="07b6d-3783">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3783">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3784">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3784">Remarks</span></span>

<span data-ttu-id="07b6d-3785">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3785">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="07b6d-3786">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3786">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="07b6d-3787">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3787">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="07b6d-3788">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3788">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="07b6d-3789">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3789">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="07b6d-3790">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3790">The maximum value for a single byte is 255.</span></span>

### <a name="method-backstyle"></a><span data-ttu-id="07b6d-3791">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="07b6d-3791">Method backStyle</span></span>

<span data-ttu-id="07b6d-3792">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3792">Determines whether the control background can be transparent.</span></span>

    public int backStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3793">Parameters</span></span>

<span data-ttu-id="07b6d-3794">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3794">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3795">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3795">Return Value</span></span>

<span data-ttu-id="07b6d-3796">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3796">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="07b6d-3797">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="07b6d-3797">Method beginDrag</span></span>

<span data-ttu-id="07b6d-3798">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3798">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3799">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3799">Parameters</span></span>

<span data-ttu-id="07b6d-3800">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3800">x</span></span>  
<span data-ttu-id="07b6d-3801">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3801">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="07b6d-3802">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3802">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3803">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3803">y</span></span>  
<span data-ttu-id="07b6d-3804">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3804">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="07b6d-3805">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3805">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3806">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3806">Return Value</span></span>

<span data-ttu-id="07b6d-3807">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3807">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3808">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3808">Remarks</span></span>

<span data-ttu-id="07b6d-3809">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3809">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="07b6d-3810">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3810">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-border"></a><span data-ttu-id="07b6d-3811">メソッド border</span><span class="sxs-lookup"><span data-stu-id="07b6d-3811">Method border</span></span>

<span data-ttu-id="07b6d-3812">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3812">Gets or sets the style of the borderline of the control.</span></span>

    public int border([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3813">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3813">Parameters</span></span>

<span data-ttu-id="07b6d-3814">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3814">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3815">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3815">Return Value</span></span>

<span data-ttu-id="07b6d-3816">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3816">An integer between zero and four, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3817">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3817">Remarks</span></span>

<span data-ttu-id="07b6d-3818">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3818">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="07b6d-3819">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3819">Value.</span></span> | <span data-ttu-id="07b6d-3820">説明。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3820">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="07b6d-3821">0</span><span class="sxs-lookup"><span data-stu-id="07b6d-3821">0</span></span>      | <span data-ttu-id="07b6d-3822">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3822">Auto.</span></span>        |
| <span data-ttu-id="07b6d-3823">1</span><span class="sxs-lookup"><span data-stu-id="07b6d-3823">1</span></span>      | <span data-ttu-id="07b6d-3824">3D。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3824">3D.</span></span>          |
| <span data-ttu-id="07b6d-3825">2</span><span class="sxs-lookup"><span data-stu-id="07b6d-3825">2</span></span>      | <span data-ttu-id="07b6d-3826">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3826">Single line.</span></span> |
| <span data-ttu-id="07b6d-3827">3</span><span class="sxs-lookup"><span data-stu-id="07b6d-3827">3</span></span>      | <span data-ttu-id="07b6d-3828">均一。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3828">Flat.</span></span>        |
| <span data-ttu-id="07b6d-3829">4</span><span class="sxs-lookup"><span data-stu-id="07b6d-3829">4</span></span>      | <span data-ttu-id="07b6d-3830">なし。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3830">None.</span></span>        |

### <a name="method-bottommargin"></a><span data-ttu-id="07b6d-3831">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="07b6d-3831">Method bottomMargin</span></span>

    public int bottomMargin([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3832">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3832">Parameters</span></span>

<span data-ttu-id="07b6d-3833">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3833">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3834">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3834">Return Value</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="07b6d-3835">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-3835">Method calcControlSize</span></span>

<span data-ttu-id="07b6d-3836">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3836">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3837">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3837">Parameters</span></span>

<span data-ttu-id="07b6d-3838">chars</span><span class="sxs-lookup"><span data-stu-id="07b6d-3838">chars</span></span>  
<span data-ttu-id="07b6d-3839">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3839">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3840">明細行</span><span class="sxs-lookup"><span data-stu-id="07b6d-3840">lines</span></span>  
<span data-ttu-id="07b6d-3841">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3841">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3842">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3842">Return Value</span></span>

<span data-ttu-id="07b6d-3843">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3843">The container that holds the width and height.</span></span>

### <a name="method-canadddatafield"></a><span data-ttu-id="07b6d-3844">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="07b6d-3844">Method canAddDataField</span></span>

    public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3845">Parameters</span></span>

<span data-ttu-id="07b6d-3846">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="07b6d-3846">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3847">fieldId</span><span class="sxs-lookup"><span data-stu-id="07b6d-3847">fieldId</span></span>  

<!-- -->

<span data-ttu-id="07b6d-3848">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="07b6d-3848">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3849">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3849">Return Value</span></span>

### <a name="method-cancontain"></a><span data-ttu-id="07b6d-3850">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="07b6d-3850">Method canContain</span></span>

    public boolean canContain(FormControl control)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3851">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3851">Parameters</span></span>

<span data-ttu-id="07b6d-3852">control</span><span class="sxs-lookup"><span data-stu-id="07b6d-3852">control</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3853">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3853">Return Value</span></span>

### <a name="method-colorscheme"></a><span data-ttu-id="07b6d-3854">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="07b6d-3854">Method colorScheme</span></span>

<span data-ttu-id="07b6d-3855">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3855">Gets or sets the color scheme of the control.</span></span>

    public int colorScheme([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3856">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3856">Parameters</span></span>

<span data-ttu-id="07b6d-3857">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3857">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3858">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3858">Return Value</span></span>

<span data-ttu-id="07b6d-3859">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3859">An integer between zero and two, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3860">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3860">Remarks</span></span>

<span data-ttu-id="07b6d-3861">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3861">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="07b6d-3862">値です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3862">Value.</span></span> | <span data-ttu-id="07b6d-3863">スタイル。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3863">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="07b6d-3864">0</span><span class="sxs-lookup"><span data-stu-id="07b6d-3864">0</span></span>      | <span data-ttu-id="07b6d-3865">既定。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3865">Default.</span></span>                      |
| <span data-ttu-id="07b6d-3866">1</span><span class="sxs-lookup"><span data-stu-id="07b6d-3866">1</span></span>      | <span data-ttu-id="07b6d-3867">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3867">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="07b6d-3868">2</span><span class="sxs-lookup"><span data-stu-id="07b6d-3868">2</span></span>      | <span data-ttu-id="07b6d-3869">真の配色。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3869">The true-color scheme.</span></span>        |

### <a name="method-configurationkey"></a><span data-ttu-id="07b6d-3870">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="07b6d-3870">Method configurationKey</span></span>

<span data-ttu-id="07b6d-3871">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3871">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3872">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3872">Parameters</span></span>

<span data-ttu-id="07b6d-3873">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3873">value</span></span>  
<span data-ttu-id="07b6d-3874">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3874">The ID of the configuration key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3875">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3875">Return Value</span></span>

<span data-ttu-id="07b6d-3876">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3876">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3877">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3877">Remarks</span></span>

<span data-ttu-id="07b6d-3878">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3878">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="07b6d-3879">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3879">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="07b6d-3880">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-3880">Method configurationKeyEx</span></span>

<span data-ttu-id="07b6d-3881">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3881">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="07b6d-3882">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3882">Return Value</span></span>

<span data-ttu-id="07b6d-3883">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3883">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3884">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3884">Remarks</span></span>

<span data-ttu-id="07b6d-3885">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3885">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="07b6d-3886">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3886">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="07b6d-3887">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3887">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-contains"></a><span data-ttu-id="07b6d-3888">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="07b6d-3888">Method contains</span></span>

    public boolean contains(FormControl control)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3889">Parameters</span></span>

<span data-ttu-id="07b6d-3890">control</span><span class="sxs-lookup"><span data-stu-id="07b6d-3890">control</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3891">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3891">Return Value</span></span>

### <a name="method-controlcount"></a><span data-ttu-id="07b6d-3892">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="07b6d-3892">Method controlCount</span></span>

    public int controlCount()

#### <a name="return-value"></a><span data-ttu-id="07b6d-3893">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3893">Return Value</span></span>

### <a name="method-controlnum"></a><span data-ttu-id="07b6d-3894">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="07b6d-3894">Method controlNum</span></span>

    public FormControl controlNum(int controlNo)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3895">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3895">Parameters</span></span>

<span data-ttu-id="07b6d-3896">controlNo</span><span class="sxs-lookup"><span data-stu-id="07b6d-3896">controlNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3897">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3897">Return Value</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="07b6d-3898">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="07b6d-3898">Method countryRegionCodes</span></span>

<span data-ttu-id="07b6d-3899">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3899">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3900">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3900">Parameters</span></span>

<span data-ttu-id="07b6d-3901">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3901">value</span></span>  
<span data-ttu-id="07b6d-3902">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3902">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3903">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3903">Return Value</span></span>

<span data-ttu-id="07b6d-3904">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3904">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-countryregioncontextfield"></a><span data-ttu-id="07b6d-3905">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="07b6d-3905">Method countryRegionContextField</span></span>

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3906">Parameters</span></span>

<span data-ttu-id="07b6d-3907">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3907">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3908">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3908">Return Value</span></span>

### <a name="method-datagroup"></a><span data-ttu-id="07b6d-3909">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="07b6d-3909">Method dataGroup</span></span>

    public str dataGroup([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3910">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3910">Parameters</span></span>

<span data-ttu-id="07b6d-3911">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3911">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3912">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3912">Return Value</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="07b6d-3913">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="07b6d-3913">Method dataRelationPath</span></span>

<span data-ttu-id="07b6d-3914">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3914">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3915">Parameters</span></span>

<span data-ttu-id="07b6d-3916">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3916">value</span></span>  
<span data-ttu-id="07b6d-3917">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3917">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3918">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3918">Return Value</span></span>

<span data-ttu-id="07b6d-3919">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3919">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3920">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3920">Remarks</span></span>

<span data-ttu-id="07b6d-3921">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3921">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="07b6d-3922">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3922">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-datasource"></a><span data-ttu-id="07b6d-3923">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-3923">Method dataSource</span></span>

<span data-ttu-id="07b6d-3924">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3924">Gets or sets a data source to be used by the control or the form.</span></span>

    public int dataSource([AnyType value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3925">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3925">Parameters</span></span>

<span data-ttu-id="07b6d-3926">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3926">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3927">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3927">Return Value</span></span>

<span data-ttu-id="07b6d-3928">使用する必要のあるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3928">The identifier of the data source that must be used.</span></span>

### <a name="method-defaultaction"></a><span data-ttu-id="07b6d-3929">メソッド defaultAction</span><span class="sxs-lookup"><span data-stu-id="07b6d-3929">Method defaultAction</span></span>

    public str defaultAction([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3930">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3930">Parameters</span></span>

<span data-ttu-id="07b6d-3931">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3931">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3932">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3932">Return Value</span></span>

### <a name="method-defaultactionlabel"></a><span data-ttu-id="07b6d-3933">メソッド defaultActionLabel</span><span class="sxs-lookup"><span data-stu-id="07b6d-3933">Method defaultActionLabel</span></span>

    public str defaultActionLabel([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3934">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3934">Parameters</span></span>

<span data-ttu-id="07b6d-3935">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3935">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3936">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3936">Return Value</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="07b6d-3937">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="07b6d-3937">Method displayTarget</span></span>

<span data-ttu-id="07b6d-3938">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3938">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3939">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3939">Parameters</span></span>

<span data-ttu-id="07b6d-3940">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3940">value</span></span>  
<span data-ttu-id="07b6d-3941">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3941">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3942">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3942">Return Value</span></span>

<span data-ttu-id="07b6d-3943">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3943">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="07b6d-3944">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="07b6d-3944">Method dragDrop</span></span>

<span data-ttu-id="07b6d-3945">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3945">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3946">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3946">Parameters</span></span>

<span data-ttu-id="07b6d-3947">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3947">value</span></span>  
<span data-ttu-id="07b6d-3948">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3948">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3949">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3949">Return Value</span></span>

<span data-ttu-id="07b6d-3950">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3950">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3951">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3951">Remarks</span></span>

<span data-ttu-id="07b6d-3952">dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3952">Use the dragLeave Method, dragOver Method, and dragOverEx Method methods to specify the behavior.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="07b6d-3953">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="07b6d-3953">Method dragOver</span></span>

<span data-ttu-id="07b6d-3954">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3954">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3955">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3955">Parameters</span></span>

<span data-ttu-id="07b6d-3956">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-3956">dragSource</span></span>  
<span data-ttu-id="07b6d-3957">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3957">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3958">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-3958">dragMode</span></span>  
<span data-ttu-id="07b6d-3959">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3959">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3960">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3960">x</span></span>  
<span data-ttu-id="07b6d-3961">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3961">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3962">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3962">y</span></span>  
<span data-ttu-id="07b6d-3963">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3963">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3964">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3964">Return Value</span></span>

<span data-ttu-id="07b6d-3965">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3965">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="07b6d-3966">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-3966">Method dragOverEx</span></span>

<span data-ttu-id="07b6d-3967">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3967">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-3968">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3968">Parameters</span></span>

<span data-ttu-id="07b6d-3969">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-3969">dragSource</span></span>  
<span data-ttu-id="07b6d-3970">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3970">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3971">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-3971">dragMode</span></span>  
<span data-ttu-id="07b6d-3972">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3972">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3973">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-3973">x</span></span>  
<span data-ttu-id="07b6d-3974">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3974">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-3975">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-3975">y</span></span>  
<span data-ttu-id="07b6d-3976">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3976">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3977">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3977">Return Value</span></span>

<span data-ttu-id="07b6d-3978">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3978">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="07b6d-3979">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="07b6d-3979">Method dragText</span></span>

<span data-ttu-id="07b6d-3980">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3980">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="07b6d-3981">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3981">Return Value</span></span>

<span data-ttu-id="07b6d-3982">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3982">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="07b6d-3983">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="07b6d-3983">Method enabled</span></span>

<span data-ttu-id="07b6d-3984">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3984">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3985">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3985">Parameters</span></span>

<span data-ttu-id="07b6d-3986">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3986">value</span></span>  
<span data-ttu-id="07b6d-3987">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3987">A Boolean value that indicates whether the control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-3988">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3988">Return Value</span></span>

<span data-ttu-id="07b6d-3989">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3989">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-3990">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-3990">Remarks</span></span>

<span data-ttu-id="07b6d-3991">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3991">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="07b6d-3992">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3992">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="07b6d-3993">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-3993">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-exportallowed"></a><span data-ttu-id="07b6d-3994">メソッド exportAllowed</span><span class="sxs-lookup"><span data-stu-id="07b6d-3994">Method exportAllowed</span></span>

    public boolean exportAllowed([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3995">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3995">Parameters</span></span>

<span data-ttu-id="07b6d-3996">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3996">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-3997">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-3997">Return Value</span></span>

### <a name="method-exportlabel"></a><span data-ttu-id="07b6d-3998">メソッド exportLabel</span><span class="sxs-lookup"><span data-stu-id="07b6d-3998">Method exportLabel</span></span>

    public str exportLabel([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-3999">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-3999">Parameters</span></span>

<span data-ttu-id="07b6d-4000">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4000">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4001">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4001">Return Value</span></span>

### <a name="method-getlinedata"></a><span data-ttu-id="07b6d-4002">メソッド getLineData</span><span class="sxs-lookup"><span data-stu-id="07b6d-4002">Method getLineData</span></span>

    public Struct getLineData(int lineNumber)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4003">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4003">Parameters</span></span>

<span data-ttu-id="07b6d-4004">lineNumber</span><span class="sxs-lookup"><span data-stu-id="07b6d-4004">lineNumber</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4005">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4005">Return Value</span></span>

### <a name="method-getselecteddata"></a><span data-ttu-id="07b6d-4006">メソッド getSelectedData</span><span class="sxs-lookup"><span data-stu-id="07b6d-4006">Method getSelectedData</span></span>

    public Struct getSelectedData()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4007">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4007">Return Value</span></span>

### <a name="method-gridlines"></a><span data-ttu-id="07b6d-4008">メソッド gridLines</span><span class="sxs-lookup"><span data-stu-id="07b6d-4008">Method gridLines</span></span>

    public boolean gridLines([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4009">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4009">Parameters</span></span>

<span data-ttu-id="07b6d-4010">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4010">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4011">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4011">Return Value</span></span>

### <a name="method-gridlinesstyle"></a><span data-ttu-id="07b6d-4012">メソッド gridLinesStyle</span><span class="sxs-lookup"><span data-stu-id="07b6d-4012">Method gridLinesStyle</span></span>

    public int gridLinesStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4013">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4013">Parameters</span></span>

<span data-ttu-id="07b6d-4014">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4014">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4015">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4015">Return Value</span></span>

### <a name="method-groupby"></a><span data-ttu-id="07b6d-4016">メソッド groupBy</span><span class="sxs-lookup"><span data-stu-id="07b6d-4016">Method groupBy</span></span>

    public str groupBy([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4017">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4017">Parameters</span></span>

<span data-ttu-id="07b6d-4018">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4018">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4019">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4019">Return Value</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="07b6d-4020">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="07b6d-4020">Method hasChanged</span></span>

<span data-ttu-id="07b6d-4021">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4021">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4022">Parameters</span></span>

<span data-ttu-id="07b6d-4023">val</span><span class="sxs-lookup"><span data-stu-id="07b6d-4023">val</span></span>  
<span data-ttu-id="07b6d-4024">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4024">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4025">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4025">Return Value</span></span>

<span data-ttu-id="07b6d-4026">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4026">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="07b6d-4027">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="07b6d-4027">Method hasUserSetting</span></span>

<span data-ttu-id="07b6d-4028">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4028">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4029">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4029">Return Value</span></span>

<span data-ttu-id="07b6d-4030">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4030">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="07b6d-4031">メソッド height</span><span class="sxs-lookup"><span data-stu-id="07b6d-4031">Method height</span></span>

<span data-ttu-id="07b6d-4032">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4032">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4033">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4033">Parameters</span></span>

<span data-ttu-id="07b6d-4034">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4034">value</span></span>  
<span data-ttu-id="07b6d-4035">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4035">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4036">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4036">mode</span></span>  
<span data-ttu-id="07b6d-4037">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4037">An integer that indicates how the height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4038">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4038">Return Value</span></span>

<span data-ttu-id="07b6d-4039">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4039">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4040">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4040">Remarks</span></span>

<span data-ttu-id="07b6d-4041">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4041">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="07b6d-4042">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-4042">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="07b6d-4043">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4043">Mode.</span></span>            | <span data-ttu-id="07b6d-4044">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4044">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-4045">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4045">-1 Exact.</span></span>        | <span data-ttu-id="07b6d-4046">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4046">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-4047">0 自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4047">0 Auto.</span></span>          | <span data-ttu-id="07b6d-4048">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4048">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-4049">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4049">1 Column height.</span></span> | <span data-ttu-id="07b6d-4050">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4050">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="07b6d-4051">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4051">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="07b6d-4052">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4052">Method heightMode</span></span>

<span data-ttu-id="07b6d-4053">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4053">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4054">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4054">Parameters</span></span>

<span data-ttu-id="07b6d-4055">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4055">value</span></span>  
<span data-ttu-id="07b6d-4056">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4056">An integer value that indicates how control height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4057">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4057">Return Value</span></span>

<span data-ttu-id="07b6d-4058">計算モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4058">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4059">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4059">Remarks</span></span>

<span data-ttu-id="07b6d-4060">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-4060">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="07b6d-4061">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4061">Mode.</span></span>          | <span data-ttu-id="07b6d-4062">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4062">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-4063">正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4063">Exact.</span></span>         | <span data-ttu-id="07b6d-4064">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4064">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-4065">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4065">Auto.</span></span>          | <span data-ttu-id="07b6d-4066">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4066">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-4067">列の高さ</span><span class="sxs-lookup"><span data-stu-id="07b6d-4067">Column height.</span></span> | <span data-ttu-id="07b6d-4068">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4068">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="07b6d-4069">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4069">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="07b6d-4070">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-4070">Method heightValue</span></span>

<span data-ttu-id="07b6d-4071">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4071">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4072">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4072">Parameters</span></span>

<span data-ttu-id="07b6d-4073">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4073">value</span></span>  
<span data-ttu-id="07b6d-4074">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4074">An Integer that specifies the height in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4075">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4075">Return Value</span></span>

<span data-ttu-id="07b6d-4076">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4076">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4077">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4077">Remarks</span></span>

<span data-ttu-id="07b6d-4078">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4078">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="07b6d-4079">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="07b6d-4079">Method helpField</span></span>

<span data-ttu-id="07b6d-4080">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4080">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4081">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4081">Return Value</span></span>

<span data-ttu-id="07b6d-4082">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4082">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4083">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4083">Remarks</span></span>

<span data-ttu-id="07b6d-4084">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4084">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="07b6d-4085">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4085">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="07b6d-4086">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="07b6d-4086">Method helpText</span></span>

<span data-ttu-id="07b6d-4087">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4087">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4088">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4088">Parameters</span></span>

<span data-ttu-id="07b6d-4089">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4089">value</span></span>  
<span data-ttu-id="07b6d-4090">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4090">The value that is assigned as the Help text for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4091">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4091">Return Value</span></span>

<span data-ttu-id="07b6d-4092">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4092">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4093">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4093">Remarks</span></span>

<span data-ttu-id="07b6d-4094">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4094">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="07b6d-4095">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4095">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="07b6d-4096">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="07b6d-4096">Method hierarchyParent</span></span>

<span data-ttu-id="07b6d-4097">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4097">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4098">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4098">Parameters</span></span>

<span data-ttu-id="07b6d-4099">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4099">value</span></span>  
<span data-ttu-id="07b6d-4100">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4100">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4101">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4101">Return Value</span></span>

<span data-ttu-id="07b6d-4102">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4102">The HierarchyParent property value of the control.</span></span>

### <a name="method-highlightactive"></a><span data-ttu-id="07b6d-4103">メソッド highlightActive</span><span class="sxs-lookup"><span data-stu-id="07b6d-4103">Method highlightActive</span></span>

    public boolean highlightActive([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4104">Parameters</span></span>

<span data-ttu-id="07b6d-4105">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4105">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4106">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4106">Return Value</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="07b6d-4107">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="07b6d-4107">Method hWnd</span></span>

<span data-ttu-id="07b6d-4108">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4108">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4109">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4109">Return Value</span></span>

<span data-ttu-id="07b6d-4110">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4110">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4111">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4111">Remarks</span></span>

<span data-ttu-id="07b6d-4112">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4112">The handle can be used with the Windows API.</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="07b6d-4113">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="07b6d-4113">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4114">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4114">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="07b6d-4115">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="07b6d-4115">Method isDisplayed</span></span>

<span data-ttu-id="07b6d-4116">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4116">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4117">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4117">Return Value</span></span>

<span data-ttu-id="07b6d-4118">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4118">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4119">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4119">Remarks</span></span>

<span data-ttu-id="07b6d-4120">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4120">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="07b6d-4121">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="07b6d-4121">Method isRestricted</span></span>

<span data-ttu-id="07b6d-4122">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4122">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4123">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4123">Return Value</span></span>

<span data-ttu-id="07b6d-4124">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4124">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="07b6d-4125">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="07b6d-4125">Method isUserSetupEnabled</span></span>

<span data-ttu-id="07b6d-4126">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4126">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4127">Parameters</span></span>

<span data-ttu-id="07b6d-4128">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="07b6d-4128">neededSetupRights</span></span>  
<span data-ttu-id="07b6d-4129">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4129">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4130">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4130">Return Value</span></span>

<span data-ttu-id="07b6d-4131">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4131">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="07b6d-4132">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4132">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4133">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4133">Remarks</span></span>

<span data-ttu-id="07b6d-4134">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4134">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-4135">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="07b6d-4135">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="07b6d-4136">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4136">No changes can be made to the control.</span></span> <span data-ttu-id="07b6d-4137">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4137">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="07b6d-4138">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="07b6d-4138">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="07b6d-4139">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4139">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="07b6d-4140">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4140">The user cannot move the control.</span></span>   |
| <span data-ttu-id="07b6d-4141">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="07b6d-4141">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="07b6d-4142">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4142">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="07b6d-4143">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4143">The user can also move the control.</span></span> |

### <a name="method-leave"></a><span data-ttu-id="07b6d-4144">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="07b6d-4144">Method leave</span></span>

    public boolean leave()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4145">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4145">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="07b6d-4146">メソッド left</span><span class="sxs-lookup"><span data-stu-id="07b6d-4146">Method left</span></span>

<span data-ttu-id="07b6d-4147">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4147">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4148">Parameters</span></span>

<span data-ttu-id="07b6d-4149">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4149">value</span></span>  
<span data-ttu-id="07b6d-4150">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4150">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4151">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4151">mode</span></span>  
<span data-ttu-id="07b6d-4152">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4152">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4153">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4153">Return Value</span></span>

<span data-ttu-id="07b6d-4154">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4154">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="07b6d-4155">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="07b6d-4155">Method leftMargin</span></span>

    public int leftMargin([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4156">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4156">Parameters</span></span>

<span data-ttu-id="07b6d-4157">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4157">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4158">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4158">Return Value</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="07b6d-4159">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4159">Method leftMode</span></span>

<span data-ttu-id="07b6d-4160">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4160">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4161">Parameters</span></span>

<span data-ttu-id="07b6d-4162">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4162">value</span></span>  
<span data-ttu-id="07b6d-4163">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4163">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4164">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4164">Return Value</span></span>

<span data-ttu-id="07b6d-4165">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4165">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="07b6d-4166">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-4166">Method leftValue</span></span>

<span data-ttu-id="07b6d-4167">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4167">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4168">Parameters</span></span>

<span data-ttu-id="07b6d-4169">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4169">value</span></span>  
<span data-ttu-id="07b6d-4170">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4170">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4171">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4171">Return Value</span></span>

<span data-ttu-id="07b6d-4172">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4172">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="07b6d-4173">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="07b6d-4173">Method markAsUserAdd</span></span>

<span data-ttu-id="07b6d-4174">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4174">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4175">Parameters</span></span>

<span data-ttu-id="07b6d-4176">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4176">value</span></span>  
<span data-ttu-id="07b6d-4177">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4177">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4178">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4178">Return Value</span></span>

<span data-ttu-id="07b6d-4179">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4179">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-morerowsindicator"></a><span data-ttu-id="07b6d-4180">メソッド moreRowsIndicator</span><span class="sxs-lookup"><span data-stu-id="07b6d-4180">Method moreRowsIndicator</span></span>

    public int moreRowsIndicator([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4181">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4181">Parameters</span></span>

<span data-ttu-id="07b6d-4182">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4182">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4183">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4183">Return Value</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="07b6d-4184">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="07b6d-4184">Method mouseDblClick</span></span>

<span data-ttu-id="07b6d-4185">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4185">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4186">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4186">Parameters</span></span>

<span data-ttu-id="07b6d-4187">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-4187">x</span></span>  
<span data-ttu-id="07b6d-4188">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4188">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4189">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-4189">y</span></span>  
<span data-ttu-id="07b6d-4190">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4190">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4191">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-4191">button</span></span>  
<span data-ttu-id="07b6d-4192">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4192">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4193">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-4193">Ctrl</span></span>  
<span data-ttu-id="07b6d-4194">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4194">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4195">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-4195">Shift</span></span>  
<span data-ttu-id="07b6d-4196">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4196">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4197">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4197">Return Value</span></span>

<span data-ttu-id="07b6d-4198">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4198">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4199">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4199">Remarks</span></span>

<span data-ttu-id="07b6d-4200">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4200">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="07b6d-4201">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="07b6d-4201">Method mouseDown</span></span>

<span data-ttu-id="07b6d-4202">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4202">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4203">Parameters</span></span>

<span data-ttu-id="07b6d-4204">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-4204">x</span></span>  
<span data-ttu-id="07b6d-4205">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4205">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4206">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-4206">y</span></span>  
<span data-ttu-id="07b6d-4207">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4207">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4208">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-4208">button</span></span>  
<span data-ttu-id="07b6d-4209">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4209">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4210">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-4210">Ctrl</span></span>  
<span data-ttu-id="07b6d-4211">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4211">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4212">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-4212">Shift</span></span>  
<span data-ttu-id="07b6d-4213">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4213">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4214">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4214">Return Value</span></span>

<span data-ttu-id="07b6d-4215">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4215">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4216">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4216">Remarks</span></span>

<span data-ttu-id="07b6d-4217">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4217">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="07b6d-4218">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4218">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="07b6d-4219">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="07b6d-4219">Method mouseMove</span></span>

<span data-ttu-id="07b6d-4220">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4220">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4221">Parameters</span></span>

<span data-ttu-id="07b6d-4222">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-4222">x</span></span>  
<span data-ttu-id="07b6d-4223">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4223">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4224">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-4224">y</span></span>  
<span data-ttu-id="07b6d-4225">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4225">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4226">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-4226">button</span></span>  
<span data-ttu-id="07b6d-4227">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4227">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4228">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-4228">Ctrl</span></span>  
<span data-ttu-id="07b6d-4229">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4229">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4230">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-4230">Shift</span></span>  
<span data-ttu-id="07b6d-4231">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4231">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4232">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4232">Return Value</span></span>

<span data-ttu-id="07b6d-4233">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4233">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4234">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4234">Remarks</span></span>

<span data-ttu-id="07b6d-4235">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4235">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="07b6d-4236">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="07b6d-4236">Method mouseUp</span></span>

<span data-ttu-id="07b6d-4237">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4237">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4238">Parameters</span></span>

<span data-ttu-id="07b6d-4239">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-4239">x</span></span>  
<span data-ttu-id="07b6d-4240">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4240">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4241">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-4241">y</span></span>  
<span data-ttu-id="07b6d-4242">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4242">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4243">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-4243">button</span></span>  
<span data-ttu-id="07b6d-4244">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4244">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4245">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-4245">Ctrl</span></span>  
<span data-ttu-id="07b6d-4246">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4246">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4247">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-4247">Shift</span></span>  
<span data-ttu-id="07b6d-4248">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4248">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4249">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4249">Return Value</span></span>

<span data-ttu-id="07b6d-4250">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4250">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4251">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4251">Remarks</span></span>

<span data-ttu-id="07b6d-4252">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4252">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="07b6d-4253">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4253">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-movecontrol"></a><span data-ttu-id="07b6d-4254">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-4254">Method moveControl</span></span>

    public int moveControl(int controlId, [int insertAfterId])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4255">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4255">Parameters</span></span>

<span data-ttu-id="07b6d-4256">controlId</span><span class="sxs-lookup"><span data-stu-id="07b6d-4256">controlId</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4257">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="07b6d-4257">insertAfterId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4258">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4258">Return Value</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="07b6d-4259">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="07b6d-4259">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4260">Parameters</span></span>

<span data-ttu-id="07b6d-4261">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4261">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4262">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4262">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="07b6d-4263">メソッド名</span><span class="sxs-lookup"><span data-stu-id="07b6d-4263">Method name</span></span>

<span data-ttu-id="07b6d-4264">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4264">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4265">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4265">Parameters</span></span>

<span data-ttu-id="07b6d-4266">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4266">value</span></span>  
<span data-ttu-id="07b6d-4267">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4267">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4268">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4268">Return Value</span></span>

<span data-ttu-id="07b6d-4269">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4269">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4270">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4270">Remarks</span></span>

<span data-ttu-id="07b6d-4271">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4271">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="07b6d-4272">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4272">It must begin with a letter.</span></span>
-   <span data-ttu-id="07b6d-4273">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4273">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="07b6d-4274">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4274">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="07b6d-4275">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4275">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="07b6d-4276">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4276">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="07b6d-4277">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="07b6d-4277">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4278">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4278">Parameters</span></span>

<span data-ttu-id="07b6d-4279">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4279">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4280">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4280">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="07b6d-4281">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="07b6d-4281">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4282">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4282">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="07b6d-4283">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-4283">Method parentControl</span></span>

<span data-ttu-id="07b6d-4284">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4284">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4285">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4285">Return Value</span></span>

<span data-ttu-id="07b6d-4286">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4286">The parent control for the control.</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="07b6d-4287">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="07b6d-4287">Method rightMargin</span></span>

    public int rightMargin([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4288">Parameters</span></span>

<span data-ttu-id="07b6d-4289">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4289">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4290">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4290">Return Value</span></span>

### <a name="method-scrollbars"></a><span data-ttu-id="07b6d-4291">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="07b6d-4291">Method scrollbars</span></span>

    public int scrollbars([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4292">Parameters</span></span>

<span data-ttu-id="07b6d-4293">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4293">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4294">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4294">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="07b6d-4295">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="07b6d-4295">Method securityKey</span></span>

<span data-ttu-id="07b6d-4296">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4296">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4297">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4297">Parameters</span></span>

<span data-ttu-id="07b6d-4298">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4298">value</span></span>  
<span data-ttu-id="07b6d-4299">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4299">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4300">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4300">Return Value</span></span>

<span data-ttu-id="07b6d-4301">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4301">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-showcollabels"></a><span data-ttu-id="07b6d-4302">メソッド showColLabels</span><span class="sxs-lookup"><span data-stu-id="07b6d-4302">Method showColLabels</span></span>

    public boolean showColLabels([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4303">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4303">Parameters</span></span>

<span data-ttu-id="07b6d-4304">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4304">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4305">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4305">Return Value</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="07b6d-4306">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="07b6d-4306">Method showContextMenu</span></span>

<span data-ttu-id="07b6d-4307">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4307">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4308">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4308">Parameters</span></span>

<span data-ttu-id="07b6d-4309">menuHandle</span><span class="sxs-lookup"><span data-stu-id="07b6d-4309">menuHandle</span></span>  
<span data-ttu-id="07b6d-4310">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4310">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4311">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4311">Return Value</span></span>

<span data-ttu-id="07b6d-4312">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4312">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-showrowlabels"></a><span data-ttu-id="07b6d-4313">メソッド showRowLabels</span><span class="sxs-lookup"><span data-stu-id="07b6d-4313">Method showRowLabels</span></span>

    public boolean showRowLabels([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4314">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4314">Parameters</span></span>

<span data-ttu-id="07b6d-4315">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4315">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4316">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4316">Return Value</span></span>

### <a name="method-skip"></a><span data-ttu-id="07b6d-4317">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="07b6d-4317">Method skip</span></span>

<span data-ttu-id="07b6d-4318">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4318">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4319">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4319">Parameters</span></span>

<span data-ttu-id="07b6d-4320">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4320">value</span></span>  
<span data-ttu-id="07b6d-4321">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4321">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4322">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4322">Return Value</span></span>

<span data-ttu-id="07b6d-4323">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4323">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="method-sort"></a><span data-ttu-id="07b6d-4324">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="07b6d-4324">Method sort</span></span>

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4325">Parameters</span></span>

<span data-ttu-id="07b6d-4326">sortDirection</span><span class="sxs-lookup"><span data-stu-id="07b6d-4326">sortDirection</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4327">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4327">Return Value</span></span>

### <a name="method-style"></a><span data-ttu-id="07b6d-4328">メソッド style</span><span class="sxs-lookup"><span data-stu-id="07b6d-4328">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4329">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4329">Parameters</span></span>

<span data-ttu-id="07b6d-4330">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4330">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4331">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4331">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="07b6d-4332">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="07b6d-4332">Method toolTip</span></span>

<span data-ttu-id="07b6d-4333">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4333">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="07b6d-4334">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4334">Return Value</span></span>

<span data-ttu-id="07b6d-4335">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4335">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4336">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4336">Remarks</span></span>

<span data-ttu-id="07b6d-4337">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4337">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="07b6d-4338">メソッド top</span><span class="sxs-lookup"><span data-stu-id="07b6d-4338">Method top</span></span>

<span data-ttu-id="07b6d-4339">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4339">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4340">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4340">Parameters</span></span>

<span data-ttu-id="07b6d-4341">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4341">value</span></span>  
<span data-ttu-id="07b6d-4342">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4342">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4343">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4343">mode</span></span>  
<span data-ttu-id="07b6d-4344">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4344">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4345">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4345">Return Value</span></span>

<span data-ttu-id="07b6d-4346">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4346">The vertical position of the control in the form.</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="07b6d-4347">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="07b6d-4347">Method topMargin</span></span>

    public int topMargin([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4348">Parameters</span></span>

<span data-ttu-id="07b6d-4349">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4349">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4350">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4350">Return Value</span></span>

### <a name="method-topmode"></a><span data-ttu-id="07b6d-4351">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4351">Method topMode</span></span>

<span data-ttu-id="07b6d-4352">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4352">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4353">Parameters</span></span>

<span data-ttu-id="07b6d-4354">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4354">value</span></span>  
<span data-ttu-id="07b6d-4355">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4355">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4356">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4356">Return Value</span></span>

<span data-ttu-id="07b6d-4357">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4357">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="07b6d-4358">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-4358">Method topValue</span></span>

<span data-ttu-id="07b6d-4359">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4359">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4360">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4360">Parameters</span></span>

<span data-ttu-id="07b6d-4361">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4361">value</span></span>  
<span data-ttu-id="07b6d-4362">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4362">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4363">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4363">Return Value</span></span>

<span data-ttu-id="07b6d-4364">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4364">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="07b6d-4365">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="07b6d-4365">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4366">Parameters</span></span>

<span data-ttu-id="07b6d-4367">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4368">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4368">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="07b6d-4369">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="07b6d-4369">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4370">Parameters</span></span>

<span data-ttu-id="07b6d-4371">データ</span><span class="sxs-lookup"><span data-stu-id="07b6d-4371">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4372">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4372">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="07b6d-4373">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="07b6d-4373">Method userData</span></span>

<span data-ttu-id="07b6d-4374">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4374">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4375">Parameters</span></span>

<span data-ttu-id="07b6d-4376">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4376">value</span></span>  
<span data-ttu-id="07b6d-4377">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4377">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4378">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4378">Return Value</span></span>

<span data-ttu-id="07b6d-4379">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4379">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="07b6d-4380">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="07b6d-4380">Method userDataItem</span></span>

<span data-ttu-id="07b6d-4381">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4381">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4382">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4382">Parameters</span></span>

<span data-ttu-id="07b6d-4383">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4383">value</span></span>  
<span data-ttu-id="07b6d-4384">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4384">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4385">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4385">Return Value</span></span>

<span data-ttu-id="07b6d-4386">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4386">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="07b6d-4387">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="07b6d-4387">Method userDataItems</span></span>

<span data-ttu-id="07b6d-4388">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4388">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4389">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4389">Parameters</span></span>

<span data-ttu-id="07b6d-4390">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4390">value</span></span>  
<span data-ttu-id="07b6d-4391">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4391">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4392">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4392">Return Value</span></span>

<span data-ttu-id="07b6d-4393">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4393">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="07b6d-4394">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="07b6d-4394">Method userDisable</span></span>

<span data-ttu-id="07b6d-4395">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4395">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4396">Parameters</span></span>

<span data-ttu-id="07b6d-4397">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4397">value</span></span>  
<span data-ttu-id="07b6d-4398">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4398">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4399">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4399">Return Value</span></span>

<span data-ttu-id="07b6d-4400">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4400">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="07b6d-4401">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="07b6d-4401">Method userHeight</span></span>

<span data-ttu-id="07b6d-4402">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4402">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4403">Parameters</span></span>

<span data-ttu-id="07b6d-4404">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4404">value</span></span>  
<span data-ttu-id="07b6d-4405">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4405">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4406">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4406">Return Value</span></span>

<span data-ttu-id="07b6d-4407">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4407">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="07b6d-4408">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="07b6d-4408">Method userHide</span></span>

<span data-ttu-id="07b6d-4409">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4409">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4410">Parameters</span></span>

<span data-ttu-id="07b6d-4411">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4411">value</span></span>  
<span data-ttu-id="07b6d-4412">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4412">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4413">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4413">Return Value</span></span>

<span data-ttu-id="07b6d-4414">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4414">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4415">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4415">Remarks</span></span>

<span data-ttu-id="07b6d-4416">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4416">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="07b6d-4417">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4417">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="07b6d-4418">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4418">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="07b6d-4419">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="07b6d-4419">Method userOrgContainer</span></span>

<span data-ttu-id="07b6d-4420">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4420">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4421">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4421">Parameters</span></span>

<span data-ttu-id="07b6d-4422">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4422">value</span></span>  
<span data-ttu-id="07b6d-4423">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4423">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4424">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4424">Return Value</span></span>

<span data-ttu-id="07b6d-4425">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4425">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="07b6d-4426">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="07b6d-4426">Method userOrgSibling</span></span>

<span data-ttu-id="07b6d-4427">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4427">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4428">Parameters</span></span>

<span data-ttu-id="07b6d-4429">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4429">value</span></span>  
<span data-ttu-id="07b6d-4430">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4430">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4431">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4431">Return Value</span></span>

<span data-ttu-id="07b6d-4432">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4432">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="07b6d-4433">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="07b6d-4433">Method userPromptText</span></span>

<span data-ttu-id="07b6d-4434">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4434">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4435">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4435">Parameters</span></span>

<span data-ttu-id="07b6d-4436">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4436">value</span></span>  
<span data-ttu-id="07b6d-4437">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4437">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4438">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4438">Return Value</span></span>

<span data-ttu-id="07b6d-4439">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4439">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="07b6d-4440">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="07b6d-4440">Method userSecurityLevel</span></span>

<span data-ttu-id="07b6d-4441">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4441">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4442">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4442">Parameters</span></span>

<span data-ttu-id="07b6d-4443">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4443">value</span></span>  
<span data-ttu-id="07b6d-4444">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4444">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4445">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4445">Return Value</span></span>

<span data-ttu-id="07b6d-4446">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4446">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="07b6d-4447">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="07b6d-4447">Method userSkip</span></span>

<span data-ttu-id="07b6d-4448">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4448">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4449">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4449">Parameters</span></span>

<span data-ttu-id="07b6d-4450">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4450">value</span></span>  
<span data-ttu-id="07b6d-4451">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4451">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="07b6d-4452">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4452">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4453">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4453">Return Value</span></span>

<span data-ttu-id="07b6d-4454">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4454">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="07b6d-4455">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="07b6d-4455">Method userWidth</span></span>

<span data-ttu-id="07b6d-4456">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4456">Sets or returns the width of the control in pixels.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4457">Parameters</span></span>

<span data-ttu-id="07b6d-4458">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4458">value</span></span>  
<span data-ttu-id="07b6d-4459">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4459">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4460">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4460">Return Value</span></span>

<span data-ttu-id="07b6d-4461">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4461">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4462">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4462">Remarks</span></span>

<span data-ttu-id="07b6d-4463">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4463">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="07b6d-4464">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4464">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="07b6d-4465">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4465">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-useuserlayout"></a><span data-ttu-id="07b6d-4466">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="07b6d-4466">Method useUserLayout</span></span>

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4467">Parameters</span></span>

<span data-ttu-id="07b6d-4468">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4468">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4469">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4469">Return Value</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="07b6d-4470">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="07b6d-4470">Method verticalSpacing</span></span>

<span data-ttu-id="07b6d-4471">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4471">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4472">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4472">Parameters</span></span>

<span data-ttu-id="07b6d-4473">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4473">value</span></span>  
<span data-ttu-id="07b6d-4474">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4474">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4475">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4475">mode</span></span>  
<span data-ttu-id="07b6d-4476">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4476">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4477">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4477">Return Value</span></span>

<span data-ttu-id="07b6d-4478">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4478">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="07b6d-4479">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4479">Method verticalSpacingMode</span></span>

<span data-ttu-id="07b6d-4480">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4480">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4481">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4481">Parameters</span></span>

<span data-ttu-id="07b6d-4482">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4482">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4483">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4483">Return Value</span></span>

<span data-ttu-id="07b6d-4484">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4484">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="07b6d-4485">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-4485">Method verticalSpacingValue</span></span>

<span data-ttu-id="07b6d-4486">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4486">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4487">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4487">Parameters</span></span>

<span data-ttu-id="07b6d-4488">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4488">value</span></span>  
<span data-ttu-id="07b6d-4489">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4489">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4490">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4490">Return Value</span></span>

<span data-ttu-id="07b6d-4491">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4491">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="07b6d-4492">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="07b6d-4492">Method visible</span></span>

<span data-ttu-id="07b6d-4493">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4493">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4494">Parameters</span></span>

<span data-ttu-id="07b6d-4495">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4495">value</span></span>  
<span data-ttu-id="07b6d-4496">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4496">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4497">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4497">Return Value</span></span>

<span data-ttu-id="07b6d-4498">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4498">true if the control is visible; otherwise, false.</span></span>

### <a name="method-visiblecols"></a><span data-ttu-id="07b6d-4499">メソッド visibleCols</span><span class="sxs-lookup"><span data-stu-id="07b6d-4499">Method visibleCols</span></span>

    public int visibleCols([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4500">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4500">Parameters</span></span>

<span data-ttu-id="07b6d-4501">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4501">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4502">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4502">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4503">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4503">Return Value</span></span>

### <a name="method-visiblecolsmode"></a><span data-ttu-id="07b6d-4504">メソッド visibleColsMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4504">Method visibleColsMode</span></span>

    public AutoMode visibleColsMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4505">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4505">Parameters</span></span>

<span data-ttu-id="07b6d-4506">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4506">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4507">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4507">Return Value</span></span>

### <a name="method-visiblecolsvalue"></a><span data-ttu-id="07b6d-4508">メソッド visibleColsValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-4508">Method visibleColsValue</span></span>

    public int visibleColsValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4509">Parameters</span></span>

<span data-ttu-id="07b6d-4510">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4510">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4511">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4511">Return Value</span></span>

### <a name="method-visiblerows"></a><span data-ttu-id="07b6d-4512">メソッド visibleRows</span><span class="sxs-lookup"><span data-stu-id="07b6d-4512">Method visibleRows</span></span>

    public int visibleRows([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4513">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4513">Parameters</span></span>

<span data-ttu-id="07b6d-4514">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4514">value</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4515">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4515">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4516">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4516">Return Value</span></span>

### <a name="method-visiblerowsmode"></a><span data-ttu-id="07b6d-4517">メソッド visibleRowsMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4517">Method visibleRowsMode</span></span>

    public AutoMode visibleRowsMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4518">Parameters</span></span>

<span data-ttu-id="07b6d-4519">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4519">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4520">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4520">Return Value</span></span>

### <a name="method-visiblerowsvalue"></a><span data-ttu-id="07b6d-4521">メソッド visibleRowsValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-4521">Method visibleRowsValue</span></span>

    public int visibleRowsValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4522">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4522">Parameters</span></span>

<span data-ttu-id="07b6d-4523">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4523">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="07b6d-4524">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4524">Return Value</span></span>

### <a name="method-width"></a><span data-ttu-id="07b6d-4525">メソッド width</span><span class="sxs-lookup"><span data-stu-id="07b6d-4525">Method width</span></span>

<span data-ttu-id="07b6d-4526">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4526">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4527">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4527">Parameters</span></span>

<span data-ttu-id="07b6d-4528">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4528">value</span></span>  
<span data-ttu-id="07b6d-4529">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4529">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4530">モード</span><span class="sxs-lookup"><span data-stu-id="07b6d-4530">mode</span></span>  
<span data-ttu-id="07b6d-4531">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4531">An Integer that indicates how the width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4532">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4532">Return Value</span></span>

<span data-ttu-id="07b6d-4533">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4533">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4534">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4534">Remarks</span></span>

<span data-ttu-id="07b6d-4535">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4535">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="07b6d-4536">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-4536">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="07b6d-4537">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4537">Mode.</span></span>           | <span data-ttu-id="07b6d-4538">幅計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4538">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-4539">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4539">-1 Exact.</span></span>       | <span data-ttu-id="07b6d-4540">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4540">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-4541">0 自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4541">0 Auto.</span></span>         | <span data-ttu-id="07b6d-4542">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4542">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-4543">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4543">1 Column width.</span></span> | <span data-ttu-id="07b6d-4544">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4544">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="07b6d-4545">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4545">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="07b6d-4546">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4546">Method widthMode</span></span>

<span data-ttu-id="07b6d-4547">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4547">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4548">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4548">Parameters</span></span>

<span data-ttu-id="07b6d-4549">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4549">value</span></span>  
<span data-ttu-id="07b6d-4550">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4550">An integer value that indicates how control width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4551">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4551">Return Value</span></span>

<span data-ttu-id="07b6d-4552">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4552">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4553">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4553">Remarks</span></span>

<span data-ttu-id="07b6d-4554">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="07b6d-4554">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="07b6d-4555">モード。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4555">Mode.</span></span>         | <span data-ttu-id="07b6d-4556">幅計算。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4556">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b6d-4557">正確。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4557">Exact.</span></span>        | <span data-ttu-id="07b6d-4558">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4558">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="07b6d-4559">自動。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4559">Auto.</span></span>         | <span data-ttu-id="07b6d-4560">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4560">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="07b6d-4561">列の幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4561">Column width.</span></span> | <span data-ttu-id="07b6d-4562">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4562">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="07b6d-4563">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4563">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="07b6d-4564">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-4564">Method widthValue</span></span>

<span data-ttu-id="07b6d-4565">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4565">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4566">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4566">Parameters</span></span>

<span data-ttu-id="07b6d-4567">値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4567">value</span></span>  
<span data-ttu-id="07b6d-4568">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4568">An Integer that specifies the width in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07b6d-4569">戻り値</span><span class="sxs-lookup"><span data-stu-id="07b6d-4569">Return Value</span></span>

<span data-ttu-id="07b6d-4570">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4570">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="07b6d-4571">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4571">Remarks</span></span>

<span data-ttu-id="07b6d-4572">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4572">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-cut"></a><span data-ttu-id="07b6d-4573">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="07b6d-4573">Method cut</span></span>

<span data-ttu-id="07b6d-4574">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4574">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-applyquickfilter"></a><span data-ttu-id="07b6d-4575">メソッド applyQuickFilter</span><span class="sxs-lookup"><span data-stu-id="07b6d-4575">Method applyQuickFilter</span></span>

    public void applyQuickFilter([int controlId], [str filterValue])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4576">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4576">Parameters</span></span>

<span data-ttu-id="07b6d-4577">controlId</span><span class="sxs-lookup"><span data-stu-id="07b6d-4577">controlId</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4578">filterValue</span><span class="sxs-lookup"><span data-stu-id="07b6d-4578">filterValue</span></span>  

### <a name="method-autosizecolumns"></a><span data-ttu-id="07b6d-4579">メソッド autoSizeColumns</span><span class="sxs-lookup"><span data-stu-id="07b6d-4579">Method autoSizeColumns</span></span>

    public void autoSizeColumns([boolean autoSizeColumns])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4580">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4580">Parameters</span></span>

<span data-ttu-id="07b6d-4581">autoSizeColumns</span><span class="sxs-lookup"><span data-stu-id="07b6d-4581">autoSizeColumns</span></span>  

### <a name="method-drop"></a><span data-ttu-id="07b6d-4582">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="07b6d-4582">Method drop</span></span>

<span data-ttu-id="07b6d-4583">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4583">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4584">Parameters</span></span>

<span data-ttu-id="07b6d-4585">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-4585">dragSource</span></span>  
<span data-ttu-id="07b6d-4586">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4586">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4587">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4587">dragMode</span></span>  
<span data-ttu-id="07b6d-4588">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4588">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4589">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-4589">x</span></span>  
<span data-ttu-id="07b6d-4590">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4590">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4591">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-4591">y</span></span>  
<span data-ttu-id="07b6d-4592">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4592">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-context"></a><span data-ttu-id="07b6d-4593">メソッド context</span><span class="sxs-lookup"><span data-stu-id="07b6d-4593">Method context</span></span>

<span data-ttu-id="07b6d-4594">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4594">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-jumpref"></a><span data-ttu-id="07b6d-4595">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="07b6d-4595">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-onlookup"></a><span data-ttu-id="07b6d-4596">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="07b6d-4596">Method OnLookup</span></span>

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4597">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4597">Parameters</span></span>

<span data-ttu-id="07b6d-4598">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-4598">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4599">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-4599">e</span></span>  

### <a name="method-onlostfocus"></a><span data-ttu-id="07b6d-4600">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-4600">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4601">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4601">Parameters</span></span>

<span data-ttu-id="07b6d-4602">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-4602">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4603">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-4603">e</span></span>  

### <a name="method-registeroverridemethod"></a><span data-ttu-id="07b6d-4604">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="07b6d-4604">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4605">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4605">Parameters</span></span>

<span data-ttu-id="07b6d-4606">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="07b6d-4606">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4607">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="07b6d-4607">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4608">overrideObject</span><span class="sxs-lookup"><span data-stu-id="07b6d-4608">overrideObject</span></span>  

### <a name="method-copy"></a><span data-ttu-id="07b6d-4609">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="07b6d-4609">Method copy</span></span>

<span data-ttu-id="07b6d-4610">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4610">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-enter"></a><span data-ttu-id="07b6d-4611">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="07b6d-4611">Method enter</span></span>

    public void enter()

### <a name="method-mouseenter"></a><span data-ttu-id="07b6d-4612">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="07b6d-4612">Method mouseEnter</span></span>

<span data-ttu-id="07b6d-4613">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4613">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4614">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4614">Parameters</span></span>

<span data-ttu-id="07b6d-4615">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-4615">x</span></span>  
<span data-ttu-id="07b6d-4616">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4616">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4617">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-4617">y</span></span>  
<span data-ttu-id="07b6d-4618">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4618">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4619">ボタン</span><span class="sxs-lookup"><span data-stu-id="07b6d-4619">button</span></span>  
<span data-ttu-id="07b6d-4620">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4620">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4621">Ctrl</span><span class="sxs-lookup"><span data-stu-id="07b6d-4621">Ctrl</span></span>  
<span data-ttu-id="07b6d-4622">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4622">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4623">シフト</span><span class="sxs-lookup"><span data-stu-id="07b6d-4623">Shift</span></span>  
<span data-ttu-id="07b6d-4624">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4624">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-displaycontrol"></a><span data-ttu-id="07b6d-4625">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="07b6d-4625">Method displayControl</span></span>

<span data-ttu-id="07b6d-4626">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4626">Displays the control.</span></span>

    public void displayControl()

### <a name="method-onleaving"></a><span data-ttu-id="07b6d-4627">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="07b6d-4627">Method OnLeaving</span></span>

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4628">Parameters</span></span>

<span data-ttu-id="07b6d-4629">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-4629">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4630">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-4630">e</span></span>  

### <a name="method-paste"></a><span data-ttu-id="07b6d-4631">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="07b6d-4631">Method paste</span></span>

<span data-ttu-id="07b6d-4632">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4632">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-resetusersetting"></a><span data-ttu-id="07b6d-4633">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="07b6d-4633">Method resetUserSetting</span></span>

<span data-ttu-id="07b6d-4634">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4634">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-quickfilterprovider"></a><span data-ttu-id="07b6d-4635">メソッド quickFilterProvider</span><span class="sxs-lookup"><span data-stu-id="07b6d-4635">Method quickFilterProvider</span></span>

    public void quickFilterProvider([GridQuickFilterProvider quickFilterProvider])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4636">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4636">Parameters</span></span>

<span data-ttu-id="07b6d-4637">quickFilterProvider</span><span class="sxs-lookup"><span data-stu-id="07b6d-4637">quickFilterProvider</span></span>  

### <a name="method-dropex"></a><span data-ttu-id="07b6d-4638">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="07b6d-4638">Method dropEx</span></span>

<span data-ttu-id="07b6d-4639">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4639">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4640">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4640">Parameters</span></span>

<span data-ttu-id="07b6d-4641">dragSource</span><span class="sxs-lookup"><span data-stu-id="07b6d-4641">dragSource</span></span>  
<span data-ttu-id="07b6d-4642">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4642">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4643">dragMode</span><span class="sxs-lookup"><span data-stu-id="07b6d-4643">dragMode</span></span>  
<span data-ttu-id="07b6d-4644">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4644">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4645">x</span><span class="sxs-lookup"><span data-stu-id="07b6d-4645">x</span></span>  
<span data-ttu-id="07b6d-4646">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4646">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4647">y</span><span class="sxs-lookup"><span data-stu-id="07b6d-4647">y</span></span>  
<span data-ttu-id="07b6d-4648">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4648">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-onenter"></a><span data-ttu-id="07b6d-4649">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="07b6d-4649">Method OnEnter</span></span>

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4650">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4650">Parameters</span></span>

<span data-ttu-id="07b6d-4651">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-4651">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4652">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-4652">e</span></span>  

### <a name="method-inputsearch"></a><span data-ttu-id="07b6d-4653">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="07b6d-4653">Method inputSearch</span></span>

<span data-ttu-id="07b6d-4654">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4654">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4655">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4655">Parameters</span></span>

<span data-ttu-id="07b6d-4656">searchStr</span><span class="sxs-lookup"><span data-stu-id="07b6d-4656">searchStr</span></span>  
<span data-ttu-id="07b6d-4657">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4657">The string value to use to filter data; optional.</span></span>

### <a name="method-filter"></a><span data-ttu-id="07b6d-4658">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="07b6d-4658">Method filter</span></span>

    public void filter([str filterStr])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4659">Parameters</span></span>

<span data-ttu-id="07b6d-4660">filterStr</span><span class="sxs-lookup"><span data-stu-id="07b6d-4660">filterStr</span></span>  

### <a name="method-prefcolumnsize"></a><span data-ttu-id="07b6d-4661">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="07b6d-4661">Method prefColumnSize</span></span>

<span data-ttu-id="07b6d-4662">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4662">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="07b6d-4663">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4663">Parameters</span></span>

<span data-ttu-id="07b6d-4664">width</span><span class="sxs-lookup"><span data-stu-id="07b6d-4664">width</span></span>  
<span data-ttu-id="07b6d-4665">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4665">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="07b6d-4666">height</span><span class="sxs-lookup"><span data-stu-id="07b6d-4666">height</span></span>  
<span data-ttu-id="07b6d-4667">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4667">The preferred height of the control.</span></span>

### <a name="method-dragleave"></a><span data-ttu-id="07b6d-4668">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="07b6d-4668">Method dragLeave</span></span>

<span data-ttu-id="07b6d-4669">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4669">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-ongotfocus"></a><span data-ttu-id="07b6d-4670">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-4670">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="07b6d-4671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07b6d-4671">Parameters</span></span>

<span data-ttu-id="07b6d-4672">sender</span><span class="sxs-lookup"><span data-stu-id="07b6d-4672">sender</span></span>  

<!-- -->

<span data-ttu-id="07b6d-4673">e</span><span class="sxs-lookup"><span data-stu-id="07b6d-4673">e</span></span>  

### <a name="method-lostfocus"></a><span data-ttu-id="07b6d-4674">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-4674">Method lostFocus</span></span>

<span data-ttu-id="07b6d-4675">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4675">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-enddrag"></a><span data-ttu-id="07b6d-4676">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="07b6d-4676">Method endDrag</span></span>

<span data-ttu-id="07b6d-4677">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4677">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="07b6d-4678">備考</span><span class="sxs-lookup"><span data-stu-id="07b6d-4678">Remarks</span></span>

<span data-ttu-id="07b6d-4679">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4679">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="07b6d-4680">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4680">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-arrange"></a><span data-ttu-id="07b6d-4681">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="07b6d-4681">Method arrange</span></span>

    public void arrange()

### <a name="method-gotfocus"></a><span data-ttu-id="07b6d-4682">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-4682">Method gotFocus</span></span>

<span data-ttu-id="07b6d-4683">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4683">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-mouseleave"></a><span data-ttu-id="07b6d-4684">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="07b6d-4684">Method mouseLeave</span></span>

<span data-ttu-id="07b6d-4685">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4685">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-setfocus"></a><span data-ttu-id="07b6d-4686">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="07b6d-4686">Method setFocus</span></span>

<span data-ttu-id="07b6d-4687">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="07b6d-4687">Sets the focus on the control.</span></span>

    public void setFocus()



