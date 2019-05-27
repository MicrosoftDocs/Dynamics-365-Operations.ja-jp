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
ms.openlocfilehash: ccf772ab2f05d2c24135d267ef46be264ab8dfd2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537045"
---
# <a name="f-classes-formfasttabsummaryseparator-to-formgridcontrol"></a><span data-ttu-id="de50b-103">F クラス (FormFastTabSummarySeparator から FormGridControl)</span><span class="sxs-lookup"><span data-stu-id="de50b-103">F classes (FormFastTabSummarySeparator to FormGridControl)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de50b-104">FormFastTabSummarySeparator から FormGridControl までのクラスの API 参照。</span><span class="sxs-lookup"><span data-stu-id="de50b-104">API reference for classes from FormFastTabSummarySeparator to FormGridControl.</span></span>

<a name="class-formfasttabsummaryseparator"></a><span data-ttu-id="de50b-105">クラス FormFastTabSummarySeparator</span><span class="sxs-lookup"><span data-stu-id="de50b-105">Class FormFastTabSummarySeparator</span></span>
---------------------------------

    class FormFastTabSummarySeparator extends FormControl

### <a name="remarks"></a><span data-ttu-id="de50b-106">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="de50b-107">例</span><span class="sxs-lookup"><span data-stu-id="de50b-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="de50b-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="de50b-108">Methods</span></span>

| <span data-ttu-id="de50b-109">方法</span><span class="sxs-lookup"><span data-stu-id="de50b-109">Method</span></span>                                                                                                      | <span data-ttu-id="de50b-110">説明</span><span class="sxs-lookup"><span data-stu-id="de50b-110">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="de50b-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-112">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="de50b-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-114">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-115">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="de50b-115">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="de50b-116">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-116">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="de50b-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="de50b-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="de50b-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="de50b-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="de50b-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="de50b-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="de50b-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-126">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-127">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="de50b-127">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="de50b-128">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-128">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="de50b-129">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-129">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="de50b-130">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-130">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-131">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-131">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="de50b-132">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-132">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="de50b-134">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-134">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-135">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="de50b-135">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="de50b-136">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-136">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="de50b-137">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-137">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="de50b-138">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-138">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="de50b-139">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-139">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="de50b-140">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-140">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="de50b-141">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-141">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="de50b-142">コントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-142">Gets or sets the value that indicates whether the control is displayed.</span></span> |
| <span data-ttu-id="de50b-143">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-143">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-144">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-144">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="de50b-145">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-145">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="de50b-146">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-146">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="de50b-147">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-147">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="de50b-148">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-148">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="de50b-149">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="de50b-149">public str dragText()</span></span>                                                                                       | <span data-ttu-id="de50b-150">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-150">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-151">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-151">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="de50b-152">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-152">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-153">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-153">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="de50b-154">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-154">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="de50b-155">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-155">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-156">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-156">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="de50b-157">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="de50b-157">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="de50b-158">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-158">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="de50b-159">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="de50b-159">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="de50b-160">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-160">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="de50b-161">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-161">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="de50b-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-162">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-163">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-165">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-165">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="de50b-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-166">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-167">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="de50b-167">public str helpField()</span></span>                                                                                      | <span data-ttu-id="de50b-168">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-168">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-169">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-169">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="de50b-170">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-170">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="de50b-171">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-171">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="de50b-172">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-172">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="de50b-173">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="de50b-173">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="de50b-174">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-174">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-175">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="de50b-175">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-176">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="de50b-176">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="de50b-177">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-177">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="de50b-178">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="de50b-178">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="de50b-179">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-179">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-180">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="de50b-180">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="de50b-181">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-181">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="de50b-182">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-182">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-183">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-183">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="de50b-184">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-184">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="de50b-185">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-185">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-186">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-186">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-187">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-187">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-188">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-188">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="de50b-189">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-189">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="de50b-190">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="de50b-190">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="de50b-191">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-191">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="de50b-192">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-192">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="de50b-193">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-193">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="de50b-194">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-194">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-195">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-195">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="de50b-196">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-196">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-197">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-197">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="de50b-198">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-198">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="de50b-199">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-199">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="de50b-200">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-200">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="de50b-201">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-201">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-202">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="de50b-202">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-203">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="de50b-203">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="de50b-204">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-204">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-205">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-205">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="de50b-206">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-206">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-207">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="de50b-207">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="de50b-208">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-208">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-209">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-209">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="de50b-210">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-210">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="de50b-211">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="de50b-211">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="de50b-212">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-212">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-213">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-213">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="de50b-214">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-214">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-215">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-215">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="de50b-216">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-216">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-217">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-217">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-218">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-218">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-219">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-219">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="de50b-220">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-220">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-221">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="de50b-221">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-222">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-222">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-223">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-223">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-224">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-224">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="de50b-225">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-225">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="de50b-226">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-226">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="de50b-227">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-227">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-228">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-228">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="de50b-229">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-229">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="de50b-230">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-230">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-231">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-231">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="de50b-232">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-232">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-233">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-233">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="de50b-234">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-234">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="de50b-235">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-235">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="de50b-236">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-236">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="de50b-237">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-237">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-238">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-238">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="de50b-239">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-239">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="de50b-240">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-240">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="de50b-241">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-241">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="de50b-242">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-242">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-243">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-243">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="de50b-244">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-244">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-245">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-245">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-246">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-246">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="de50b-247">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-247">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-248">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-248">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="de50b-249">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-249">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-250">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-250">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="de50b-251">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-251">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-252">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-252">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="de50b-253">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-253">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-254">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-254">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="de50b-255">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-255">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="de50b-256">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-256">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-257">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-257">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-258">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-258">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-259">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-259">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="de50b-260">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-260">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="de50b-261">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-261">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="de50b-262">public void copy()</span><span class="sxs-lookup"><span data-stu-id="de50b-262">public void copy()</span></span>                                                                                          | <span data-ttu-id="de50b-263">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="de50b-263">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="de50b-264">public void cut()</span><span class="sxs-lookup"><span data-stu-id="de50b-264">public void cut()</span></span>                                                                                           | <span data-ttu-id="de50b-265">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="de50b-265">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="de50b-266">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-266">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="de50b-267">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-267">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="de50b-268">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="de50b-268">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="de50b-269">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-269">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-270">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="de50b-270">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="de50b-271">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-271">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-272">public void context()</span><span class="sxs-lookup"><span data-stu-id="de50b-272">public void context()</span></span>                                                                                       | <span data-ttu-id="de50b-273">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-273">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-274">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-274">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="de50b-275">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-275">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="de50b-276">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="de50b-276">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="de50b-277">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-277">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="de50b-278">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-278">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="de50b-279">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-279">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="de50b-280">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="de50b-280">public void displayControl()</span></span>                                                                                | <span data-ttu-id="de50b-281">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-281">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="de50b-282">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="de50b-282">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="de50b-283">public void paste()</span><span class="sxs-lookup"><span data-stu-id="de50b-283">public void paste()</span></span>                                                                                         | <span data-ttu-id="de50b-284">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="de50b-284">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-285">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="de50b-285">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="de50b-286">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="de50b-286">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="de50b-287">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-287">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="de50b-288">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-288">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="de50b-289">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-289">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="de50b-290">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-290">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-291">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="de50b-291">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="de50b-292">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="de50b-292">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="de50b-293">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="de50b-293">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="de50b-294">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-294">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |

### <a name="method-aligncontrol"></a><span data-ttu-id="de50b-295">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="de50b-295">Method alignControl</span></span>

<span data-ttu-id="de50b-296">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-296">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-297">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-297">Parameters</span></span>

<span data-ttu-id="de50b-298">値</span><span class="sxs-lookup"><span data-stu-id="de50b-298">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-299">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-299">Return Value</span></span>

<span data-ttu-id="de50b-300">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-300">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-301">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-301">Remarks</span></span>

<span data-ttu-id="de50b-302">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-302">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="de50b-303">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="de50b-303">Method allowEdit</span></span>

<span data-ttu-id="de50b-304">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-304">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-305">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-305">Parameters</span></span>

<span data-ttu-id="de50b-306">値</span><span class="sxs-lookup"><span data-stu-id="de50b-306">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-307">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-307">Return Value</span></span>

<span data-ttu-id="de50b-308">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-308">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-309">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-309">Remarks</span></span>

<span data-ttu-id="de50b-310">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="de50b-310">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="de50b-311">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="de50b-311">Method allowSysSetup</span></span>

<span data-ttu-id="de50b-312">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-312">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="de50b-313">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-313">Return Value</span></span>

<span data-ttu-id="de50b-314">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-314">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="de50b-315">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="de50b-315">Method autoDeclaration</span></span>

<span data-ttu-id="de50b-316">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-316">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-317">Parameters</span></span>

<span data-ttu-id="de50b-318">値</span><span class="sxs-lookup"><span data-stu-id="de50b-318">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-319">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-319">Return Value</span></span>

<span data-ttu-id="de50b-320">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-320">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-321">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-321">Remarks</span></span>

<span data-ttu-id="de50b-322">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-322">Controls cannot have identical names.</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="de50b-323">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="de50b-323">Method backgroundColor</span></span>

<span data-ttu-id="de50b-324">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-324">Gets or sets the background color of the control.</span></span>

    public int backgroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-325">Parameters</span></span>

<span data-ttu-id="de50b-326">値</span><span class="sxs-lookup"><span data-stu-id="de50b-326">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-327">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-327">Return Value</span></span>

<span data-ttu-id="de50b-328">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-328">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-329">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-329">Remarks</span></span>

<span data-ttu-id="de50b-330">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-330">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="de50b-331">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de50b-331">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="de50b-332">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="de50b-332">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="de50b-333">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="de50b-333">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="de50b-334">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="de50b-334">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="de50b-335">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-335">The maximum value for a single byte is 255.</span></span>

### <a name="method-backstyle"></a><span data-ttu-id="de50b-336">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="de50b-336">Method backStyle</span></span>

<span data-ttu-id="de50b-337">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-337">Determines whether the control background can be transparent.</span></span>

    public int backStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-338">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-338">Parameters</span></span>

<span data-ttu-id="de50b-339">値</span><span class="sxs-lookup"><span data-stu-id="de50b-339">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-340">Return Value</span></span>

<span data-ttu-id="de50b-341">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-341">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="de50b-342">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="de50b-342">Method beginDrag</span></span>

<span data-ttu-id="de50b-343">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-343">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-344">Parameters</span></span>

<span data-ttu-id="de50b-345">x</span><span class="sxs-lookup"><span data-stu-id="de50b-345">x</span></span>  
<span data-ttu-id="de50b-346">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-346">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="de50b-347">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-347">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="de50b-348">y</span><span class="sxs-lookup"><span data-stu-id="de50b-348">y</span></span>  
<span data-ttu-id="de50b-349">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-349">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="de50b-350">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-350">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-351">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-351">Return Value</span></span>

<span data-ttu-id="de50b-352">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-352">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-353">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-353">Remarks</span></span>

<span data-ttu-id="de50b-354">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="de50b-354">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="de50b-355">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="de50b-355">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-bold"></a><span data-ttu-id="de50b-356">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="de50b-356">Method bold</span></span>

<span data-ttu-id="de50b-357">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-357">Gets or sets the weight of font used to output text in the control.</span></span>

    public int bold([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-358">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-358">Parameters</span></span>

<span data-ttu-id="de50b-359">値</span><span class="sxs-lookup"><span data-stu-id="de50b-359">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-360">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-360">Return Value</span></span>

<span data-ttu-id="de50b-361">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-361">An integer value between zero and nine, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-362">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-362">Remarks</span></span>

<span data-ttu-id="de50b-363">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-363">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="de50b-364">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-364">0 Use the default font weight.</span></span>
-   <span data-ttu-id="de50b-365">1 シン。</span><span class="sxs-lookup"><span data-stu-id="de50b-365">1 Thin.</span></span>
-   <span data-ttu-id="de50b-366">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="de50b-366">2 Extra-light.</span></span>
-   <span data-ttu-id="de50b-367">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="de50b-367">3 Light.</span></span>
-   <span data-ttu-id="de50b-368">4 標準。</span><span class="sxs-lookup"><span data-stu-id="de50b-368">4 Normal.</span></span>
-   <span data-ttu-id="de50b-369">5 中。</span><span class="sxs-lookup"><span data-stu-id="de50b-369">5 Medium.</span></span>
-   <span data-ttu-id="de50b-370">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="de50b-370">6 Semibold.</span></span>
-   <span data-ttu-id="de50b-371">7 太字。</span><span class="sxs-lookup"><span data-stu-id="de50b-371">7 Bold.</span></span>
-   <span data-ttu-id="de50b-372">8 極太。</span><span class="sxs-lookup"><span data-stu-id="de50b-372">8 Extra-bold.</span></span>
-   <span data-ttu-id="de50b-373">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="de50b-373">9 Heavy.</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="de50b-374">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="de50b-374">Method calcControlSize</span></span>

<span data-ttu-id="de50b-375">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-375">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="de50b-376">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-376">Parameters</span></span>

<span data-ttu-id="de50b-377">chars</span><span class="sxs-lookup"><span data-stu-id="de50b-377">chars</span></span>  
<span data-ttu-id="de50b-378">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="de50b-378">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="de50b-379">明細行</span><span class="sxs-lookup"><span data-stu-id="de50b-379">lines</span></span>  
<span data-ttu-id="de50b-380">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="de50b-380">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-381">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-381">Return Value</span></span>

<span data-ttu-id="de50b-382">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="de50b-382">The container that holds the width and height.</span></span>

### <a name="method-characterset"></a><span data-ttu-id="de50b-383">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="de50b-383">Method characterSet</span></span>

<span data-ttu-id="de50b-384">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-384">Gets or sets the character set of the font.</span></span>

    public int characterSet([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-385">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-385">Parameters</span></span>

<span data-ttu-id="de50b-386">値</span><span class="sxs-lookup"><span data-stu-id="de50b-386">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-387">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-387">Return Value</span></span>

<span data-ttu-id="de50b-388">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-388">An integer value that indicates the character set of the font.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-389">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-389">Remarks</span></span>

<span data-ttu-id="de50b-390">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-390">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="de50b-391">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-391">Value.</span></span> | <span data-ttu-id="de50b-392">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-392">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="de50b-393">0</span><span class="sxs-lookup"><span data-stu-id="de50b-393">0</span></span>      | <span data-ttu-id="de50b-394">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-394">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="de50b-395">1</span><span class="sxs-lookup"><span data-stu-id="de50b-395">1</span></span>      | <span data-ttu-id="de50b-396">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-396">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="de50b-397">2</span><span class="sxs-lookup"><span data-stu-id="de50b-397">2</span></span>      | <span data-ttu-id="de50b-398">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-398">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="de50b-399">77</span><span class="sxs-lookup"><span data-stu-id="de50b-399">77</span></span>     | <span data-ttu-id="de50b-400">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-400">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="de50b-401">128</span><span class="sxs-lookup"><span data-stu-id="de50b-401">128</span></span>    | <span data-ttu-id="de50b-402">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-402">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="de50b-403">129</span><span class="sxs-lookup"><span data-stu-id="de50b-403">129</span></span>    | <span data-ttu-id="de50b-404">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-404">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="de50b-405">134</span><span class="sxs-lookup"><span data-stu-id="de50b-405">134</span></span>    | <span data-ttu-id="de50b-406">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-406">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="de50b-407">136</span><span class="sxs-lookup"><span data-stu-id="de50b-407">136</span></span>    | <span data-ttu-id="de50b-408">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-408">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="de50b-409">161</span><span class="sxs-lookup"><span data-stu-id="de50b-409">161</span></span>    | <span data-ttu-id="de50b-410">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-410">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="de50b-411">162</span><span class="sxs-lookup"><span data-stu-id="de50b-411">162</span></span>    | <span data-ttu-id="de50b-412">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-412">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="de50b-413">163</span><span class="sxs-lookup"><span data-stu-id="de50b-413">163</span></span>    | <span data-ttu-id="de50b-414">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-414">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="de50b-415">186</span><span class="sxs-lookup"><span data-stu-id="de50b-415">186</span></span>    | <span data-ttu-id="de50b-416">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-416">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="de50b-417">204</span><span class="sxs-lookup"><span data-stu-id="de50b-417">204</span></span>    | <span data-ttu-id="de50b-418">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-418">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="de50b-419">238</span><span class="sxs-lookup"><span data-stu-id="de50b-419">238</span></span>    | <span data-ttu-id="de50b-420">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-420">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="de50b-421">255</span><span class="sxs-lookup"><span data-stu-id="de50b-421">255</span></span>    | <span data-ttu-id="de50b-422">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-422">OEM\_CHARSET</span></span>         |

<span data-ttu-id="de50b-423">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-423">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="de50b-424">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-424">Value.</span></span> | <span data-ttu-id="de50b-425">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-425">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="de50b-426">130</span><span class="sxs-lookup"><span data-stu-id="de50b-426">130</span></span>    | <span data-ttu-id="de50b-427">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-427">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="de50b-428">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-428">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="de50b-429">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-429">Value.</span></span> | <span data-ttu-id="de50b-430">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-430">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="de50b-431">177</span><span class="sxs-lookup"><span data-stu-id="de50b-431">177</span></span>    | <span data-ttu-id="de50b-432">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-432">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="de50b-433">178</span><span class="sxs-lookup"><span data-stu-id="de50b-433">178</span></span>    | <span data-ttu-id="de50b-434">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-434">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="de50b-435">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-435">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="de50b-436">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-436">Value.</span></span> | <span data-ttu-id="de50b-437">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-437">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="de50b-438">222</span><span class="sxs-lookup"><span data-stu-id="de50b-438">222</span></span>    | <span data-ttu-id="de50b-439">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-439">THAI\_CHARSET</span></span> |

<span data-ttu-id="de50b-440">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-440">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="de50b-441">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-441">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="de50b-442">詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de50b-442">For more information, see the LOGFONT structure on the MSDN website, http://go.microsoft.com/fwlink/?LinkID=85972.</span></span>

### <a name="method-colorscheme"></a><span data-ttu-id="de50b-443">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="de50b-443">Method colorScheme</span></span>

<span data-ttu-id="de50b-444">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-444">Gets or sets the color scheme of the control.</span></span>

    public int colorScheme([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-445">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-445">Parameters</span></span>

<span data-ttu-id="de50b-446">値</span><span class="sxs-lookup"><span data-stu-id="de50b-446">value</span></span>  
<span data-ttu-id="de50b-447">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-447">The value to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-448">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-448">Return Value</span></span>

<span data-ttu-id="de50b-449">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-449">An integer between zero and two, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-450">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-450">Remarks</span></span>

<span data-ttu-id="de50b-451">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-451">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="de50b-452">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-452">Value.</span></span> | <span data-ttu-id="de50b-453">スタイル。</span><span class="sxs-lookup"><span data-stu-id="de50b-453">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="de50b-454">0</span><span class="sxs-lookup"><span data-stu-id="de50b-454">0</span></span>      | <span data-ttu-id="de50b-455">既定。</span><span class="sxs-lookup"><span data-stu-id="de50b-455">Default.</span></span>               |
| <span data-ttu-id="de50b-456">1</span><span class="sxs-lookup"><span data-stu-id="de50b-456">1</span></span>      | <span data-ttu-id="de50b-457">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="de50b-457">The Windows palette.</span></span>   |
| <span data-ttu-id="de50b-458">2</span><span class="sxs-lookup"><span data-stu-id="de50b-458">2</span></span>      | <span data-ttu-id="de50b-459">真の配色。</span><span class="sxs-lookup"><span data-stu-id="de50b-459">The true-color scheme.</span></span> |

### <a name="method-configurationkey"></a><span data-ttu-id="de50b-460">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="de50b-460">Method configurationKey</span></span>

<span data-ttu-id="de50b-461">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-461">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-462">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-462">Parameters</span></span>

<span data-ttu-id="de50b-463">値</span><span class="sxs-lookup"><span data-stu-id="de50b-463">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-464">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-464">Return Value</span></span>

<span data-ttu-id="de50b-465">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-465">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-466">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-466">Remarks</span></span>

<span data-ttu-id="de50b-467">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-467">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="de50b-468">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="de50b-468">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="de50b-469">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="de50b-469">Method configurationKeyEx</span></span>

<span data-ttu-id="de50b-470">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-470">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="de50b-471">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-471">Return Value</span></span>

<span data-ttu-id="de50b-472">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="de50b-472">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-473">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-473">Remarks</span></span>

<span data-ttu-id="de50b-474">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="de50b-474">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="de50b-475">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-475">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="de50b-476">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-476">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="de50b-477">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="de50b-477">Method countryRegionCodes</span></span>

<span data-ttu-id="de50b-478">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-478">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-479">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-479">Parameters</span></span>

<span data-ttu-id="de50b-480">値</span><span class="sxs-lookup"><span data-stu-id="de50b-480">value</span></span>  
<span data-ttu-id="de50b-481">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-481">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-482">Return Value</span></span>

<span data-ttu-id="de50b-483">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-483">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="de50b-484">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="de50b-484">Method dataRelationPath</span></span>

<span data-ttu-id="de50b-485">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-485">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-486">Parameters</span></span>

<span data-ttu-id="de50b-487">値</span><span class="sxs-lookup"><span data-stu-id="de50b-487">value</span></span>  
<span data-ttu-id="de50b-488">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-488">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-489">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-489">Return Value</span></span>

<span data-ttu-id="de50b-490">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="de50b-490">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-491">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-491">Remarks</span></span>

<span data-ttu-id="de50b-492">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="de50b-492">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="de50b-493">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="de50b-493">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="de50b-494">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="de50b-494">Method displayTarget</span></span>

<span data-ttu-id="de50b-495">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-495">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, Finance and Operations, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-496">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-496">Parameters</span></span>

<span data-ttu-id="de50b-497">値</span><span class="sxs-lookup"><span data-stu-id="de50b-497">value</span></span>  
<span data-ttu-id="de50b-498">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-498">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-499">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-499">Return Value</span></span>

<span data-ttu-id="de50b-500">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="de50b-500">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="de50b-501">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="de50b-501">Method dragDrop</span></span>

<span data-ttu-id="de50b-502">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-502">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-503">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-503">Parameters</span></span>

<span data-ttu-id="de50b-504">値</span><span class="sxs-lookup"><span data-stu-id="de50b-504">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-505">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-505">Return Value</span></span>

<span data-ttu-id="de50b-506">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="de50b-506">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="de50b-507">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="de50b-507">Method dragOver</span></span>

<span data-ttu-id="de50b-508">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-508">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-509">Parameters</span></span>

<span data-ttu-id="de50b-510">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-510">dragSource</span></span>  
<span data-ttu-id="de50b-511">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-511">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-512">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-512">dragMode</span></span>  
<span data-ttu-id="de50b-513">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-513">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-514">x</span><span class="sxs-lookup"><span data-stu-id="de50b-514">x</span></span>  
<span data-ttu-id="de50b-515">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-515">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-516">y</span><span class="sxs-lookup"><span data-stu-id="de50b-516">y</span></span>  
<span data-ttu-id="de50b-517">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-517">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-518">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-518">Return Value</span></span>

<span data-ttu-id="de50b-519">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="de50b-519">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="de50b-520">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="de50b-520">Method dragOverEx</span></span>

<span data-ttu-id="de50b-521">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-521">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-522">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-522">Parameters</span></span>

<span data-ttu-id="de50b-523">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-523">dragSource</span></span>  
<span data-ttu-id="de50b-524">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-524">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-525">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-525">dragMode</span></span>  
<span data-ttu-id="de50b-526">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-526">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-527">x</span><span class="sxs-lookup"><span data-stu-id="de50b-527">x</span></span>  
<span data-ttu-id="de50b-528">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-528">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-529">y</span><span class="sxs-lookup"><span data-stu-id="de50b-529">y</span></span>  
<span data-ttu-id="de50b-530">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-530">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-531">Return Value</span></span>

<span data-ttu-id="de50b-532">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="de50b-532">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="de50b-533">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="de50b-533">Method dragText</span></span>

<span data-ttu-id="de50b-534">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-534">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="de50b-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-535">Return Value</span></span>

<span data-ttu-id="de50b-536">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-536">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="de50b-537">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="de50b-537">Method enabled</span></span>

<span data-ttu-id="de50b-538">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-538">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-539">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-539">Parameters</span></span>

<span data-ttu-id="de50b-540">値</span><span class="sxs-lookup"><span data-stu-id="de50b-540">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-541">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-541">Return Value</span></span>

<span data-ttu-id="de50b-542">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-542">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-543">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-543">Remarks</span></span>

<span data-ttu-id="de50b-544">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-544">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="de50b-545">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-545">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="de50b-546">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-546">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-font"></a><span data-ttu-id="de50b-547">メソッド font</span><span class="sxs-lookup"><span data-stu-id="de50b-547">Method font</span></span>

<span data-ttu-id="de50b-548">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-548">Gets or sets the name of the font for the control to use.</span></span>

    public str font([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-549">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-549">Parameters</span></span>

<span data-ttu-id="de50b-550">値</span><span class="sxs-lookup"><span data-stu-id="de50b-550">value</span></span>  
<span data-ttu-id="de50b-551">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-551">The value to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-552">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-552">Return Value</span></span>

<span data-ttu-id="de50b-553">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-553">The name of the font to use, such as Tahoma or Verdana.</span></span>

### <a name="method-fontsize"></a><span data-ttu-id="de50b-554">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="de50b-554">Method fontSize</span></span>

<span data-ttu-id="de50b-555">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-555">Gets or sets the size of the font for the control to use.</span></span>

    public int fontSize([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-556">Parameters</span></span>

<span data-ttu-id="de50b-557">値</span><span class="sxs-lookup"><span data-stu-id="de50b-557">value</span></span>  
<span data-ttu-id="de50b-558">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-558">The value to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-559">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-559">Return Value</span></span>

<span data-ttu-id="de50b-560">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-560">The height of the font in points.</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="de50b-561">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="de50b-561">Method hasChanged</span></span>

<span data-ttu-id="de50b-562">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-562">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="de50b-563">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-563">Parameters</span></span>

<span data-ttu-id="de50b-564">val</span><span class="sxs-lookup"><span data-stu-id="de50b-564">val</span></span>  
<span data-ttu-id="de50b-565">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-565">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-566">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-566">Return Value</span></span>

<span data-ttu-id="de50b-567">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-567">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="de50b-568">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="de50b-568">Method hasUserSetting</span></span>

<span data-ttu-id="de50b-569">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-569">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="de50b-570">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-570">Return Value</span></span>

<span data-ttu-id="de50b-571">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-571">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="de50b-572">メソッド height</span><span class="sxs-lookup"><span data-stu-id="de50b-572">Method height</span></span>

<span data-ttu-id="de50b-573">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-573">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-574">Parameters</span></span>

<span data-ttu-id="de50b-575">値</span><span class="sxs-lookup"><span data-stu-id="de50b-575">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-576">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-576">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-577">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-577">Return Value</span></span>

<span data-ttu-id="de50b-578">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-578">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-579">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-579">Remarks</span></span>

<span data-ttu-id="de50b-580">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-580">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="de50b-581">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-581">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="de50b-582">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-582">Mode.</span></span>            | <span data-ttu-id="de50b-583">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-583">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-584">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-584">-1 Exact.</span></span>        | <span data-ttu-id="de50b-585">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-585">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-586">0 自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-586">0 Auto.</span></span>          | <span data-ttu-id="de50b-587">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-587">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-588">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-588">1 Column height.</span></span> | <span data-ttu-id="de50b-589">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-589">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="de50b-590">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-590">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="de50b-591">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="de50b-591">Method heightMode</span></span>

<span data-ttu-id="de50b-592">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-592">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-593">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-593">Parameters</span></span>

<span data-ttu-id="de50b-594">値</span><span class="sxs-lookup"><span data-stu-id="de50b-594">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-595">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-595">Return Value</span></span>

<span data-ttu-id="de50b-596">計算モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-596">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-597">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-597">Remarks</span></span>

<span data-ttu-id="de50b-598">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-598">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="de50b-599">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-599">Mode.</span></span>          | <span data-ttu-id="de50b-600">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-600">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-601">正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-601">Exact.</span></span>         | <span data-ttu-id="de50b-602">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-602">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-603">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-603">Auto.</span></span>          | <span data-ttu-id="de50b-604">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-604">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-605">列の高さ</span><span class="sxs-lookup"><span data-stu-id="de50b-605">Column height.</span></span> | <span data-ttu-id="de50b-606">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-606">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="de50b-607">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="de50b-607">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="de50b-608">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="de50b-608">Method heightValue</span></span>

<span data-ttu-id="de50b-609">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-609">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-610">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-610">Parameters</span></span>

<span data-ttu-id="de50b-611">値</span><span class="sxs-lookup"><span data-stu-id="de50b-611">value</span></span>  
<span data-ttu-id="de50b-612">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-612">The value to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-613">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-613">Return Value</span></span>

<span data-ttu-id="de50b-614">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-614">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-615">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-615">Remarks</span></span>

<span data-ttu-id="de50b-616">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="de50b-616">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="de50b-617">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="de50b-617">Method helpField</span></span>

<span data-ttu-id="de50b-618">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-618">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="de50b-619">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-619">Return Value</span></span>

<span data-ttu-id="de50b-620">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-620">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-621">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-621">Remarks</span></span>

<span data-ttu-id="de50b-622">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-622">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="de50b-623">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-623">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="de50b-624">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="de50b-624">Method helpText</span></span>

<span data-ttu-id="de50b-625">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-625">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-626">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-626">Parameters</span></span>

<span data-ttu-id="de50b-627">値</span><span class="sxs-lookup"><span data-stu-id="de50b-627">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-628">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-628">Return Value</span></span>

<span data-ttu-id="de50b-629">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-629">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-630">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-630">Remarks</span></span>

<span data-ttu-id="de50b-631">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-631">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="de50b-632">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="de50b-632">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="de50b-633">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="de50b-633">Method hierarchyParent</span></span>

<span data-ttu-id="de50b-634">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-634">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-635">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-635">Parameters</span></span>

<span data-ttu-id="de50b-636">値</span><span class="sxs-lookup"><span data-stu-id="de50b-636">value</span></span>  
<span data-ttu-id="de50b-637">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-637">The value to assign the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-638">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-638">Return Value</span></span>

<span data-ttu-id="de50b-639">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="de50b-639">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="de50b-640">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="de50b-640">Method hWnd</span></span>

<span data-ttu-id="de50b-641">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-641">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="de50b-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-642">Return Value</span></span>

<span data-ttu-id="de50b-643">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="de50b-643">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-644">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-644">Remarks</span></span>

<span data-ttu-id="de50b-645">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-645">The handle can be used with the Windows API.</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="de50b-646">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="de50b-646">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="de50b-647">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-647">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="de50b-648">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="de50b-648">Method isDisplayed</span></span>

<span data-ttu-id="de50b-649">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-649">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="de50b-650">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-650">Return Value</span></span>

<span data-ttu-id="de50b-651">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-651">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-652">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-652">Remarks</span></span>

<span data-ttu-id="de50b-653">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="de50b-653">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="de50b-654">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="de50b-654">Method isRestricted</span></span>

<span data-ttu-id="de50b-655">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-655">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="de50b-656">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-656">Return Value</span></span>

<span data-ttu-id="de50b-657">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-657">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="de50b-658">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="de50b-658">Method isUserSetupEnabled</span></span>

<span data-ttu-id="de50b-659">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-659">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="de50b-660">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-660">Parameters</span></span>

<span data-ttu-id="de50b-661">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="de50b-661">neededSetupRights</span></span>  
<span data-ttu-id="de50b-662">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="de50b-662">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-663">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-663">Return Value</span></span>

<span data-ttu-id="de50b-664">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-664">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-665">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-665">Remarks</span></span>

<span data-ttu-id="de50b-666">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="de50b-666">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-667">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="de50b-667">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="de50b-668">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="de50b-668">No changes can be made to the control.</span></span> <span data-ttu-id="de50b-669">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-669">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="de50b-670">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="de50b-670">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="de50b-671">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-671">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="de50b-672">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="de50b-672">The user cannot move the control.</span></span>   |
| <span data-ttu-id="de50b-673">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="de50b-673">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="de50b-674">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-674">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="de50b-675">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-675">The user can also move the control.</span></span> |

<span data-ttu-id="de50b-676">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-676">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="method-italic"></a><span data-ttu-id="de50b-677">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="de50b-677">Method italic</span></span>

    public boolean italic([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-678">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-678">Parameters</span></span>

<span data-ttu-id="de50b-679">値</span><span class="sxs-lookup"><span data-stu-id="de50b-679">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-680">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-680">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="de50b-681">メソッド left</span><span class="sxs-lookup"><span data-stu-id="de50b-681">Method left</span></span>

<span data-ttu-id="de50b-682">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-682">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-683">Parameters</span></span>

<span data-ttu-id="de50b-684">値</span><span class="sxs-lookup"><span data-stu-id="de50b-684">value</span></span>  
<span data-ttu-id="de50b-685">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-685">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-686">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-686">mode</span></span>  
<span data-ttu-id="de50b-687">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-687">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-688">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-688">Return Value</span></span>

<span data-ttu-id="de50b-689">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-689">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="de50b-690">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="de50b-690">Method leftMode</span></span>

<span data-ttu-id="de50b-691">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-691">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-692">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-692">Parameters</span></span>

<span data-ttu-id="de50b-693">値</span><span class="sxs-lookup"><span data-stu-id="de50b-693">value</span></span>  
<span data-ttu-id="de50b-694">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-694">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-695">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-695">Return Value</span></span>

<span data-ttu-id="de50b-696">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-696">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="de50b-697">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="de50b-697">Method leftValue</span></span>

<span data-ttu-id="de50b-698">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-698">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-699">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-699">Parameters</span></span>

<span data-ttu-id="de50b-700">値</span><span class="sxs-lookup"><span data-stu-id="de50b-700">value</span></span>  
<span data-ttu-id="de50b-701">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-701">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-702">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-702">Return Value</span></span>

<span data-ttu-id="de50b-703">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-703">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="de50b-704">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="de50b-704">Method markAsUserAdd</span></span>

<span data-ttu-id="de50b-705">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="de50b-705">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-706">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-706">Parameters</span></span>

<span data-ttu-id="de50b-707">値</span><span class="sxs-lookup"><span data-stu-id="de50b-707">value</span></span>  
<span data-ttu-id="de50b-708">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-708">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-709">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-709">Return Value</span></span>

<span data-ttu-id="de50b-710">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-710">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="de50b-711">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="de50b-711">Method mouseDblClick</span></span>

<span data-ttu-id="de50b-712">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-712">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-713">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-713">Parameters</span></span>

<span data-ttu-id="de50b-714">x</span><span class="sxs-lookup"><span data-stu-id="de50b-714">x</span></span>  
<span data-ttu-id="de50b-715">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-715">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-716">y</span><span class="sxs-lookup"><span data-stu-id="de50b-716">y</span></span>  
<span data-ttu-id="de50b-717">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-717">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-718">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-718">button</span></span>  
<span data-ttu-id="de50b-719">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-719">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-720">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-720">Ctrl</span></span>  
<span data-ttu-id="de50b-721">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-721">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-722">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-722">Shift</span></span>  
<span data-ttu-id="de50b-723">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-723">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-724">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-724">Return Value</span></span>

<span data-ttu-id="de50b-725">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-725">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-726">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-726">Remarks</span></span>

<span data-ttu-id="de50b-727">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-727">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="de50b-728">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="de50b-728">Method mouseDown</span></span>

<span data-ttu-id="de50b-729">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-729">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-730">Parameters</span></span>

<span data-ttu-id="de50b-731">x</span><span class="sxs-lookup"><span data-stu-id="de50b-731">x</span></span>  
<span data-ttu-id="de50b-732">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-732">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-733">y</span><span class="sxs-lookup"><span data-stu-id="de50b-733">y</span></span>  
<span data-ttu-id="de50b-734">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-734">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-735">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-735">button</span></span>  
<span data-ttu-id="de50b-736">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-736">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-737">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-737">Ctrl</span></span>  
<span data-ttu-id="de50b-738">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-738">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-739">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-739">Shift</span></span>  
<span data-ttu-id="de50b-740">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-740">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-741">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-741">Return Value</span></span>

<span data-ttu-id="de50b-742">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-742">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-743">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-743">Remarks</span></span>

<span data-ttu-id="de50b-744">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-744">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="de50b-745">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-745">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="de50b-746">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="de50b-746">Method mouseMove</span></span>

<span data-ttu-id="de50b-747">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-747">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-748">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-748">Parameters</span></span>

<span data-ttu-id="de50b-749">x</span><span class="sxs-lookup"><span data-stu-id="de50b-749">x</span></span>  
<span data-ttu-id="de50b-750">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-750">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-751">y</span><span class="sxs-lookup"><span data-stu-id="de50b-751">y</span></span>  
<span data-ttu-id="de50b-752">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-752">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-753">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-753">button</span></span>  
<span data-ttu-id="de50b-754">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-754">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-755">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-755">Ctrl</span></span>  
<span data-ttu-id="de50b-756">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-756">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-757">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-757">Shift</span></span>  
<span data-ttu-id="de50b-758">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-758">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-759">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-759">Return Value</span></span>

<span data-ttu-id="de50b-760">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-760">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-761">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-761">Remarks</span></span>

<span data-ttu-id="de50b-762">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-762">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="de50b-763">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="de50b-763">Method mouseUp</span></span>

<span data-ttu-id="de50b-764">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-764">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-765">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-765">Parameters</span></span>

<span data-ttu-id="de50b-766">x</span><span class="sxs-lookup"><span data-stu-id="de50b-766">x</span></span>  
<span data-ttu-id="de50b-767">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-767">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-768">y</span><span class="sxs-lookup"><span data-stu-id="de50b-768">y</span></span>  
<span data-ttu-id="de50b-769">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-769">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-770">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-770">button</span></span>  
<span data-ttu-id="de50b-771">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-771">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-772">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-772">Ctrl</span></span>  
<span data-ttu-id="de50b-773">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-773">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-774">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-774">Shift</span></span>  
<span data-ttu-id="de50b-775">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-775">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-776">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-776">Return Value</span></span>

<span data-ttu-id="de50b-777">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-777">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-778">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-778">Remarks</span></span>

<span data-ttu-id="de50b-779">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-779">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="de50b-780">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-780">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-name"></a><span data-ttu-id="de50b-781">メソッド名</span><span class="sxs-lookup"><span data-stu-id="de50b-781">Method name</span></span>

<span data-ttu-id="de50b-782">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-782">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-783">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-783">Parameters</span></span>

<span data-ttu-id="de50b-784">値</span><span class="sxs-lookup"><span data-stu-id="de50b-784">value</span></span>  
<span data-ttu-id="de50b-785">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-785">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-786">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-786">Return Value</span></span>

<span data-ttu-id="de50b-787">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-787">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-788">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-788">Remarks</span></span>

<span data-ttu-id="de50b-789">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-789">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="de50b-790">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-790">It must begin with a letter.</span></span>
-   <span data-ttu-id="de50b-791">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-791">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="de50b-792">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-792">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="de50b-793">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-793">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="de50b-794">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-794">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="de50b-795">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="de50b-795">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-796">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-796">Parameters</span></span>

<span data-ttu-id="de50b-797">値</span><span class="sxs-lookup"><span data-stu-id="de50b-797">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-798">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-798">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="de50b-799">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="de50b-799">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="de50b-800">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-800">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="de50b-801">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="de50b-801">Method parentControl</span></span>

<span data-ttu-id="de50b-802">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-802">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="de50b-803">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-803">Return Value</span></span>

<span data-ttu-id="de50b-804">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="de50b-804">The parent control for the control.</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="de50b-805">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="de50b-805">Method securityKey</span></span>

<span data-ttu-id="de50b-806">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-806">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-807">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-807">Parameters</span></span>

<span data-ttu-id="de50b-808">値</span><span class="sxs-lookup"><span data-stu-id="de50b-808">value</span></span>  
<span data-ttu-id="de50b-809">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-809">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-810">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-810">Return Value</span></span>

<span data-ttu-id="de50b-811">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="de50b-811">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="de50b-812">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="de50b-812">Method showContextMenu</span></span>

<span data-ttu-id="de50b-813">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-813">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="de50b-814">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-814">Parameters</span></span>

<span data-ttu-id="de50b-815">menuHandle</span><span class="sxs-lookup"><span data-stu-id="de50b-815">menuHandle</span></span>  
<span data-ttu-id="de50b-816">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-816">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-817">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-817">Return Value</span></span>

<span data-ttu-id="de50b-818">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-818">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-skip"></a><span data-ttu-id="de50b-819">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="de50b-819">Method skip</span></span>

<span data-ttu-id="de50b-820">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-820">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-821">Parameters</span></span>

<span data-ttu-id="de50b-822">値</span><span class="sxs-lookup"><span data-stu-id="de50b-822">value</span></span>  
<span data-ttu-id="de50b-823">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-823">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-824">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-824">Return Value</span></span>

<span data-ttu-id="de50b-825">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-825">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-826">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-826">Remarks</span></span>

<span data-ttu-id="de50b-827">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-827">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="de50b-828">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="de50b-828">Method toolTip</span></span>

<span data-ttu-id="de50b-829">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-829">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="de50b-830">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-830">Return Value</span></span>

<span data-ttu-id="de50b-831">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-831">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-832">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-832">Remarks</span></span>

<span data-ttu-id="de50b-833">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-833">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="de50b-834">メソッド top</span><span class="sxs-lookup"><span data-stu-id="de50b-834">Method top</span></span>

<span data-ttu-id="de50b-835">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-835">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-836">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-836">Parameters</span></span>

<span data-ttu-id="de50b-837">値</span><span class="sxs-lookup"><span data-stu-id="de50b-837">value</span></span>  
<span data-ttu-id="de50b-838">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-838">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-839">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-839">mode</span></span>  
<span data-ttu-id="de50b-840">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-840">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-841">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-841">Return Value</span></span>

<span data-ttu-id="de50b-842">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-842">The vertical position of the control in the form.</span></span>

### <a name="method-topmode"></a><span data-ttu-id="de50b-843">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="de50b-843">Method topMode</span></span>

<span data-ttu-id="de50b-844">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-844">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-845">Parameters</span></span>

<span data-ttu-id="de50b-846">値</span><span class="sxs-lookup"><span data-stu-id="de50b-846">value</span></span>  
<span data-ttu-id="de50b-847">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-847">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-848">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-848">Return Value</span></span>

<span data-ttu-id="de50b-849">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-849">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="de50b-850">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="de50b-850">Method topValue</span></span>

<span data-ttu-id="de50b-851">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-851">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-852">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-852">Parameters</span></span>

<span data-ttu-id="de50b-853">値</span><span class="sxs-lookup"><span data-stu-id="de50b-853">value</span></span>  
<span data-ttu-id="de50b-854">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-854">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-855">Return Value</span></span>

<span data-ttu-id="de50b-856">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-856">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="de50b-857">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="de50b-857">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-858">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-858">Parameters</span></span>

<span data-ttu-id="de50b-859">値</span><span class="sxs-lookup"><span data-stu-id="de50b-859">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-860">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-860">Return Value</span></span>

### <a name="method-underline"></a><span data-ttu-id="de50b-861">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="de50b-861">Method underline</span></span>

    public boolean underline([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-862">Parameters</span></span>

<span data-ttu-id="de50b-863">値</span><span class="sxs-lookup"><span data-stu-id="de50b-863">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-864">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-864">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="de50b-865">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="de50b-865">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="de50b-866">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-866">Parameters</span></span>

<span data-ttu-id="de50b-867">データ</span><span class="sxs-lookup"><span data-stu-id="de50b-867">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-868">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-868">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="de50b-869">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="de50b-869">Method userData</span></span>

<span data-ttu-id="de50b-870">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-870">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-871">Parameters</span></span>

<span data-ttu-id="de50b-872">値</span><span class="sxs-lookup"><span data-stu-id="de50b-872">value</span></span>  
<span data-ttu-id="de50b-873">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-873">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-874">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-874">Return Value</span></span>

<span data-ttu-id="de50b-875">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="de50b-875">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="de50b-876">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="de50b-876">Method userDataItem</span></span>

<span data-ttu-id="de50b-877">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-877">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-878">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-878">Parameters</span></span>

<span data-ttu-id="de50b-879">値</span><span class="sxs-lookup"><span data-stu-id="de50b-879">value</span></span>  
<span data-ttu-id="de50b-880">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-880">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-881">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-881">Return Value</span></span>

<span data-ttu-id="de50b-882">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="de50b-882">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="de50b-883">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="de50b-883">Method userDataItems</span></span>

<span data-ttu-id="de50b-884">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-884">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-885">Parameters</span></span>

<span data-ttu-id="de50b-886">値</span><span class="sxs-lookup"><span data-stu-id="de50b-886">value</span></span>  
<span data-ttu-id="de50b-887">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-887">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-888">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-888">Return Value</span></span>

<span data-ttu-id="de50b-889">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="de50b-889">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="de50b-890">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="de50b-890">Method userDisable</span></span>

<span data-ttu-id="de50b-891">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-891">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-892">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-892">Parameters</span></span>

<span data-ttu-id="de50b-893">値</span><span class="sxs-lookup"><span data-stu-id="de50b-893">value</span></span>  
<span data-ttu-id="de50b-894">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-894">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-895">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-895">Return Value</span></span>

<span data-ttu-id="de50b-896">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-896">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="de50b-897">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="de50b-897">Method userHeight</span></span>

<span data-ttu-id="de50b-898">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-898">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-899">Parameters</span></span>

<span data-ttu-id="de50b-900">値</span><span class="sxs-lookup"><span data-stu-id="de50b-900">value</span></span>  
<span data-ttu-id="de50b-901">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-901">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-902">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-902">Return Value</span></span>

<span data-ttu-id="de50b-903">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-903">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="de50b-904">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="de50b-904">Method userHide</span></span>

<span data-ttu-id="de50b-905">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-905">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-906">Parameters</span></span>

<span data-ttu-id="de50b-907">値</span><span class="sxs-lookup"><span data-stu-id="de50b-907">value</span></span>  
<span data-ttu-id="de50b-908">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-908">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-909">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-909">Return Value</span></span>

<span data-ttu-id="de50b-910">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-910">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-911">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-911">Remarks</span></span>

<span data-ttu-id="de50b-912">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-912">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="de50b-913">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="de50b-913">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="de50b-914">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-914">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="de50b-915">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="de50b-915">Method userOrgContainer</span></span>

<span data-ttu-id="de50b-916">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-916">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-917">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-917">Parameters</span></span>

<span data-ttu-id="de50b-918">値</span><span class="sxs-lookup"><span data-stu-id="de50b-918">value</span></span>  
<span data-ttu-id="de50b-919">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-919">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-920">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-920">Return Value</span></span>

<span data-ttu-id="de50b-921">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="de50b-921">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="de50b-922">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="de50b-922">Method userOrgSibling</span></span>

<span data-ttu-id="de50b-923">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-923">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-924">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-924">Parameters</span></span>

<span data-ttu-id="de50b-925">値</span><span class="sxs-lookup"><span data-stu-id="de50b-925">value</span></span>  
<span data-ttu-id="de50b-926">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-926">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-927">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-927">Return Value</span></span>

<span data-ttu-id="de50b-928">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="de50b-928">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="de50b-929">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="de50b-929">Method userPromptText</span></span>

<span data-ttu-id="de50b-930">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-930">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-931">Parameters</span></span>

<span data-ttu-id="de50b-932">値</span><span class="sxs-lookup"><span data-stu-id="de50b-932">value</span></span>  
<span data-ttu-id="de50b-933">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-933">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-934">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-934">Return Value</span></span>

<span data-ttu-id="de50b-935">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-935">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="de50b-936">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="de50b-936">Method userSecurityLevel</span></span>

<span data-ttu-id="de50b-937">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-937">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-938">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-938">Parameters</span></span>

<span data-ttu-id="de50b-939">値</span><span class="sxs-lookup"><span data-stu-id="de50b-939">value</span></span>  
<span data-ttu-id="de50b-940">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-940">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-941">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-941">Return Value</span></span>

<span data-ttu-id="de50b-942">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="de50b-942">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="de50b-943">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="de50b-943">Method userSkip</span></span>

<span data-ttu-id="de50b-944">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-944">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-945">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-945">Parameters</span></span>

<span data-ttu-id="de50b-946">値</span><span class="sxs-lookup"><span data-stu-id="de50b-946">value</span></span>  
<span data-ttu-id="de50b-947">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-947">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="de50b-948">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-948">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-949">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-949">Return Value</span></span>

<span data-ttu-id="de50b-950">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-950">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="de50b-951">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="de50b-951">Method userWidth</span></span>

<span data-ttu-id="de50b-952">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-952">Sets or returns the width of the control in pixels.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-953">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-953">Parameters</span></span>

<span data-ttu-id="de50b-954">値</span><span class="sxs-lookup"><span data-stu-id="de50b-954">value</span></span>  
<span data-ttu-id="de50b-955">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-955">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-956">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-956">Return Value</span></span>

<span data-ttu-id="de50b-957">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="de50b-957">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-958">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-958">Remarks</span></span>

<span data-ttu-id="de50b-959">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-959">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="de50b-960">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="de50b-960">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="de50b-961">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="de50b-961">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="de50b-962">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="de50b-962">Method verticalSpacing</span></span>

<span data-ttu-id="de50b-963">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-963">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-964">Parameters</span></span>

<span data-ttu-id="de50b-965">値</span><span class="sxs-lookup"><span data-stu-id="de50b-965">value</span></span>  
<span data-ttu-id="de50b-966">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-966">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-967">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-967">mode</span></span>  
<span data-ttu-id="de50b-968">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-968">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-969">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-969">Return Value</span></span>

<span data-ttu-id="de50b-970">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="de50b-970">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="de50b-971">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="de50b-971">Method verticalSpacingMode</span></span>

<span data-ttu-id="de50b-972">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-972">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-973">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-973">Parameters</span></span>

<span data-ttu-id="de50b-974">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-974">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-975">Return Value</span></span>

<span data-ttu-id="de50b-976">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-976">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="de50b-977">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="de50b-977">Method verticalSpacingValue</span></span>

<span data-ttu-id="de50b-978">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-978">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-979">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-979">Parameters</span></span>

<span data-ttu-id="de50b-980">値</span><span class="sxs-lookup"><span data-stu-id="de50b-980">value</span></span>  
<span data-ttu-id="de50b-981">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-981">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-982">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-982">Return Value</span></span>

<span data-ttu-id="de50b-983">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="de50b-983">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="de50b-984">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="de50b-984">Method visible</span></span>

<span data-ttu-id="de50b-985">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-985">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-986">Parameters</span></span>

<span data-ttu-id="de50b-987">値</span><span class="sxs-lookup"><span data-stu-id="de50b-987">value</span></span>  
<span data-ttu-id="de50b-988">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-988">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-989">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-989">Return Value</span></span>

<span data-ttu-id="de50b-990">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-990">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="de50b-991">メソッド width</span><span class="sxs-lookup"><span data-stu-id="de50b-991">Method width</span></span>

<span data-ttu-id="de50b-992">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-992">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-993">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-993">Parameters</span></span>

<span data-ttu-id="de50b-994">値</span><span class="sxs-lookup"><span data-stu-id="de50b-994">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-995">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-995">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-996">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-996">Return Value</span></span>

<span data-ttu-id="de50b-997">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-997">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-998">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-998">Remarks</span></span>

<span data-ttu-id="de50b-999">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-999">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="de50b-1000">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-1000">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="de50b-1001">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-1001">Mode.</span></span>           | <span data-ttu-id="de50b-1002">幅計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-1002">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-1003">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-1003">-1 Exact.</span></span>       | <span data-ttu-id="de50b-1004">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1004">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-1005">0 自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-1005">0 Auto.</span></span>         | <span data-ttu-id="de50b-1006">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1006">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-1007">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-1007">1 Column width.</span></span> | <span data-ttu-id="de50b-1008">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1008">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="de50b-1009">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1009">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="de50b-1010">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1010">Method widthMode</span></span>

<span data-ttu-id="de50b-1011">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1011">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1012">Parameters</span></span>

<span data-ttu-id="de50b-1013">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1013">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1014">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1014">Return Value</span></span>

<span data-ttu-id="de50b-1015">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1015">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1016">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1016">Remarks</span></span>

<span data-ttu-id="de50b-1017">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-1017">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="de50b-1018">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-1018">Mode.</span></span>         | <span data-ttu-id="de50b-1019">幅計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-1019">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-1020">正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-1020">Exact.</span></span>        | <span data-ttu-id="de50b-1021">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1021">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-1022">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-1022">Auto.</span></span>         | <span data-ttu-id="de50b-1023">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1023">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-1024">列の幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-1024">Column width.</span></span> | <span data-ttu-id="de50b-1025">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1025">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="de50b-1026">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1026">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="de50b-1027">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1027">Method widthValue</span></span>

<span data-ttu-id="de50b-1028">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1028">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1029">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1029">Parameters</span></span>

<span data-ttu-id="de50b-1030">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1030">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1031">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1031">Return Value</span></span>

<span data-ttu-id="de50b-1032">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-1032">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1033">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1033">Remarks</span></span>

<span data-ttu-id="de50b-1034">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1034">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-drop"></a><span data-ttu-id="de50b-1035">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="de50b-1035">Method drop</span></span>

<span data-ttu-id="de50b-1036">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1036">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-1037">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1037">Parameters</span></span>

<span data-ttu-id="de50b-1038">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-1038">dragSource</span></span>  
<span data-ttu-id="de50b-1039">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1039">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1040">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1040">dragMode</span></span>  
<span data-ttu-id="de50b-1041">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1041">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1042">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1042">x</span></span>  
<span data-ttu-id="de50b-1043">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1043">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1044">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1044">y</span></span>  
<span data-ttu-id="de50b-1045">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1045">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-copy"></a><span data-ttu-id="de50b-1046">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="de50b-1046">Method copy</span></span>

<span data-ttu-id="de50b-1047">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="de50b-1047">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-cut"></a><span data-ttu-id="de50b-1048">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="de50b-1048">Method cut</span></span>

<span data-ttu-id="de50b-1049">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="de50b-1049">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-setfocus"></a><span data-ttu-id="de50b-1050">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-1050">Method setFocus</span></span>

<span data-ttu-id="de50b-1051">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1051">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-mouseleave"></a><span data-ttu-id="de50b-1052">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="de50b-1052">Method mouseLeave</span></span>

<span data-ttu-id="de50b-1053">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1053">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-enddrag"></a><span data-ttu-id="de50b-1054">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="de50b-1054">Method endDrag</span></span>

<span data-ttu-id="de50b-1055">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1055">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="de50b-1056">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1056">Remarks</span></span>

<span data-ttu-id="de50b-1057">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1057">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="de50b-1058">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1058">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-context"></a><span data-ttu-id="de50b-1059">メソッド context</span><span class="sxs-lookup"><span data-stu-id="de50b-1059">Method context</span></span>

<span data-ttu-id="de50b-1060">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1060">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-gotfocus"></a><span data-ttu-id="de50b-1061">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-1061">Method gotFocus</span></span>

<span data-ttu-id="de50b-1062">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1062">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-prefcolumnsize"></a><span data-ttu-id="de50b-1063">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="de50b-1063">Method prefColumnSize</span></span>

<span data-ttu-id="de50b-1064">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1064">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="de50b-1065">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1065">Parameters</span></span>

<span data-ttu-id="de50b-1066">width</span><span class="sxs-lookup"><span data-stu-id="de50b-1066">width</span></span>  
<span data-ttu-id="de50b-1067">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="de50b-1067">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="de50b-1068">height</span><span class="sxs-lookup"><span data-stu-id="de50b-1068">height</span></span>  
<span data-ttu-id="de50b-1069">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="de50b-1069">The preferred height of the control.</span></span>

### <a name="method-lostfocus"></a><span data-ttu-id="de50b-1070">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-1070">Method lostFocus</span></span>

<span data-ttu-id="de50b-1071">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1071">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-displaycontrol"></a><span data-ttu-id="de50b-1072">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="de50b-1072">Method displayControl</span></span>

<span data-ttu-id="de50b-1073">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1073">Displays the control.</span></span>

    public void displayControl()

### <a name="method-registeroverridemethod"></a><span data-ttu-id="de50b-1074">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="de50b-1074">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="de50b-1075">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1075">Parameters</span></span>

<span data-ttu-id="de50b-1076">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="de50b-1076">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="de50b-1077">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="de50b-1077">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="de50b-1078">overrideObject</span><span class="sxs-lookup"><span data-stu-id="de50b-1078">overrideObject</span></span>  

### <a name="method-paste"></a><span data-ttu-id="de50b-1079">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="de50b-1079">Method paste</span></span>

<span data-ttu-id="de50b-1080">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1080">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-resetusersetting"></a><span data-ttu-id="de50b-1081">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="de50b-1081">Method resetUserSetting</span></span>

<span data-ttu-id="de50b-1082">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="de50b-1082">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-dropex"></a><span data-ttu-id="de50b-1083">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="de50b-1083">Method dropEx</span></span>

<span data-ttu-id="de50b-1084">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1084">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-1085">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1085">Parameters</span></span>

<span data-ttu-id="de50b-1086">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-1086">dragSource</span></span>  
<span data-ttu-id="de50b-1087">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1087">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1088">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1088">dragMode</span></span>  
<span data-ttu-id="de50b-1089">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1089">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1090">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1090">x</span></span>  
<span data-ttu-id="de50b-1091">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1091">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1092">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1092">y</span></span>  
<span data-ttu-id="de50b-1093">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1093">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-mouseenter"></a><span data-ttu-id="de50b-1094">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="de50b-1094">Method mouseEnter</span></span>

<span data-ttu-id="de50b-1095">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1095">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-1096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1096">Parameters</span></span>

<span data-ttu-id="de50b-1097">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1097">x</span></span>  
<span data-ttu-id="de50b-1098">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1098">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1099">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1099">y</span></span>  
<span data-ttu-id="de50b-1100">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1100">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1101">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-1101">button</span></span>  
<span data-ttu-id="de50b-1102">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1102">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1103">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-1103">Ctrl</span></span>  
<span data-ttu-id="de50b-1104">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1104">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1105">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-1105">Shift</span></span>  
<span data-ttu-id="de50b-1106">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1106">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-inputsearch"></a><span data-ttu-id="de50b-1107">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="de50b-1107">Method inputSearch</span></span>

<span data-ttu-id="de50b-1108">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1108">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="de50b-1109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1109">Parameters</span></span>

<span data-ttu-id="de50b-1110">searchStr</span><span class="sxs-lookup"><span data-stu-id="de50b-1110">searchStr</span></span>  
<span data-ttu-id="de50b-1111">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1111">The string value to use to filter data; optional.</span></span>

### <a name="method-dragleave"></a><span data-ttu-id="de50b-1112">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="de50b-1112">Method dragLeave</span></span>

<span data-ttu-id="de50b-1113">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1113">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

## <a name="class-formfilterpanecontrol"></a><span data-ttu-id="de50b-1114">クラス FormFilterPaneControl</span><span class="sxs-lookup"><span data-stu-id="de50b-1114">Class FormFilterPaneControl</span></span>
    class FormFilterPaneControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="de50b-1115">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1115">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="de50b-1116">例</span><span class="sxs-lookup"><span data-stu-id="de50b-1116">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="de50b-1117">メソッド</span><span class="sxs-lookup"><span data-stu-id="de50b-1117">Methods</span></span>

| <span data-ttu-id="de50b-1118">方法</span><span class="sxs-lookup"><span data-stu-id="de50b-1118">Method</span></span>                                                                                                      | <span data-ttu-id="de50b-1119">説明</span><span class="sxs-lookup"><span data-stu-id="de50b-1119">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-1120">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1120">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1121">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1121">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1122">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1122">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="de50b-1123">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1123">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-1124">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1124">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="de50b-1125">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1125">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-1126">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="de50b-1126">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="de50b-1127">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1127">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="de50b-1128">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1128">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1129">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1129">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1130">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1130">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1131">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1131">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1132">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1132">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="de50b-1133">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1133">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="de50b-1134">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-1134">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="de50b-1135">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1135">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-1136">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1136">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1137">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1137">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1138">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1138">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1139">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="de50b-1139">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="de50b-1140">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1140">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="de50b-1141">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1141">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="de50b-1142">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1142">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-1143">public int columns(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1143">public int columns(\[int value\], \[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1144">public AutoMode columnsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1144">public AutoMode columnsMode(\[AutoMode mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1145">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1145">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1146">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1146">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1147">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1147">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1148">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1148">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1149">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1149">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="de50b-1150">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1150">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-1151">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="de50b-1151">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="de50b-1152">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1152">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="de50b-1153">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1153">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="de50b-1154">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1154">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="de50b-1155">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1155">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1156">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1156">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="de50b-1157">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1157">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="de50b-1158">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1158">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="de50b-1159">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1159">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-1160">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1160">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="de50b-1161">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1161">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span> |
| <span data-ttu-id="de50b-1162">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1162">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-1163">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1163">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="de50b-1164">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-1164">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="de50b-1165">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1165">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="de50b-1166">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-1166">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="de50b-1167">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1167">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="de50b-1168">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="de50b-1168">public str dragText()</span></span>                                                                                       | <span data-ttu-id="de50b-1169">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1169">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-1170">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1170">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="de50b-1171">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1171">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-1172">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1172">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="de50b-1173">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1173">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="de50b-1174">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="de50b-1174">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="de50b-1175">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1175">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="de50b-1176">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1176">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="de50b-1177">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1177">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-1178">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1178">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-1179">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1179">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-1180">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1180">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="de50b-1181">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1181">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-1182">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="de50b-1182">public str helpField()</span></span>                                                                                      | <span data-ttu-id="de50b-1183">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1183">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-1184">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1184">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="de50b-1185">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1185">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="de50b-1186">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1186">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1187">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1187">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="de50b-1188">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1188">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="de50b-1189">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="de50b-1189">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="de50b-1190">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1190">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-1191">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="de50b-1191">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1192">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="de50b-1192">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="de50b-1193">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1193">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="de50b-1194">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="de50b-1194">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="de50b-1195">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1195">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-1196">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="de50b-1196">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="de50b-1197">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1197">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="de50b-1198">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="de50b-1198">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1199">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1199">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="de50b-1200">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1200">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="de50b-1201">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1201">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1202">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1202">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1203">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1203">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1204">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1204">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-1205">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1205">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-1206">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1206">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-1207">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1207">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="de50b-1208">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1208">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="de50b-1209">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="de50b-1209">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="de50b-1210">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-1210">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="de50b-1211">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1211">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="de50b-1212">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-1212">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="de50b-1213">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1213">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-1214">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-1214">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="de50b-1215">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1215">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-1216">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-1216">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="de50b-1217">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1217">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="de50b-1218">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1218">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="de50b-1219">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1219">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="de50b-1220">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1220">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1221">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="de50b-1221">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1222">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="de50b-1222">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="de50b-1223">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1223">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-1224">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1224">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1225">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1225">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1226">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1226">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1227">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1227">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="de50b-1228">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1228">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-1229">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="de50b-1229">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="de50b-1230">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1230">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-1231">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1231">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="de50b-1232">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1232">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="de50b-1233">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1233">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1234">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="de50b-1234">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="de50b-1235">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1235">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-1236">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1236">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="de50b-1237">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1237">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-1238">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1238">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1239">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1239">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1240">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1240">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1241">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1241">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="de50b-1242">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1242">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-1243">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1243">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-1244">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1244">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-1245">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1245">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1246">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="de50b-1246">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1247">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1247">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-1248">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1248">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-1249">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1249">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="de50b-1250">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1250">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="de50b-1251">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1251">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="de50b-1252">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1252">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-1253">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1253">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="de50b-1254">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1254">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="de50b-1255">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1255">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-1256">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1256">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="de50b-1257">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1257">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-1258">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1258">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="de50b-1259">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1259">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="de50b-1260">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1260">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="de50b-1261">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1261">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="de50b-1262">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1262">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-1263">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1263">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="de50b-1264">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1264">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="de50b-1265">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1265">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="de50b-1266">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1266">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="de50b-1267">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1267">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-1268">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1268">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="de50b-1269">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1269">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-1270">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1270">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-1271">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1271">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="de50b-1272">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1272">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-1273">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1273">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="de50b-1274">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1274">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-1275">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1275">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="de50b-1276">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1276">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-1277">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1277">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="de50b-1278">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1278">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-1279">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1279">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="de50b-1280">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1280">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="de50b-1281">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1281">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-1282">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1282">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-1283">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1283">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-1284">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1284">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="de50b-1285">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1285">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1286">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-1286">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="de50b-1287">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1287">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="de50b-1288">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-1288">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="de50b-1289">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1289">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="de50b-1290">public void paste()</span><span class="sxs-lookup"><span data-stu-id="de50b-1290">public void paste()</span></span>                                                                                         | <span data-ttu-id="de50b-1291">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1291">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-1292">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-1292">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="de50b-1293">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1293">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="de50b-1294">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1294">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1295">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="de50b-1295">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="de50b-1296">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1296">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-1297">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-1297">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="de50b-1298">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1298">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="de50b-1299">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="de50b-1299">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="de50b-1300">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1300">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="de50b-1301">public void enter()</span><span class="sxs-lookup"><span data-stu-id="de50b-1301">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1302">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-1302">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="de50b-1303">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1303">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="de50b-1304">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-1304">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="de50b-1305">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1305">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-1306">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="de50b-1306">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1307">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1307">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1308">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1308">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1309">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="de50b-1309">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="de50b-1310">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1310">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="de50b-1311">public void cut()</span><span class="sxs-lookup"><span data-stu-id="de50b-1311">public void cut()</span></span>                                                                                           | <span data-ttu-id="de50b-1312">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="de50b-1312">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="de50b-1313">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1313">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1314">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="de50b-1314">public void displayControl()</span></span>                                                                                | <span data-ttu-id="de50b-1315">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1315">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="de50b-1316">public void copy()</span><span class="sxs-lookup"><span data-stu-id="de50b-1316">public void copy()</span></span>                                                                                          | <span data-ttu-id="de50b-1317">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="de50b-1317">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="de50b-1318">public void context()</span><span class="sxs-lookup"><span data-stu-id="de50b-1318">public void context()</span></span>                                                                                       | <span data-ttu-id="de50b-1319">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1319">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-1320">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="de50b-1320">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="de50b-1321">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="de50b-1321">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="de50b-1322">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="de50b-1322">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="de50b-1323">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1323">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="de50b-1324">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="de50b-1324">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-1325">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="de50b-1325">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="de50b-1326">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1326">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |

### <a name="method-alignchild"></a><span data-ttu-id="de50b-1327">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="de50b-1327">Method alignChild</span></span>

    public boolean alignChild([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1328">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1328">Parameters</span></span>

<span data-ttu-id="de50b-1329">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1329">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1330">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1330">Return Value</span></span>

### <a name="method-alignchildren"></a><span data-ttu-id="de50b-1331">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="de50b-1331">Method alignChildren</span></span>

    public boolean alignChildren([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1332">Parameters</span></span>

<span data-ttu-id="de50b-1333">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1333">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1334">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1334">Return Value</span></span>

### <a name="method-aligncontrol"></a><span data-ttu-id="de50b-1335">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="de50b-1335">Method alignControl</span></span>

<span data-ttu-id="de50b-1336">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1336">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1337">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1337">Parameters</span></span>

<span data-ttu-id="de50b-1338">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1338">value</span></span>  
<span data-ttu-id="de50b-1339">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1339">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1340">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1340">Return Value</span></span>

<span data-ttu-id="de50b-1341">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1341">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1342">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1342">Remarks</span></span>

<span data-ttu-id="de50b-1343">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1343">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="de50b-1344">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="de50b-1344">Method allowEdit</span></span>

<span data-ttu-id="de50b-1345">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1345">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1346">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1346">Parameters</span></span>

<span data-ttu-id="de50b-1347">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1347">value</span></span>  
<span data-ttu-id="de50b-1348">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1348">The value to assign to the allowEdit property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1349">Return Value</span></span>

<span data-ttu-id="de50b-1350">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1350">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1351">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1351">Remarks</span></span>

<span data-ttu-id="de50b-1352">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1352">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="de50b-1353">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="de50b-1353">Method allowSysSetup</span></span>

<span data-ttu-id="de50b-1354">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1354">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="de50b-1355">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1355">Return Value</span></span>

<span data-ttu-id="de50b-1356">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1356">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-allowusersetup"></a><span data-ttu-id="de50b-1357">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="de50b-1357">Method allowUserSetup</span></span>

    public int allowUserSetup([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1358">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1358">Parameters</span></span>

<span data-ttu-id="de50b-1359">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1359">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1360">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1360">Return Value</span></span>

### <a name="method-arrangeguide"></a><span data-ttu-id="de50b-1361">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="de50b-1361">Method arrangeGuide</span></span>

    public int arrangeGuide([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1362">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1362">Parameters</span></span>

<span data-ttu-id="de50b-1363">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1363">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1364">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1364">Return Value</span></span>

### <a name="method-arrangemethod"></a><span data-ttu-id="de50b-1365">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="de50b-1365">Method arrangeMethod</span></span>

    public int arrangeMethod([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1366">Parameters</span></span>

<span data-ttu-id="de50b-1367">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1368">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1368">Return Value</span></span>

### <a name="method-arrangewhen"></a><span data-ttu-id="de50b-1369">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="de50b-1369">Method arrangeWhen</span></span>

    public int arrangeWhen([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1370">Parameters</span></span>

<span data-ttu-id="de50b-1371">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1371">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1372">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1372">Return Value</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="de50b-1373">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="de50b-1373">Method autoDeclaration</span></span>

<span data-ttu-id="de50b-1374">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1374">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1375">Parameters</span></span>

<span data-ttu-id="de50b-1376">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1376">value</span></span>  
<span data-ttu-id="de50b-1377">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1377">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1378">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1378">Return Value</span></span>

<span data-ttu-id="de50b-1379">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1379">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1380">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1380">Remarks</span></span>

<span data-ttu-id="de50b-1381">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1381">Controls cannot have identical names.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="de50b-1382">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="de50b-1382">Method beginDrag</span></span>

<span data-ttu-id="de50b-1383">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1383">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-1384">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1384">Parameters</span></span>

<span data-ttu-id="de50b-1385">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1385">x</span></span>  
<span data-ttu-id="de50b-1386">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1386">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="de50b-1387">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-1387">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="de50b-1388">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1388">y</span></span>  
<span data-ttu-id="de50b-1389">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1389">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="de50b-1390">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-1390">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1391">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1391">Return Value</span></span>

<span data-ttu-id="de50b-1392">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1392">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1393">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1393">Remarks</span></span>

<span data-ttu-id="de50b-1394">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1394">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="de50b-1395">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1395">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-bottommargin"></a><span data-ttu-id="de50b-1396">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="de50b-1396">Method bottomMargin</span></span>

    public int bottomMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1397">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1397">Parameters</span></span>

<span data-ttu-id="de50b-1398">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1398">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-1399">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1399">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1400">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1400">Return Value</span></span>

### <a name="method-bottommarginmode"></a><span data-ttu-id="de50b-1401">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1401">Method bottomMarginMode</span></span>

    public AutoMode bottomMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1402">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1402">Parameters</span></span>

<span data-ttu-id="de50b-1403">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1403">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1404">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1404">Return Value</span></span>

### <a name="method-bottommarginvalue"></a><span data-ttu-id="de50b-1405">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1405">Method bottomMarginValue</span></span>

    public int bottomMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1406">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1406">Parameters</span></span>

<span data-ttu-id="de50b-1407">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1407">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1408">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1408">Return Value</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="de50b-1409">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="de50b-1409">Method calcControlSize</span></span>

<span data-ttu-id="de50b-1410">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1410">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="de50b-1411">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1411">Parameters</span></span>

<span data-ttu-id="de50b-1412">chars</span><span class="sxs-lookup"><span data-stu-id="de50b-1412">chars</span></span>  
<span data-ttu-id="de50b-1413">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="de50b-1413">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="de50b-1414">明細行</span><span class="sxs-lookup"><span data-stu-id="de50b-1414">lines</span></span>  
<span data-ttu-id="de50b-1415">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="de50b-1415">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1416">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1416">Return Value</span></span>

<span data-ttu-id="de50b-1417">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="de50b-1417">The container that holds the width and height.</span></span>

### <a name="method-caption"></a><span data-ttu-id="de50b-1418">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="de50b-1418">Method caption</span></span>

<span data-ttu-id="de50b-1419">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1419">Gets or set the caption of the control.</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1420">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1420">Parameters</span></span>

<span data-ttu-id="de50b-1421">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1421">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1422">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1422">Return Value</span></span>

<span data-ttu-id="de50b-1423">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-1423">The string that is used as the caption of the control.</span></span>

### <a name="method-columns"></a><span data-ttu-id="de50b-1424">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="de50b-1424">Method columns</span></span>

    public int columns([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1425">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1425">Parameters</span></span>

<span data-ttu-id="de50b-1426">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1426">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-1427">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1427">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1428">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1428">Return Value</span></span>

### <a name="method-columnsmode"></a><span data-ttu-id="de50b-1429">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1429">Method columnsMode</span></span>

    public AutoMode columnsMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1430">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1430">Parameters</span></span>

<span data-ttu-id="de50b-1431">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1431">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1432">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1432">Return Value</span></span>

### <a name="method-columnspace"></a><span data-ttu-id="de50b-1433">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="de50b-1433">Method columnspace</span></span>

    public int columnspace([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1434">Parameters</span></span>

<span data-ttu-id="de50b-1435">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1435">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-1436">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1436">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1437">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1437">Return Value</span></span>

### <a name="method-columnspacemode"></a><span data-ttu-id="de50b-1438">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1438">Method columnspaceMode</span></span>

    public AutoMode columnspaceMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1439">Parameters</span></span>

<span data-ttu-id="de50b-1440">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1440">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1441">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1441">Return Value</span></span>

### <a name="method-columnspacevalue"></a><span data-ttu-id="de50b-1442">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1442">Method columnspaceValue</span></span>

    public int columnspaceValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1443">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1443">Parameters</span></span>

<span data-ttu-id="de50b-1444">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1444">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1445">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1445">Return Value</span></span>

### <a name="method-columnsvalue"></a><span data-ttu-id="de50b-1446">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1446">Method columnsValue</span></span>

    public int columnsValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1447">Parameters</span></span>

<span data-ttu-id="de50b-1448">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1448">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1449">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1449">Return Value</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="de50b-1450">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="de50b-1450">Method configurationKey</span></span>

<span data-ttu-id="de50b-1451">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1451">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1452">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1452">Parameters</span></span>

<span data-ttu-id="de50b-1453">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1453">value</span></span>  
<span data-ttu-id="de50b-1454">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1454">The ID of the configuration key being assigned to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1455">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1455">Return Value</span></span>

<span data-ttu-id="de50b-1456">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-1456">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1457">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1457">Remarks</span></span>

<span data-ttu-id="de50b-1458">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1458">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="de50b-1459">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1459">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="de50b-1460">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="de50b-1460">Method configurationKeyEx</span></span>

<span data-ttu-id="de50b-1461">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1461">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="de50b-1462">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1462">Return Value</span></span>

<span data-ttu-id="de50b-1463">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="de50b-1463">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1464">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1464">Remarks</span></span>

<span data-ttu-id="de50b-1465">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1465">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="de50b-1466">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1466">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="de50b-1467">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1467">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="de50b-1468">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="de50b-1468">Method countryRegionCodes</span></span>

<span data-ttu-id="de50b-1469">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1469">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1470">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1470">Parameters</span></span>

<span data-ttu-id="de50b-1471">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1471">value</span></span>  
<span data-ttu-id="de50b-1472">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1472">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1473">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1473">Return Value</span></span>

<span data-ttu-id="de50b-1474">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-1474">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-countryregioncontextfield"></a><span data-ttu-id="de50b-1475">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="de50b-1475">Method countryRegionContextField</span></span>

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1476">Parameters</span></span>

<span data-ttu-id="de50b-1477">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1477">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1478">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1478">Return Value</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="de50b-1479">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="de50b-1479">Method dataRelationPath</span></span>

<span data-ttu-id="de50b-1480">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1480">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1481">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1481">Parameters</span></span>

<span data-ttu-id="de50b-1482">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1482">value</span></span>  
<span data-ttu-id="de50b-1483">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1483">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1484">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1484">Return Value</span></span>

<span data-ttu-id="de50b-1485">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="de50b-1485">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1486">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1486">Remarks</span></span>

<span data-ttu-id="de50b-1487">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1487">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="de50b-1488">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="de50b-1488">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-datasource"></a><span data-ttu-id="de50b-1489">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="de50b-1489">Method dataSource</span></span>

<span data-ttu-id="de50b-1490">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1490">Gets or sets a data source to be used by the control or the form.</span></span>

    public int dataSource([AnyType value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1491">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1491">Parameters</span></span>

<span data-ttu-id="de50b-1492">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1492">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1493">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1493">Return Value</span></span>

<span data-ttu-id="de50b-1494">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-1494">The identifier of the data source to be used.</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="de50b-1495">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="de50b-1495">Method displayTarget</span></span>

<span data-ttu-id="de50b-1496">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1496">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1497">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1497">Parameters</span></span>

<span data-ttu-id="de50b-1498">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1498">value</span></span>  
<span data-ttu-id="de50b-1499">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1499">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1500">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1500">Return Value</span></span>

<span data-ttu-id="de50b-1501">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1501">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="de50b-1502">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="de50b-1502">Method dragDrop</span></span>

<span data-ttu-id="de50b-1503">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1503">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1504">Parameters</span></span>

<span data-ttu-id="de50b-1505">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1505">value</span></span>  
<span data-ttu-id="de50b-1506">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1506">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1507">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1507">Return Value</span></span>

<span data-ttu-id="de50b-1508">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1508">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1509">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1509">Remarks</span></span>

<span data-ttu-id="de50b-1510">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1510">Use the dragLeave , the dragOver, and the dragOverEx to specify the behavior.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="de50b-1511">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="de50b-1511">Method dragOver</span></span>

<span data-ttu-id="de50b-1512">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1512">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-1513">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1513">Parameters</span></span>

<span data-ttu-id="de50b-1514">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-1514">dragSource</span></span>  
<span data-ttu-id="de50b-1515">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1515">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1516">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1516">dragMode</span></span>  
<span data-ttu-id="de50b-1517">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1517">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1518">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1518">x</span></span>  
<span data-ttu-id="de50b-1519">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1519">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1520">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1520">y</span></span>  
<span data-ttu-id="de50b-1521">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1521">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1522">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1522">Return Value</span></span>

<span data-ttu-id="de50b-1523">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1523">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="de50b-1524">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="de50b-1524">Method dragOverEx</span></span>

<span data-ttu-id="de50b-1525">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1525">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-1526">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1526">Parameters</span></span>

<span data-ttu-id="de50b-1527">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-1527">dragSource</span></span>  
<span data-ttu-id="de50b-1528">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1528">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1529">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1529">dragMode</span></span>  
<span data-ttu-id="de50b-1530">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1530">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1531">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1531">x</span></span>  
<span data-ttu-id="de50b-1532">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1532">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-1533">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1533">y</span></span>  
<span data-ttu-id="de50b-1534">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1534">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1535">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1535">Return Value</span></span>

<span data-ttu-id="de50b-1536">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1536">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="de50b-1537">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="de50b-1537">Method dragText</span></span>

<span data-ttu-id="de50b-1538">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1538">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="de50b-1539">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1539">Return Value</span></span>

<span data-ttu-id="de50b-1540">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-1540">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="de50b-1541">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="de50b-1541">Method enabled</span></span>

<span data-ttu-id="de50b-1542">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1542">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1543">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1543">Parameters</span></span>

<span data-ttu-id="de50b-1544">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1544">value</span></span>  
<span data-ttu-id="de50b-1545">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1545">A Boolean value that indicates whether the control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1546">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1546">Return Value</span></span>

<span data-ttu-id="de50b-1547">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1547">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1548">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1548">Remarks</span></span>

<span data-ttu-id="de50b-1549">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1549">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="de50b-1550">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1550">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="de50b-1551">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1551">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="de50b-1552">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="de50b-1552">Method hasChanged</span></span>

<span data-ttu-id="de50b-1553">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1553">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="de50b-1554">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1554">Parameters</span></span>

<span data-ttu-id="de50b-1555">val</span><span class="sxs-lookup"><span data-stu-id="de50b-1555">val</span></span>  
<span data-ttu-id="de50b-1556">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1556">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1557">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1557">Return Value</span></span>

<span data-ttu-id="de50b-1558">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1558">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="de50b-1559">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="de50b-1559">Method hasUserSetting</span></span>

<span data-ttu-id="de50b-1560">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1560">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="de50b-1561">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1561">Return Value</span></span>

<span data-ttu-id="de50b-1562">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1562">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="de50b-1563">メソッド height</span><span class="sxs-lookup"><span data-stu-id="de50b-1563">Method height</span></span>

<span data-ttu-id="de50b-1564">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1564">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1565">Parameters</span></span>

<span data-ttu-id="de50b-1566">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1566">value</span></span>  
<span data-ttu-id="de50b-1567">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1567">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-1568">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1568">mode</span></span>  
<span data-ttu-id="de50b-1569">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1569">An Integer that indicates how the height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1570">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1570">Return Value</span></span>

<span data-ttu-id="de50b-1571">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-1571">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1572">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1572">Remarks</span></span>

<span data-ttu-id="de50b-1573">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1573">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="de50b-1574">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-1574">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="de50b-1575">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-1575">Mode.</span></span>            | <span data-ttu-id="de50b-1576">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-1576">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-1577">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-1577">-1 Exact.</span></span>        | <span data-ttu-id="de50b-1578">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1578">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-1579">0 自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-1579">0 Auto.</span></span>          | <span data-ttu-id="de50b-1580">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1580">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-1581">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-1581">1 Column height.</span></span> | <span data-ttu-id="de50b-1582">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1582">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="de50b-1583">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1583">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="de50b-1584">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1584">Method heightMode</span></span>

<span data-ttu-id="de50b-1585">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1585">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1586">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1586">Parameters</span></span>

<span data-ttu-id="de50b-1587">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1587">value</span></span>  
<span data-ttu-id="de50b-1588">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1588">An integer value that indicates how control height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1589">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1589">Return Value</span></span>

<span data-ttu-id="de50b-1590">計算モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-1590">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1591">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1591">Remarks</span></span>

<span data-ttu-id="de50b-1592">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-1592">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="de50b-1593">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-1593">Mode.</span></span>          | <span data-ttu-id="de50b-1594">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-1594">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-1595">正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-1595">Exact.</span></span>         | <span data-ttu-id="de50b-1596">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1596">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-1597">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-1597">Auto.</span></span>          | <span data-ttu-id="de50b-1598">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1598">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-1599">列の高さ</span><span class="sxs-lookup"><span data-stu-id="de50b-1599">Column height.</span></span> | <span data-ttu-id="de50b-1600">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1600">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="de50b-1601">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1601">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="de50b-1602">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1602">Method heightValue</span></span>

<span data-ttu-id="de50b-1603">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1603">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1604">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1604">Parameters</span></span>

<span data-ttu-id="de50b-1605">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1605">value</span></span>  
<span data-ttu-id="de50b-1606">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1606">An Integer that specifies the height in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1607">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1607">Return Value</span></span>

<span data-ttu-id="de50b-1608">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-1608">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1609">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1609">Remarks</span></span>

<span data-ttu-id="de50b-1610">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1610">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="de50b-1611">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="de50b-1611">Method helpField</span></span>

<span data-ttu-id="de50b-1612">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1612">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="de50b-1613">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1613">Return Value</span></span>

<span data-ttu-id="de50b-1614">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-1614">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1615">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1615">Remarks</span></span>

<span data-ttu-id="de50b-1616">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1616">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="de50b-1617">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1617">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="de50b-1618">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="de50b-1618">Method helpText</span></span>

<span data-ttu-id="de50b-1619">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1619">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1620">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1620">Parameters</span></span>

<span data-ttu-id="de50b-1621">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1621">value</span></span>  
<span data-ttu-id="de50b-1622">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1622">The value that is assigned as the Help text for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1623">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1623">Return Value</span></span>

<span data-ttu-id="de50b-1624">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-1624">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1625">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1625">Remarks</span></span>

<span data-ttu-id="de50b-1626">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1626">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="de50b-1627">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1627">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hideifempty"></a><span data-ttu-id="de50b-1628">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="de50b-1628">Method hideIfEmpty</span></span>

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1629">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1629">Parameters</span></span>

<span data-ttu-id="de50b-1630">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1630">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1631">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1631">Return Value</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="de50b-1632">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="de50b-1632">Method hierarchyParent</span></span>

<span data-ttu-id="de50b-1633">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1633">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1634">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1634">Parameters</span></span>

<span data-ttu-id="de50b-1635">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1635">value</span></span>  
<span data-ttu-id="de50b-1636">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1636">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1637">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1637">Return Value</span></span>

<span data-ttu-id="de50b-1638">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1638">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="de50b-1639">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="de50b-1639">Method hWnd</span></span>

<span data-ttu-id="de50b-1640">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1640">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="de50b-1641">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1641">Return Value</span></span>

<span data-ttu-id="de50b-1642">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="de50b-1642">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1643">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1643">Remarks</span></span>

<span data-ttu-id="de50b-1644">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1644">The handle can be used with the Windows API.</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="de50b-1645">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="de50b-1645">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="de50b-1646">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1646">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="de50b-1647">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="de50b-1647">Method isDisplayed</span></span>

<span data-ttu-id="de50b-1648">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1648">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="de50b-1649">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1649">Return Value</span></span>

<span data-ttu-id="de50b-1650">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1650">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1651">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1651">Remarks</span></span>

<span data-ttu-id="de50b-1652">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1652">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="de50b-1653">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="de50b-1653">Method isRestricted</span></span>

<span data-ttu-id="de50b-1654">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1654">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="de50b-1655">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1655">Return Value</span></span>

<span data-ttu-id="de50b-1656">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1656">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="de50b-1657">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="de50b-1657">Method isUserSetupEnabled</span></span>

<span data-ttu-id="de50b-1658">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1658">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="de50b-1659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1659">Parameters</span></span>

<span data-ttu-id="de50b-1660">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="de50b-1660">neededSetupRights</span></span>  
<span data-ttu-id="de50b-1661">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1661">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1662">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1662">Return Value</span></span>

<span data-ttu-id="de50b-1663">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1663">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1664">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1664">Remarks</span></span>

<span data-ttu-id="de50b-1665">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1665">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-1666">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="de50b-1666">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="de50b-1667">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1667">No changes can be made to the control.</span></span> <span data-ttu-id="de50b-1668">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1668">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="de50b-1669">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="de50b-1669">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="de50b-1670">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1670">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="de50b-1671">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1671">The user cannot move the control.</span></span>   |
| <span data-ttu-id="de50b-1672">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="de50b-1672">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="de50b-1673">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1673">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="de50b-1674">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1674">The user can also move the control.</span></span> |

<span data-ttu-id="de50b-1675">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1675">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="method-leave"></a><span data-ttu-id="de50b-1676">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="de50b-1676">Method leave</span></span>

    public boolean leave()

#### <a name="return-value"></a><span data-ttu-id="de50b-1677">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1677">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="de50b-1678">メソッド left</span><span class="sxs-lookup"><span data-stu-id="de50b-1678">Method left</span></span>

<span data-ttu-id="de50b-1679">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1679">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1680">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1680">Parameters</span></span>

<span data-ttu-id="de50b-1681">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1681">value</span></span>  
<span data-ttu-id="de50b-1682">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1682">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-1683">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1683">mode</span></span>  
<span data-ttu-id="de50b-1684">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1684">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1685">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1685">Return Value</span></span>

<span data-ttu-id="de50b-1686">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-1686">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="de50b-1687">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="de50b-1687">Method leftMargin</span></span>

    public int leftMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1688">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1688">Parameters</span></span>

<span data-ttu-id="de50b-1689">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1689">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-1690">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1690">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1691">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1691">Return Value</span></span>

### <a name="method-leftmarginmode"></a><span data-ttu-id="de50b-1692">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1692">Method leftMarginMode</span></span>

    public AutoMode leftMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1693">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1693">Parameters</span></span>

<span data-ttu-id="de50b-1694">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1694">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1695">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1695">Return Value</span></span>

### <a name="method-leftmarginvalue"></a><span data-ttu-id="de50b-1696">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1696">Method leftMarginValue</span></span>

    public int leftMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1697">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1697">Parameters</span></span>

<span data-ttu-id="de50b-1698">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1698">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1699">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1699">Return Value</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="de50b-1700">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1700">Method leftMode</span></span>

<span data-ttu-id="de50b-1701">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1701">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1702">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1702">Parameters</span></span>

<span data-ttu-id="de50b-1703">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1703">value</span></span>  
<span data-ttu-id="de50b-1704">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1704">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1705">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1705">Return Value</span></span>

<span data-ttu-id="de50b-1706">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-1706">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="de50b-1707">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1707">Method leftValue</span></span>

<span data-ttu-id="de50b-1708">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1708">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1709">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1709">Parameters</span></span>

<span data-ttu-id="de50b-1710">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1710">value</span></span>  
<span data-ttu-id="de50b-1711">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1711">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1712">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1712">Return Value</span></span>

<span data-ttu-id="de50b-1713">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-1713">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="de50b-1714">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="de50b-1714">Method markAsUserAdd</span></span>

<span data-ttu-id="de50b-1715">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="de50b-1715">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1716">Parameters</span></span>

<span data-ttu-id="de50b-1717">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1717">value</span></span>  
<span data-ttu-id="de50b-1718">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1718">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1719">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1719">Return Value</span></span>

<span data-ttu-id="de50b-1720">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1720">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="de50b-1721">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="de50b-1721">Method mouseDblClick</span></span>

<span data-ttu-id="de50b-1722">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1722">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-1723">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1723">Parameters</span></span>

<span data-ttu-id="de50b-1724">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1724">x</span></span>  
<span data-ttu-id="de50b-1725">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1725">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1726">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1726">y</span></span>  
<span data-ttu-id="de50b-1727">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1727">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1728">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-1728">button</span></span>  
<span data-ttu-id="de50b-1729">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1729">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1730">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-1730">Ctrl</span></span>  
<span data-ttu-id="de50b-1731">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1731">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1732">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-1732">Shift</span></span>  
<span data-ttu-id="de50b-1733">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1733">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1734">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1734">Return Value</span></span>

<span data-ttu-id="de50b-1735">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1735">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1736">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1736">Remarks</span></span>

<span data-ttu-id="de50b-1737">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1737">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="de50b-1738">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="de50b-1738">Method mouseDown</span></span>

<span data-ttu-id="de50b-1739">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1739">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-1740">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1740">Parameters</span></span>

<span data-ttu-id="de50b-1741">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1741">x</span></span>  
<span data-ttu-id="de50b-1742">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1742">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1743">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1743">y</span></span>  
<span data-ttu-id="de50b-1744">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1744">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1745">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-1745">button</span></span>  
<span data-ttu-id="de50b-1746">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1746">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1747">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-1747">Ctrl</span></span>  
<span data-ttu-id="de50b-1748">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1748">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1749">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-1749">Shift</span></span>  
<span data-ttu-id="de50b-1750">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1750">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1751">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1751">Return Value</span></span>

<span data-ttu-id="de50b-1752">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1752">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1753">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1753">Remarks</span></span>

<span data-ttu-id="de50b-1754">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1754">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="de50b-1755">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1755">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="de50b-1756">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="de50b-1756">Method mouseMove</span></span>

<span data-ttu-id="de50b-1757">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1757">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-1758">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1758">Parameters</span></span>

<span data-ttu-id="de50b-1759">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1759">x</span></span>  
<span data-ttu-id="de50b-1760">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1760">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1761">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1761">y</span></span>  
<span data-ttu-id="de50b-1762">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1762">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1763">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-1763">button</span></span>  
<span data-ttu-id="de50b-1764">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1764">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1765">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-1765">Ctrl</span></span>  
<span data-ttu-id="de50b-1766">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1766">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1767">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-1767">Shift</span></span>  
<span data-ttu-id="de50b-1768">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1768">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1769">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1769">Return Value</span></span>

<span data-ttu-id="de50b-1770">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1770">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1771">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1771">Remarks</span></span>

<span data-ttu-id="de50b-1772">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1772">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="de50b-1773">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="de50b-1773">Method mouseUp</span></span>

<span data-ttu-id="de50b-1774">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1774">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-1775">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1775">Parameters</span></span>

<span data-ttu-id="de50b-1776">x</span><span class="sxs-lookup"><span data-stu-id="de50b-1776">x</span></span>  
<span data-ttu-id="de50b-1777">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1777">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1778">y</span><span class="sxs-lookup"><span data-stu-id="de50b-1778">y</span></span>  
<span data-ttu-id="de50b-1779">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1779">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1780">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-1780">button</span></span>  
<span data-ttu-id="de50b-1781">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1781">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1782">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-1782">Ctrl</span></span>  
<span data-ttu-id="de50b-1783">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1783">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-1784">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-1784">Shift</span></span>  
<span data-ttu-id="de50b-1785">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1785">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1786">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1786">Return Value</span></span>

<span data-ttu-id="de50b-1787">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1787">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1788">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1788">Remarks</span></span>

<span data-ttu-id="de50b-1789">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1789">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="de50b-1790">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1790">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-name"></a><span data-ttu-id="de50b-1791">メソッド名</span><span class="sxs-lookup"><span data-stu-id="de50b-1791">Method name</span></span>

<span data-ttu-id="de50b-1792">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1792">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1793">Parameters</span></span>

<span data-ttu-id="de50b-1794">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1794">value</span></span>  
<span data-ttu-id="de50b-1795">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-1795">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1796">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1796">Return Value</span></span>

<span data-ttu-id="de50b-1797">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-1797">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1798">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1798">Remarks</span></span>

<span data-ttu-id="de50b-1799">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1799">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="de50b-1800">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1800">It must begin with a letter.</span></span>
-   <span data-ttu-id="de50b-1801">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1801">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="de50b-1802">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1802">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="de50b-1803">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1803">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="de50b-1804">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-1804">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="de50b-1805">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="de50b-1805">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1806">Parameters</span></span>

<span data-ttu-id="de50b-1807">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1807">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1808">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1808">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="de50b-1809">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="de50b-1809">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="de50b-1810">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1810">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="de50b-1811">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="de50b-1811">Method parentControl</span></span>

<span data-ttu-id="de50b-1812">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1812">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="de50b-1813">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1813">Return Value</span></span>

<span data-ttu-id="de50b-1814">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="de50b-1814">The parent control for the control.</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="de50b-1815">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="de50b-1815">Method rightMargin</span></span>

    public int rightMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1816">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1816">Parameters</span></span>

<span data-ttu-id="de50b-1817">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1817">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-1818">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1818">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1819">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1819">Return Value</span></span>

### <a name="method-rightmarginmode"></a><span data-ttu-id="de50b-1820">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1820">Method rightMarginMode</span></span>

    public AutoMode rightMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1821">Parameters</span></span>

<span data-ttu-id="de50b-1822">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1822">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1823">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1823">Return Value</span></span>

### <a name="method-rightmarginvalue"></a><span data-ttu-id="de50b-1824">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1824">Method rightMarginValue</span></span>

    public int rightMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1825">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1825">Parameters</span></span>

<span data-ttu-id="de50b-1826">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1826">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1827">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1827">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="de50b-1828">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="de50b-1828">Method securityKey</span></span>

<span data-ttu-id="de50b-1829">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1829">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1830">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1830">Parameters</span></span>

<span data-ttu-id="de50b-1831">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1831">value</span></span>  
<span data-ttu-id="de50b-1832">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1832">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1833">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1833">Return Value</span></span>

<span data-ttu-id="de50b-1834">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1834">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="de50b-1835">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="de50b-1835">Method showContextMenu</span></span>

<span data-ttu-id="de50b-1836">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1836">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="de50b-1837">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1837">Parameters</span></span>

<span data-ttu-id="de50b-1838">menuHandle</span><span class="sxs-lookup"><span data-stu-id="de50b-1838">menuHandle</span></span>  
<span data-ttu-id="de50b-1839">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-1839">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1840">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1840">Return Value</span></span>

<span data-ttu-id="de50b-1841">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-1841">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-skip"></a><span data-ttu-id="de50b-1842">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="de50b-1842">Method skip</span></span>

<span data-ttu-id="de50b-1843">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1843">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1844">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1844">Parameters</span></span>

<span data-ttu-id="de50b-1845">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1845">value</span></span>  
<span data-ttu-id="de50b-1846">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1846">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1847">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1847">Return Value</span></span>

<span data-ttu-id="de50b-1848">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-1848">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1849">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1849">Remarks</span></span>

<span data-ttu-id="de50b-1850">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1850">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="method-sort"></a><span data-ttu-id="de50b-1851">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="de50b-1851">Method sort</span></span>

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a><span data-ttu-id="de50b-1852">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1852">Parameters</span></span>

<span data-ttu-id="de50b-1853">sortDirection</span><span class="sxs-lookup"><span data-stu-id="de50b-1853">sortDirection</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1854">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1854">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="de50b-1855">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="de50b-1855">Method toolTip</span></span>

<span data-ttu-id="de50b-1856">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1856">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="de50b-1857">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1857">Return Value</span></span>

<span data-ttu-id="de50b-1858">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-1858">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1859">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1859">Remarks</span></span>

<span data-ttu-id="de50b-1860">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1860">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="de50b-1861">メソッド top</span><span class="sxs-lookup"><span data-stu-id="de50b-1861">Method top</span></span>

<span data-ttu-id="de50b-1862">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1862">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1863">Parameters</span></span>

<span data-ttu-id="de50b-1864">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1864">value</span></span>  
<span data-ttu-id="de50b-1865">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1865">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-1866">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1866">mode</span></span>  
<span data-ttu-id="de50b-1867">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1867">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1868">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1868">Return Value</span></span>

<span data-ttu-id="de50b-1869">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-1869">The vertical position of the control in the form.</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="de50b-1870">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="de50b-1870">Method topMargin</span></span>

    public int topMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1871">Parameters</span></span>

<span data-ttu-id="de50b-1872">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1872">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-1873">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1873">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1874">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1874">Return Value</span></span>

### <a name="method-topmarginmode"></a><span data-ttu-id="de50b-1875">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1875">Method topMarginMode</span></span>

    public AutoMode topMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-1876">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1876">Parameters</span></span>

<span data-ttu-id="de50b-1877">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-1877">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1878">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1878">Return Value</span></span>

### <a name="method-topmarginvalue"></a><span data-ttu-id="de50b-1879">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1879">Method topMarginValue</span></span>

    public int topMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1880">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1880">Parameters</span></span>

<span data-ttu-id="de50b-1881">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1881">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1882">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1882">Return Value</span></span>

### <a name="method-topmode"></a><span data-ttu-id="de50b-1883">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="de50b-1883">Method topMode</span></span>

<span data-ttu-id="de50b-1884">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1884">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1885">Parameters</span></span>

<span data-ttu-id="de50b-1886">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1886">value</span></span>  
<span data-ttu-id="de50b-1887">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1887">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1888">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1888">Return Value</span></span>

<span data-ttu-id="de50b-1889">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-1889">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="de50b-1890">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="de50b-1890">Method topValue</span></span>

<span data-ttu-id="de50b-1891">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1891">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1892">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1892">Parameters</span></span>

<span data-ttu-id="de50b-1893">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1893">value</span></span>  
<span data-ttu-id="de50b-1894">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1894">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1895">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1895">Return Value</span></span>

<span data-ttu-id="de50b-1896">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-1896">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="de50b-1897">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="de50b-1897">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1898">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1898">Parameters</span></span>

<span data-ttu-id="de50b-1899">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1899">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1900">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1900">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="de50b-1901">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="de50b-1901">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="de50b-1902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1902">Parameters</span></span>

<span data-ttu-id="de50b-1903">データ</span><span class="sxs-lookup"><span data-stu-id="de50b-1903">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-1904">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1904">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="de50b-1905">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="de50b-1905">Method userData</span></span>

<span data-ttu-id="de50b-1906">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1906">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1907">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1907">Parameters</span></span>

<span data-ttu-id="de50b-1908">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1908">value</span></span>  
<span data-ttu-id="de50b-1909">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1909">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1910">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1910">Return Value</span></span>

<span data-ttu-id="de50b-1911">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="de50b-1911">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="de50b-1912">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="de50b-1912">Method userDataItem</span></span>

<span data-ttu-id="de50b-1913">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1913">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1914">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1914">Parameters</span></span>

<span data-ttu-id="de50b-1915">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1915">value</span></span>  
<span data-ttu-id="de50b-1916">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1916">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1917">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1917">Return Value</span></span>

<span data-ttu-id="de50b-1918">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="de50b-1918">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="de50b-1919">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="de50b-1919">Method userDataItems</span></span>

<span data-ttu-id="de50b-1920">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1920">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1921">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1921">Parameters</span></span>

<span data-ttu-id="de50b-1922">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1922">value</span></span>  
<span data-ttu-id="de50b-1923">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-1923">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1924">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1924">Return Value</span></span>

<span data-ttu-id="de50b-1925">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="de50b-1925">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="de50b-1926">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="de50b-1926">Method userDisable</span></span>

<span data-ttu-id="de50b-1927">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1927">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1928">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1928">Parameters</span></span>

<span data-ttu-id="de50b-1929">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1929">value</span></span>  
<span data-ttu-id="de50b-1930">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1930">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1931">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1931">Return Value</span></span>

<span data-ttu-id="de50b-1932">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1932">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="de50b-1933">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="de50b-1933">Method userHeight</span></span>

<span data-ttu-id="de50b-1934">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1934">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1935">Parameters</span></span>

<span data-ttu-id="de50b-1936">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1936">value</span></span>  
<span data-ttu-id="de50b-1937">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1937">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1938">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1938">Return Value</span></span>

<span data-ttu-id="de50b-1939">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-1939">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="de50b-1940">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="de50b-1940">Method userHide</span></span>

<span data-ttu-id="de50b-1941">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1941">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1942">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1942">Parameters</span></span>

<span data-ttu-id="de50b-1943">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1943">value</span></span>  
<span data-ttu-id="de50b-1944">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1944">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1945">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1945">Return Value</span></span>

<span data-ttu-id="de50b-1946">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1946">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1947">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1947">Remarks</span></span>

<span data-ttu-id="de50b-1948">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1948">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="de50b-1949">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1949">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="de50b-1950">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1950">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="de50b-1951">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="de50b-1951">Method userOrgContainer</span></span>

<span data-ttu-id="de50b-1952">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1952">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1953">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1953">Parameters</span></span>

<span data-ttu-id="de50b-1954">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1954">value</span></span>  
<span data-ttu-id="de50b-1955">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1955">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1956">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1956">Return Value</span></span>

<span data-ttu-id="de50b-1957">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="de50b-1957">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="de50b-1958">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="de50b-1958">Method userOrgSibling</span></span>

<span data-ttu-id="de50b-1959">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1959">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1960">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1960">Parameters</span></span>

<span data-ttu-id="de50b-1961">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1961">value</span></span>  
<span data-ttu-id="de50b-1962">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1962">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1963">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1963">Return Value</span></span>

<span data-ttu-id="de50b-1964">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="de50b-1964">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="de50b-1965">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="de50b-1965">Method userPromptText</span></span>

<span data-ttu-id="de50b-1966">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1966">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1967">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1967">Parameters</span></span>

<span data-ttu-id="de50b-1968">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1968">value</span></span>  
<span data-ttu-id="de50b-1969">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1969">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1970">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1970">Return Value</span></span>

<span data-ttu-id="de50b-1971">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-1971">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="de50b-1972">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="de50b-1972">Method userSecurityLevel</span></span>

<span data-ttu-id="de50b-1973">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1973">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1974">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1974">Parameters</span></span>

<span data-ttu-id="de50b-1975">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1975">value</span></span>  
<span data-ttu-id="de50b-1976">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1976">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1977">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1977">Return Value</span></span>

<span data-ttu-id="de50b-1978">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="de50b-1978">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="de50b-1979">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="de50b-1979">Method userSkip</span></span>

<span data-ttu-id="de50b-1980">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1980">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1981">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1981">Parameters</span></span>

<span data-ttu-id="de50b-1982">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1982">value</span></span>  
<span data-ttu-id="de50b-1983">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1983">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="de50b-1984">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1984">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1985">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1985">Return Value</span></span>

<span data-ttu-id="de50b-1986">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-1986">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="de50b-1987">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="de50b-1987">Method userWidth</span></span>

<span data-ttu-id="de50b-1988">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1988">Sets or returns the width of the control in pixels.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-1989">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-1989">Parameters</span></span>

<span data-ttu-id="de50b-1990">値</span><span class="sxs-lookup"><span data-stu-id="de50b-1990">value</span></span>  
<span data-ttu-id="de50b-1991">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1991">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-1992">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-1992">Return Value</span></span>

<span data-ttu-id="de50b-1993">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="de50b-1993">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-1994">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-1994">Remarks</span></span>

<span data-ttu-id="de50b-1995">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1995">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="de50b-1996">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="de50b-1996">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="de50b-1997">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="de50b-1997">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="de50b-1998">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="de50b-1998">Method verticalSpacing</span></span>

<span data-ttu-id="de50b-1999">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-1999">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-2000">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2000">Parameters</span></span>

<span data-ttu-id="de50b-2001">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2001">value</span></span>  
<span data-ttu-id="de50b-2002">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2002">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-2003">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-2003">mode</span></span>  
<span data-ttu-id="de50b-2004">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2004">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2005">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2005">Return Value</span></span>

<span data-ttu-id="de50b-2006">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="de50b-2006">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="de50b-2007">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="de50b-2007">Method verticalSpacingMode</span></span>

<span data-ttu-id="de50b-2008">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2008">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-2009">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2009">Parameters</span></span>

<span data-ttu-id="de50b-2010">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-2010">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2011">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2011">Return Value</span></span>

<span data-ttu-id="de50b-2012">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-2012">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="de50b-2013">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="de50b-2013">Method verticalSpacingValue</span></span>

<span data-ttu-id="de50b-2014">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2014">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2015">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2015">Parameters</span></span>

<span data-ttu-id="de50b-2016">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2016">value</span></span>  
<span data-ttu-id="de50b-2017">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2017">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2018">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2018">Return Value</span></span>

<span data-ttu-id="de50b-2019">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="de50b-2019">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="de50b-2020">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="de50b-2020">Method visible</span></span>

<span data-ttu-id="de50b-2021">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2021">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2022">Parameters</span></span>

<span data-ttu-id="de50b-2023">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2023">value</span></span>  
<span data-ttu-id="de50b-2024">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2024">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2025">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2025">Return Value</span></span>

<span data-ttu-id="de50b-2026">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2026">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="de50b-2027">メソッド width</span><span class="sxs-lookup"><span data-stu-id="de50b-2027">Method width</span></span>

<span data-ttu-id="de50b-2028">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2028">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-2029">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2029">Parameters</span></span>

<span data-ttu-id="de50b-2030">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2030">value</span></span>  
<span data-ttu-id="de50b-2031">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2031">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-2032">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-2032">mode</span></span>  
<span data-ttu-id="de50b-2033">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2033">An Integer that indicates how the width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2034">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2034">Return Value</span></span>

<span data-ttu-id="de50b-2035">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-2035">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2036">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2036">Remarks</span></span>

<span data-ttu-id="de50b-2037">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2037">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="de50b-2038">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-2038">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="de50b-2039">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-2039">Mode.</span></span>           | <span data-ttu-id="de50b-2040">幅計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-2040">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-2041">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-2041">-1 Exact.</span></span>       | <span data-ttu-id="de50b-2042">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2042">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-2043">0 自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-2043">0 Auto.</span></span>         | <span data-ttu-id="de50b-2044">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2044">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-2045">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-2045">1 Column width.</span></span> | <span data-ttu-id="de50b-2046">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-2046">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="de50b-2047">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2047">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="de50b-2048">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="de50b-2048">Method widthMode</span></span>

<span data-ttu-id="de50b-2049">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2049">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2050">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2050">Parameters</span></span>

<span data-ttu-id="de50b-2051">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2051">value</span></span>  
<span data-ttu-id="de50b-2052">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2052">An integer value that indicates how control width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2053">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2053">Return Value</span></span>

<span data-ttu-id="de50b-2054">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2054">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2055">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2055">Remarks</span></span>

<span data-ttu-id="de50b-2056">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-2056">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="de50b-2057">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-2057">Mode.</span></span>         | <span data-ttu-id="de50b-2058">幅計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-2058">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-2059">正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-2059">Exact.</span></span>        | <span data-ttu-id="de50b-2060">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2060">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-2061">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-2061">Auto.</span></span>         | <span data-ttu-id="de50b-2062">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2062">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-2063">列の幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-2063">Column width.</span></span> | <span data-ttu-id="de50b-2064">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-2064">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="de50b-2065">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="de50b-2065">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="de50b-2066">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="de50b-2066">Method widthValue</span></span>

<span data-ttu-id="de50b-2067">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2067">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2068">Parameters</span></span>

<span data-ttu-id="de50b-2069">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2069">value</span></span>  
<span data-ttu-id="de50b-2070">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2070">An Integer that specifies the width in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2071">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2071">Return Value</span></span>

<span data-ttu-id="de50b-2072">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-2072">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2073">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2073">Remarks</span></span>

<span data-ttu-id="de50b-2074">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2074">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-onenter"></a><span data-ttu-id="de50b-2075">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="de50b-2075">Method OnEnter</span></span>

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-2076">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2076">Parameters</span></span>

<span data-ttu-id="de50b-2077">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-2077">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-2078">e</span><span class="sxs-lookup"><span data-stu-id="de50b-2078">e</span></span>  

### <a name="method-lostfocus"></a><span data-ttu-id="de50b-2079">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-2079">Method lostFocus</span></span>

<span data-ttu-id="de50b-2080">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2080">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-drop"></a><span data-ttu-id="de50b-2081">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="de50b-2081">Method drop</span></span>

<span data-ttu-id="de50b-2082">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2082">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-2083">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2083">Parameters</span></span>

<span data-ttu-id="de50b-2084">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-2084">dragSource</span></span>  
<span data-ttu-id="de50b-2085">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2085">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2086">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-2086">dragMode</span></span>  
<span data-ttu-id="de50b-2087">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2087">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2088">x</span><span class="sxs-lookup"><span data-stu-id="de50b-2088">x</span></span>  
<span data-ttu-id="de50b-2089">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2089">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2090">y</span><span class="sxs-lookup"><span data-stu-id="de50b-2090">y</span></span>  
<span data-ttu-id="de50b-2091">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2091">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-paste"></a><span data-ttu-id="de50b-2092">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="de50b-2092">Method paste</span></span>

<span data-ttu-id="de50b-2093">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2093">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-setfocus"></a><span data-ttu-id="de50b-2094">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-2094">Method setFocus</span></span>

<span data-ttu-id="de50b-2095">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2095">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-onleaving"></a><span data-ttu-id="de50b-2096">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="de50b-2096">Method OnLeaving</span></span>

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-2097">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2097">Parameters</span></span>

<span data-ttu-id="de50b-2098">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-2098">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-2099">e</span><span class="sxs-lookup"><span data-stu-id="de50b-2099">e</span></span>  

### <a name="method-mouseleave"></a><span data-ttu-id="de50b-2100">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="de50b-2100">Method mouseLeave</span></span>

<span data-ttu-id="de50b-2101">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2101">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-gotfocus"></a><span data-ttu-id="de50b-2102">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-2102">Method gotFocus</span></span>

<span data-ttu-id="de50b-2103">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2103">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-dragleave"></a><span data-ttu-id="de50b-2104">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="de50b-2104">Method dragLeave</span></span>

<span data-ttu-id="de50b-2105">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2105">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-enter"></a><span data-ttu-id="de50b-2106">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="de50b-2106">Method enter</span></span>

    public void enter()

### <a name="method-dropex"></a><span data-ttu-id="de50b-2107">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="de50b-2107">Method dropEx</span></span>

<span data-ttu-id="de50b-2108">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2108">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-2109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2109">Parameters</span></span>

<span data-ttu-id="de50b-2110">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-2110">dragSource</span></span>  
<span data-ttu-id="de50b-2111">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2111">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2112">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-2112">dragMode</span></span>  
<span data-ttu-id="de50b-2113">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2113">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2114">x</span><span class="sxs-lookup"><span data-stu-id="de50b-2114">x</span></span>  
<span data-ttu-id="de50b-2115">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2115">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2116">y</span><span class="sxs-lookup"><span data-stu-id="de50b-2116">y</span></span>  
<span data-ttu-id="de50b-2117">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2117">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-mouseenter"></a><span data-ttu-id="de50b-2118">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="de50b-2118">Method mouseEnter</span></span>

<span data-ttu-id="de50b-2119">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2119">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-2120">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2120">Parameters</span></span>

<span data-ttu-id="de50b-2121">x</span><span class="sxs-lookup"><span data-stu-id="de50b-2121">x</span></span>  
<span data-ttu-id="de50b-2122">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2122">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-2123">y</span><span class="sxs-lookup"><span data-stu-id="de50b-2123">y</span></span>  
<span data-ttu-id="de50b-2124">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2124">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-2125">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-2125">button</span></span>  
<span data-ttu-id="de50b-2126">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2126">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-2127">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-2127">Ctrl</span></span>  
<span data-ttu-id="de50b-2128">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2128">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-2129">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-2129">Shift</span></span>  
<span data-ttu-id="de50b-2130">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2130">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-jumpref"></a><span data-ttu-id="de50b-2131">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="de50b-2131">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-onlostfocus"></a><span data-ttu-id="de50b-2132">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-2132">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-2133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2133">Parameters</span></span>

<span data-ttu-id="de50b-2134">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-2134">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-2135">e</span><span class="sxs-lookup"><span data-stu-id="de50b-2135">e</span></span>  

### <a name="method-ongotfocus"></a><span data-ttu-id="de50b-2136">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-2136">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-2137">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2137">Parameters</span></span>

<span data-ttu-id="de50b-2138">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-2138">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-2139">e</span><span class="sxs-lookup"><span data-stu-id="de50b-2139">e</span></span>  

### <a name="method-prefcolumnsize"></a><span data-ttu-id="de50b-2140">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="de50b-2140">Method prefColumnSize</span></span>

<span data-ttu-id="de50b-2141">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2141">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="de50b-2142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2142">Parameters</span></span>

<span data-ttu-id="de50b-2143">width</span><span class="sxs-lookup"><span data-stu-id="de50b-2143">width</span></span>  
<span data-ttu-id="de50b-2144">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="de50b-2144">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="de50b-2145">height</span><span class="sxs-lookup"><span data-stu-id="de50b-2145">height</span></span>  
<span data-ttu-id="de50b-2146">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="de50b-2146">The preferred height of the control.</span></span>

### <a name="method-cut"></a><span data-ttu-id="de50b-2147">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="de50b-2147">Method cut</span></span>

<span data-ttu-id="de50b-2148">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="de50b-2148">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-registeroverridemethod"></a><span data-ttu-id="de50b-2149">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="de50b-2149">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="de50b-2150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2150">Parameters</span></span>

<span data-ttu-id="de50b-2151">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="de50b-2151">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="de50b-2152">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="de50b-2152">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="de50b-2153">overrideObject</span><span class="sxs-lookup"><span data-stu-id="de50b-2153">overrideObject</span></span>  

### <a name="method-displaycontrol"></a><span data-ttu-id="de50b-2154">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="de50b-2154">Method displayControl</span></span>

<span data-ttu-id="de50b-2155">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2155">Displays the control.</span></span>

    public void displayControl()

### <a name="method-copy"></a><span data-ttu-id="de50b-2156">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="de50b-2156">Method copy</span></span>

<span data-ttu-id="de50b-2157">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="de50b-2157">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-context"></a><span data-ttu-id="de50b-2158">メソッド context</span><span class="sxs-lookup"><span data-stu-id="de50b-2158">Method context</span></span>

<span data-ttu-id="de50b-2159">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2159">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-resetusersetting"></a><span data-ttu-id="de50b-2160">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="de50b-2160">Method resetUserSetting</span></span>

<span data-ttu-id="de50b-2161">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="de50b-2161">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-inputsearch"></a><span data-ttu-id="de50b-2162">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="de50b-2162">Method inputSearch</span></span>

<span data-ttu-id="de50b-2163">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2163">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="de50b-2164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2164">Parameters</span></span>

<span data-ttu-id="de50b-2165">searchStr</span><span class="sxs-lookup"><span data-stu-id="de50b-2165">searchStr</span></span>  
<span data-ttu-id="de50b-2166">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2166">The string value to use to filter data; optional.</span></span>

### <a name="method-filter"></a><span data-ttu-id="de50b-2167">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="de50b-2167">Method filter</span></span>

    public void filter([str filterStr])

#### <a name="parameters"></a><span data-ttu-id="de50b-2168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2168">Parameters</span></span>

<span data-ttu-id="de50b-2169">filterStr</span><span class="sxs-lookup"><span data-stu-id="de50b-2169">filterStr</span></span>  

### <a name="method-enddrag"></a><span data-ttu-id="de50b-2170">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="de50b-2170">Method endDrag</span></span>

<span data-ttu-id="de50b-2171">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2171">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="de50b-2172">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2172">Remarks</span></span>

<span data-ttu-id="de50b-2173">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2173">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="de50b-2174">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2174">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="class-formfunctionbuttoncontrol"></a><span data-ttu-id="de50b-2175">クラス FormFunctionButtonControl</span><span class="sxs-lookup"><span data-stu-id="de50b-2175">Class FormFunctionButtonControl</span></span>
    class FormFunctionButtonControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="de50b-2176">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2176">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="de50b-2177">例</span><span class="sxs-lookup"><span data-stu-id="de50b-2177">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="de50b-2178">メソッド</span><span class="sxs-lookup"><span data-stu-id="de50b-2178">Methods</span></span>

| <span data-ttu-id="de50b-2179">方法</span><span class="sxs-lookup"><span data-stu-id="de50b-2179">Method</span></span>                                                                                                      | <span data-ttu-id="de50b-2180">説明</span><span class="sxs-lookup"><span data-stu-id="de50b-2180">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-2181">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2181">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="de50b-2182">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2182">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-2183">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2183">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2184">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2184">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="de50b-2185">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2185">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-2186">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="de50b-2186">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="de50b-2187">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2187">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="de50b-2188">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2188">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="de50b-2189">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2189">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="de50b-2190">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2190">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2191">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2191">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="de50b-2192">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2192">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="de50b-2193">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2193">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-2194">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2194">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-2195">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-2195">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="de50b-2196">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2196">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-2197">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2197">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2198">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2198">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="de50b-2199">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2199">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-2200">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2200">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="de50b-2201">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2201">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="de50b-2202">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2202">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="de50b-2203">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2203">Gets or sets the appearance of the button control.</span></span>                                                                                                                      |
| <span data-ttu-id="de50b-2204">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="de50b-2204">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="de50b-2205">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2205">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="de50b-2206">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2206">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="de50b-2207">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2207">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-2208">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2208">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="de50b-2209">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2209">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-2210">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2210">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="de50b-2211">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2211">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-2212">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2212">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="de50b-2213">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2213">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-2214">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="de50b-2214">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="de50b-2215">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2215">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="de50b-2216">public int copyCallerQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2216">public int copyCallerQuery(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2217">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2217">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="de50b-2218">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2218">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="de50b-2219">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2219">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2220">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2220">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="de50b-2221">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2221">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="de50b-2222">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2222">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="de50b-2223">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2223">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-2224">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2224">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="de50b-2225">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2225">Determines whether the button should be the default button in the form.</span></span>                                                                                                 |
| <span data-ttu-id="de50b-2226">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2226">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="de50b-2227">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2227">Gets or sets the disabled image of the button.</span></span>                                                                                                                          |
| <span data-ttu-id="de50b-2228">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2228">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2229">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2229">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="de50b-2230">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2230">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                                                          |
| <span data-ttu-id="de50b-2231">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2231">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="de50b-2232">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2232">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, Finance and Operations, or in both.</span></span> |
| <span data-ttu-id="de50b-2233">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2233">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-2234">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2234">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="de50b-2235">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-2235">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="de50b-2236">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2236">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="de50b-2237">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-2237">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="de50b-2238">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2238">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="de50b-2239">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="de50b-2239">public str dragText()</span></span>                                                                                       | <span data-ttu-id="de50b-2240">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2240">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-2241">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2241">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="de50b-2242">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2242">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-2243">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2243">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="de50b-2244">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2244">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="de50b-2245">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2245">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-2246">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2246">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="de50b-2247">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2247">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2248">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2248">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="de50b-2249">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2249">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-2250">public int formViewOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2250">public int formViewOption(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2251">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2251">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="de50b-2252">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2252">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="de50b-2253">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="de50b-2253">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="de50b-2254">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2254">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="de50b-2255">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2255">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="de50b-2256">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2256">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-2257">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2257">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-2258">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2258">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-2259">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2259">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="de50b-2260">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2260">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-2261">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="de50b-2261">public str helpField()</span></span>                                                                                      | <span data-ttu-id="de50b-2262">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2262">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-2263">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2263">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="de50b-2264">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2264">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="de50b-2265">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2265">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="de50b-2266">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2266">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="de50b-2267">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="de50b-2267">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="de50b-2268">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2268">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-2269">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2269">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2270">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="de50b-2270">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2271">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="de50b-2271">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="de50b-2272">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2272">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="de50b-2273">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="de50b-2273">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="de50b-2274">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2274">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-2275">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="de50b-2275">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="de50b-2276">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2276">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="de50b-2277">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2277">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2278">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2278">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2279">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2279">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="de50b-2280">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2280">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="de50b-2281">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2281">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-2282">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2282">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-2283">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2283">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-2284">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2284">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="de50b-2285">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2285">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="de50b-2286">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="de50b-2286">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="de50b-2287">public xMenuFunction menufunction()</span><span class="sxs-lookup"><span data-stu-id="de50b-2287">public xMenuFunction menufunction()</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2288">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2288">public str menuItemName(\[str value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2289">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2289">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2290">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-2290">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="de50b-2291">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2291">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="de50b-2292">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-2292">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="de50b-2293">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2293">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-2294">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-2294">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="de50b-2295">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2295">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-2296">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-2296">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="de50b-2297">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2297">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="de50b-2298">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2298">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2299">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2299">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="de50b-2300">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2300">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="de50b-2301">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2301">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2302">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2302">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2303">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2303">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2304">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2304">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2305">public int openMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2305">public int openMode(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2306">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="de50b-2306">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2307">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2307">public str parameters(\[str value\])</span></span>                                                                        | <span data-ttu-id="de50b-2308">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2308">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                                                  |
| <span data-ttu-id="de50b-2309">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="de50b-2309">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="de50b-2310">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2310">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-2311">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2311">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2312">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2312">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2313">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2313">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="de50b-2314">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2314">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-2315">public boolean sendExternalContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2315">public boolean sendExternalContext(\[boolean value\])</span></span>                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2316">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2316">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2317">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="de50b-2317">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="de50b-2318">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2318">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-2319">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2319">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2320">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2320">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="de50b-2321">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2321">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="de50b-2322">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2322">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2323">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2323">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2324">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2324">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2325">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="de50b-2325">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="de50b-2326">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2326">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-2327">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2327">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="de50b-2328">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2328">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-2329">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2329">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="de50b-2330">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2330">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-2331">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2331">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-2332">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2332">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-2333">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2333">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2334">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2334">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2335">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="de50b-2335">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2336">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2336">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-2337">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2337">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-2338">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2338">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="de50b-2339">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2339">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="de50b-2340">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2340">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="de50b-2341">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2341">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-2342">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2342">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="de50b-2343">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2343">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="de50b-2344">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2344">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-2345">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2345">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="de50b-2346">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2346">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-2347">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2347">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="de50b-2348">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2348">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="de50b-2349">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2349">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="de50b-2350">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2350">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="de50b-2351">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2351">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-2352">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2352">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="de50b-2353">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2353">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="de50b-2354">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2354">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="de50b-2355">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2355">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="de50b-2356">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2356">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-2357">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2357">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="de50b-2358">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2358">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-2359">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2359">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-2360">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2360">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2361">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2361">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="de50b-2362">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2362">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-2363">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2363">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="de50b-2364">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2364">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-2365">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2365">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="de50b-2366">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2366">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-2367">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2367">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="de50b-2368">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2368">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-2369">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2369">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="de50b-2370">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2370">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="de50b-2371">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2371">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-2372">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2372">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-2373">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2373">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="de50b-2374">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2374">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="de50b-2375">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="de50b-2375">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="de50b-2376">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2376">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="de50b-2377">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-2377">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="de50b-2378">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2378">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="de50b-2379">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="de50b-2379">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="de50b-2380">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="de50b-2380">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="de50b-2381">public void context()</span><span class="sxs-lookup"><span data-stu-id="de50b-2381">public void context()</span></span>                                                                                       | <span data-ttu-id="de50b-2382">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2382">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-2383">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-2383">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="de50b-2384">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2384">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="de50b-2385">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2385">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2386">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-2386">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="de50b-2387">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2387">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="de50b-2388">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-2388">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="de50b-2389">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2389">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-2390">public void paste()</span><span class="sxs-lookup"><span data-stu-id="de50b-2390">public void paste()</span></span>                                                                                         | <span data-ttu-id="de50b-2391">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2391">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-2392">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2392">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2393">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="de50b-2393">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="de50b-2394">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2394">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-2395">public void cut()</span><span class="sxs-lookup"><span data-stu-id="de50b-2395">public void cut()</span></span>                                                                                           | <span data-ttu-id="de50b-2396">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="de50b-2396">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="de50b-2397">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2397">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2398">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="de50b-2398">public void displayControl()</span></span>                                                                                | <span data-ttu-id="de50b-2399">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2399">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="de50b-2400">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="de50b-2400">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="de50b-2401">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2401">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="de50b-2402">public void copy()</span><span class="sxs-lookup"><span data-stu-id="de50b-2402">public void copy()</span></span>                                                                                          | <span data-ttu-id="de50b-2403">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="de50b-2403">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="de50b-2404">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="de50b-2404">public void clicked()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2405">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2405">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2406">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-2406">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="de50b-2407">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2407">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="de50b-2408">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="de50b-2408">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="de50b-2409">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2409">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-2410">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-2410">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="de50b-2411">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2411">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="de50b-2412">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="de50b-2412">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="de50b-2413">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2413">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="de50b-2414">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="de50b-2414">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-2415">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="de50b-2415">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |

### <a name="method-aligncontrol"></a><span data-ttu-id="de50b-2416">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="de50b-2416">Method alignControl</span></span>

<span data-ttu-id="de50b-2417">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2417">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2418">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2418">Parameters</span></span>

<span data-ttu-id="de50b-2419">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2419">value</span></span>  
<span data-ttu-id="de50b-2420">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2420">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2421">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2421">Return Value</span></span>

<span data-ttu-id="de50b-2422">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2422">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2423">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2423">Remarks</span></span>

<span data-ttu-id="de50b-2424">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2424">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-alignment"></a><span data-ttu-id="de50b-2425">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="de50b-2425">Method alignment</span></span>

    public int alignment([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2426">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2426">Parameters</span></span>

<span data-ttu-id="de50b-2427">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2427">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2428">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2428">Return Value</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="de50b-2429">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="de50b-2429">Method allowEdit</span></span>

<span data-ttu-id="de50b-2430">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2430">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2431">Parameters</span></span>

<span data-ttu-id="de50b-2432">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2432">value</span></span>  
<span data-ttu-id="de50b-2433">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2433">The value to assign to the allowEdit property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2434">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2434">Return Value</span></span>

<span data-ttu-id="de50b-2435">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2435">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2436">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2436">Remarks</span></span>

<span data-ttu-id="de50b-2437">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="de50b-2437">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="de50b-2438">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="de50b-2438">Method allowSysSetup</span></span>

<span data-ttu-id="de50b-2439">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2439">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="de50b-2440">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2440">Return Value</span></span>

<span data-ttu-id="de50b-2441">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2441">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="de50b-2442">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="de50b-2442">Method autoDeclaration</span></span>

<span data-ttu-id="de50b-2443">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2443">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2444">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2444">Parameters</span></span>

<span data-ttu-id="de50b-2445">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2445">value</span></span>  
<span data-ttu-id="de50b-2446">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2446">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2447">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2447">Return Value</span></span>

<span data-ttu-id="de50b-2448">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2448">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2449">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2449">Remarks</span></span>

<span data-ttu-id="de50b-2450">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2450">Controls cannot have identical names.</span></span>

### <a name="method-autorefreshdata"></a><span data-ttu-id="de50b-2451">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="de50b-2451">Method autoRefreshData</span></span>

    public boolean autoRefreshData([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2452">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2452">Parameters</span></span>

<span data-ttu-id="de50b-2453">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2453">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2454">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2454">Return Value</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="de50b-2455">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="de50b-2455">Method backgroundColor</span></span>

<span data-ttu-id="de50b-2456">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2456">Gets or sets the background color of the control.</span></span>

    public int backgroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2457">Parameters</span></span>

<span data-ttu-id="de50b-2458">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2458">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2459">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2459">Return Value</span></span>

<span data-ttu-id="de50b-2460">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-2460">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2461">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2461">Remarks</span></span>

<span data-ttu-id="de50b-2462">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2462">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="de50b-2463">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2463">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="de50b-2464">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2464">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="de50b-2465">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2465">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="de50b-2466">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2466">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="de50b-2467">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2467">The maximum value for a single byte is 255.</span></span>

### <a name="method-backstyle"></a><span data-ttu-id="de50b-2468">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="de50b-2468">Method backStyle</span></span>

<span data-ttu-id="de50b-2469">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2469">Determines whether the control background can be transparent.</span></span>

    public int backStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2470">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2470">Parameters</span></span>

<span data-ttu-id="de50b-2471">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2471">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2472">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2472">Return Value</span></span>

<span data-ttu-id="de50b-2473">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2473">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="de50b-2474">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="de50b-2474">Method beginDrag</span></span>

<span data-ttu-id="de50b-2475">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2475">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-2476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2476">Parameters</span></span>

<span data-ttu-id="de50b-2477">x</span><span class="sxs-lookup"><span data-stu-id="de50b-2477">x</span></span>  
<span data-ttu-id="de50b-2478">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2478">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="de50b-2479">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2479">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="de50b-2480">y</span><span class="sxs-lookup"><span data-stu-id="de50b-2480">y</span></span>  
<span data-ttu-id="de50b-2481">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2481">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="de50b-2482">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2482">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2483">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2483">Return Value</span></span>

<span data-ttu-id="de50b-2484">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2484">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2485">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2485">Remarks</span></span>

<span data-ttu-id="de50b-2486">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2486">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="de50b-2487">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2487">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-big"></a><span data-ttu-id="de50b-2488">メソッド big</span><span class="sxs-lookup"><span data-stu-id="de50b-2488">Method big</span></span>

    public boolean big([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2489">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2489">Parameters</span></span>

<span data-ttu-id="de50b-2490">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2490">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2491">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2491">Return Value</span></span>

### <a name="method-bold"></a><span data-ttu-id="de50b-2492">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="de50b-2492">Method bold</span></span>

<span data-ttu-id="de50b-2493">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2493">Gets or sets the weight of font used to output text in the control.</span></span>

    public int bold([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2494">Parameters</span></span>

<span data-ttu-id="de50b-2495">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2495">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2496">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2496">Return Value</span></span>

<span data-ttu-id="de50b-2497">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2497">An integer value between zero and nine, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2498">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2498">Remarks</span></span>

<span data-ttu-id="de50b-2499">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2499">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="de50b-2500">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2500">0 Use the default font weight.</span></span>
-   <span data-ttu-id="de50b-2501">1 シン。</span><span class="sxs-lookup"><span data-stu-id="de50b-2501">1 Thin.</span></span>
-   <span data-ttu-id="de50b-2502">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="de50b-2502">2 Extra-light.</span></span>
-   <span data-ttu-id="de50b-2503">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="de50b-2503">3 Light.</span></span>
-   <span data-ttu-id="de50b-2504">4 標準。</span><span class="sxs-lookup"><span data-stu-id="de50b-2504">4 Normal.</span></span>
-   <span data-ttu-id="de50b-2505">5 中。</span><span class="sxs-lookup"><span data-stu-id="de50b-2505">5 Medium.</span></span>
-   <span data-ttu-id="de50b-2506">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="de50b-2506">6 Semibold.</span></span>
-   <span data-ttu-id="de50b-2507">7 太字。</span><span class="sxs-lookup"><span data-stu-id="de50b-2507">7 Bold.</span></span>
-   <span data-ttu-id="de50b-2508">8 極太。</span><span class="sxs-lookup"><span data-stu-id="de50b-2508">8 Extra-bold.</span></span>
-   <span data-ttu-id="de50b-2509">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="de50b-2509">9 Heavy.</span></span>

### <a name="method-border"></a><span data-ttu-id="de50b-2510">メソッド border</span><span class="sxs-lookup"><span data-stu-id="de50b-2510">Method border</span></span>

<span data-ttu-id="de50b-2511">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2511">Gets or sets the style of the borderline of the control.</span></span>

    public int border([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2512">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2512">Parameters</span></span>

<span data-ttu-id="de50b-2513">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2513">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2514">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2514">Return Value</span></span>

<span data-ttu-id="de50b-2515">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-2515">An integer between zero and four, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2516">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2516">Remarks</span></span>

<span data-ttu-id="de50b-2517">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2517">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="de50b-2518">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2518">Value.</span></span> | <span data-ttu-id="de50b-2519">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-2519">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="de50b-2520">0</span><span class="sxs-lookup"><span data-stu-id="de50b-2520">0</span></span>      | <span data-ttu-id="de50b-2521">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-2521">Auto.</span></span>        |
| <span data-ttu-id="de50b-2522">1</span><span class="sxs-lookup"><span data-stu-id="de50b-2522">1</span></span>      | <span data-ttu-id="de50b-2523">3D。</span><span class="sxs-lookup"><span data-stu-id="de50b-2523">3D.</span></span>          |
| <span data-ttu-id="de50b-2524">2</span><span class="sxs-lookup"><span data-stu-id="de50b-2524">2</span></span>      | <span data-ttu-id="de50b-2525">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="de50b-2525">Single line.</span></span> |
| <span data-ttu-id="de50b-2526">3</span><span class="sxs-lookup"><span data-stu-id="de50b-2526">3</span></span>      | <span data-ttu-id="de50b-2527">均一。</span><span class="sxs-lookup"><span data-stu-id="de50b-2527">Flat.</span></span>        |
| <span data-ttu-id="de50b-2528">4</span><span class="sxs-lookup"><span data-stu-id="de50b-2528">4</span></span>      | <span data-ttu-id="de50b-2529">なし。</span><span class="sxs-lookup"><span data-stu-id="de50b-2529">None.</span></span>        |

### <a name="method-buttondisplay"></a><span data-ttu-id="de50b-2530">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="de50b-2530">Method buttonDisplay</span></span>

<span data-ttu-id="de50b-2531">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2531">Gets or sets the appearance of the button control.</span></span>

    public int buttonDisplay([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2532">Parameters</span></span>

<span data-ttu-id="de50b-2533">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2533">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2534">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2534">Return Value</span></span>

<span data-ttu-id="de50b-2535">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-2535">An integer between zero and five, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2536">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2536">Remarks</span></span>

<span data-ttu-id="de50b-2537">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2537">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="de50b-2538">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2538">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="de50b-2539">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2539">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="de50b-2540">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2540">Value.</span></span> | <span data-ttu-id="de50b-2541">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-2541">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="de50b-2542">0</span><span class="sxs-lookup"><span data-stu-id="de50b-2542">0</span></span>      | <span data-ttu-id="de50b-2543">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="de50b-2543">Text only.</span></span>                                                       |
| <span data-ttu-id="de50b-2544">1</span><span class="sxs-lookup"><span data-stu-id="de50b-2544">1</span></span>      | <span data-ttu-id="de50b-2545">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="de50b-2545">Image Only.</span></span>                                                      |
| <span data-ttu-id="de50b-2546">2</span><span class="sxs-lookup"><span data-stu-id="de50b-2546">2</span></span>      | <span data-ttu-id="de50b-2547">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2547">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="de50b-2548">3</span><span class="sxs-lookup"><span data-stu-id="de50b-2548">3</span></span>      | <span data-ttu-id="de50b-2549">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2549">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="de50b-2550">4</span><span class="sxs-lookup"><span data-stu-id="de50b-2550">4</span></span>      | <span data-ttu-id="de50b-2551">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2551">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="de50b-2552">5</span><span class="sxs-lookup"><span data-stu-id="de50b-2552">5</span></span>      | <span data-ttu-id="de50b-2553">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2553">Text and image; the image is displayed to the right of the text.</span></span> |

### <a name="method-calccontrolsize"></a><span data-ttu-id="de50b-2554">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="de50b-2554">Method calcControlSize</span></span>

<span data-ttu-id="de50b-2555">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2555">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="de50b-2556">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2556">Parameters</span></span>

<span data-ttu-id="de50b-2557">chars</span><span class="sxs-lookup"><span data-stu-id="de50b-2557">chars</span></span>  
<span data-ttu-id="de50b-2558">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="de50b-2558">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="de50b-2559">明細行</span><span class="sxs-lookup"><span data-stu-id="de50b-2559">lines</span></span>  
<span data-ttu-id="de50b-2560">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="de50b-2560">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2561">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2561">Return Value</span></span>

<span data-ttu-id="de50b-2562">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="de50b-2562">The container that holds the width and height.</span></span>

### <a name="method-caption"></a><span data-ttu-id="de50b-2563">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="de50b-2563">Method caption</span></span>

<span data-ttu-id="de50b-2564">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2564">Gets or set the caption of the control.</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2565">Parameters</span></span>

<span data-ttu-id="de50b-2566">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2566">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2567">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2567">Return Value</span></span>

<span data-ttu-id="de50b-2568">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-2568">The string that is used as the caption of the control.</span></span>

### <a name="method-characterset"></a><span data-ttu-id="de50b-2569">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="de50b-2569">Method characterSet</span></span>

<span data-ttu-id="de50b-2570">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2570">Gets or sets the character set of the font.</span></span>

    public int characterSet([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2571">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2571">Parameters</span></span>

<span data-ttu-id="de50b-2572">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2572">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2573">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2573">Return Value</span></span>

<span data-ttu-id="de50b-2574">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2574">An integer value that indicates the character set of the font.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2575">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2575">Remarks</span></span>

<span data-ttu-id="de50b-2576">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2576">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="de50b-2577">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2577">Value.</span></span> | <span data-ttu-id="de50b-2578">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-2578">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="de50b-2579">0</span><span class="sxs-lookup"><span data-stu-id="de50b-2579">0</span></span>      | <span data-ttu-id="de50b-2580">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2580">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="de50b-2581">1</span><span class="sxs-lookup"><span data-stu-id="de50b-2581">1</span></span>      | <span data-ttu-id="de50b-2582">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2582">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="de50b-2583">2</span><span class="sxs-lookup"><span data-stu-id="de50b-2583">2</span></span>      | <span data-ttu-id="de50b-2584">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2584">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="de50b-2585">77</span><span class="sxs-lookup"><span data-stu-id="de50b-2585">77</span></span>     | <span data-ttu-id="de50b-2586">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2586">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="de50b-2587">128</span><span class="sxs-lookup"><span data-stu-id="de50b-2587">128</span></span>    | <span data-ttu-id="de50b-2588">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2588">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="de50b-2589">129</span><span class="sxs-lookup"><span data-stu-id="de50b-2589">129</span></span>    | <span data-ttu-id="de50b-2590">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2590">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="de50b-2591">134</span><span class="sxs-lookup"><span data-stu-id="de50b-2591">134</span></span>    | <span data-ttu-id="de50b-2592">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2592">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="de50b-2593">136</span><span class="sxs-lookup"><span data-stu-id="de50b-2593">136</span></span>    | <span data-ttu-id="de50b-2594">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2594">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="de50b-2595">161</span><span class="sxs-lookup"><span data-stu-id="de50b-2595">161</span></span>    | <span data-ttu-id="de50b-2596">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2596">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="de50b-2597">162</span><span class="sxs-lookup"><span data-stu-id="de50b-2597">162</span></span>    | <span data-ttu-id="de50b-2598">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2598">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="de50b-2599">163</span><span class="sxs-lookup"><span data-stu-id="de50b-2599">163</span></span>    | <span data-ttu-id="de50b-2600">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2600">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="de50b-2601">186</span><span class="sxs-lookup"><span data-stu-id="de50b-2601">186</span></span>    | <span data-ttu-id="de50b-2602">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2602">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="de50b-2603">204</span><span class="sxs-lookup"><span data-stu-id="de50b-2603">204</span></span>    | <span data-ttu-id="de50b-2604">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2604">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="de50b-2605">238</span><span class="sxs-lookup"><span data-stu-id="de50b-2605">238</span></span>    | <span data-ttu-id="de50b-2606">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2606">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="de50b-2607">255</span><span class="sxs-lookup"><span data-stu-id="de50b-2607">255</span></span>    | <span data-ttu-id="de50b-2608">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2608">OEM\_CHARSET</span></span>         |

<span data-ttu-id="de50b-2609">次のテーブルの値は、韓国語版 msCoNameWindows の値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2609">The value in the following table is for the Korean language edition of msCoNameWindows.</span></span>

| <span data-ttu-id="de50b-2610">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2610">Value.</span></span> | <span data-ttu-id="de50b-2611">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-2611">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="de50b-2612">130</span><span class="sxs-lookup"><span data-stu-id="de50b-2612">130</span></span>    | <span data-ttu-id="de50b-2613">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2613">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="de50b-2614">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2614">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="de50b-2615">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2615">Value.</span></span> | <span data-ttu-id="de50b-2616">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-2616">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="de50b-2617">177</span><span class="sxs-lookup"><span data-stu-id="de50b-2617">177</span></span>    | <span data-ttu-id="de50b-2618">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2618">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="de50b-2619">178</span><span class="sxs-lookup"><span data-stu-id="de50b-2619">178</span></span>    | <span data-ttu-id="de50b-2620">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2620">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="de50b-2621">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2621">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="de50b-2622">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2622">Value.</span></span> | <span data-ttu-id="de50b-2623">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-2623">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="de50b-2624">222</span><span class="sxs-lookup"><span data-stu-id="de50b-2624">222</span></span>    | <span data-ttu-id="de50b-2625">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="de50b-2625">THAI\_CHARSET</span></span> |

<span data-ttu-id="de50b-2626">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2626">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="de50b-2627">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2627">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="de50b-2628">詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de50b-2628">For more information, see the LOGFONT structure on the MSDN website, http://go.microsoft.com/fwlink/?LinkID=85972.</span></span>

### <a name="method-colorscheme"></a><span data-ttu-id="de50b-2629">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="de50b-2629">Method colorScheme</span></span>

<span data-ttu-id="de50b-2630">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2630">Gets or sets the color scheme of the control.</span></span>

    public int colorScheme([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2631">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2631">Parameters</span></span>

<span data-ttu-id="de50b-2632">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2632">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2633">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2633">Return Value</span></span>

<span data-ttu-id="de50b-2634">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-2634">An integer between zero and two, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2635">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2635">Remarks</span></span>

<span data-ttu-id="de50b-2636">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2636">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="de50b-2637">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2637">Value.</span></span> | <span data-ttu-id="de50b-2638">スタイル。</span><span class="sxs-lookup"><span data-stu-id="de50b-2638">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="de50b-2639">0</span><span class="sxs-lookup"><span data-stu-id="de50b-2639">0</span></span>      | <span data-ttu-id="de50b-2640">既定。</span><span class="sxs-lookup"><span data-stu-id="de50b-2640">Default.</span></span>               |
| <span data-ttu-id="de50b-2641">1</span><span class="sxs-lookup"><span data-stu-id="de50b-2641">1</span></span>      | <span data-ttu-id="de50b-2642">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="de50b-2642">The Windows palette.</span></span>   |
| <span data-ttu-id="de50b-2643">2</span><span class="sxs-lookup"><span data-stu-id="de50b-2643">2</span></span>      | <span data-ttu-id="de50b-2644">真の配色。</span><span class="sxs-lookup"><span data-stu-id="de50b-2644">The true-color scheme.</span></span> |

### <a name="method-configurationkey"></a><span data-ttu-id="de50b-2645">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="de50b-2645">Method configurationKey</span></span>

<span data-ttu-id="de50b-2646">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2646">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2647">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2647">Parameters</span></span>

<span data-ttu-id="de50b-2648">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2648">value</span></span>  
<span data-ttu-id="de50b-2649">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2649">The ID of the configuration key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2650">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2650">Return Value</span></span>

<span data-ttu-id="de50b-2651">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-2651">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2652">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2652">Remarks</span></span>

<span data-ttu-id="de50b-2653">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2653">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="de50b-2654">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2654">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="de50b-2655">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="de50b-2655">Method configurationKeyEx</span></span>

<span data-ttu-id="de50b-2656">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2656">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="de50b-2657">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2657">Return Value</span></span>

<span data-ttu-id="de50b-2658">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="de50b-2658">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2659">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2659">Remarks</span></span>

<span data-ttu-id="de50b-2660">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2660">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="de50b-2661">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2661">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="de50b-2662">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2662">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-copycallerquery"></a><span data-ttu-id="de50b-2663">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="de50b-2663">Method copyCallerQuery</span></span>

    public int copyCallerQuery([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2664">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2664">Parameters</span></span>

<span data-ttu-id="de50b-2665">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2665">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2666">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2666">Return Value</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="de50b-2667">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="de50b-2667">Method countryRegionCodes</span></span>

<span data-ttu-id="de50b-2668">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2668">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2669">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2669">Parameters</span></span>

<span data-ttu-id="de50b-2670">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2670">value</span></span>  
<span data-ttu-id="de50b-2671">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2671">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2672">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2672">Return Value</span></span>

<span data-ttu-id="de50b-2673">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-2673">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-countryregioncontextfield"></a><span data-ttu-id="de50b-2674">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="de50b-2674">Method countryRegionContextField</span></span>

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2675">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2675">Parameters</span></span>

<span data-ttu-id="de50b-2676">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2676">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2677">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2677">Return Value</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="de50b-2678">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="de50b-2678">Method dataRelationPath</span></span>

<span data-ttu-id="de50b-2679">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2679">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2680">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2680">Parameters</span></span>

<span data-ttu-id="de50b-2681">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2681">value</span></span>  
<span data-ttu-id="de50b-2682">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2682">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2683">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2683">Return Value</span></span>

<span data-ttu-id="de50b-2684">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="de50b-2684">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2685">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2685">Remarks</span></span>

<span data-ttu-id="de50b-2686">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2686">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="de50b-2687">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="de50b-2687">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-datasource"></a><span data-ttu-id="de50b-2688">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="de50b-2688">Method dataSource</span></span>

<span data-ttu-id="de50b-2689">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2689">Gets or sets a data source to be used by the control or the form.</span></span>

    public int dataSource([AnyType value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2690">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2690">Parameters</span></span>

<span data-ttu-id="de50b-2691">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2691">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2692">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2692">Return Value</span></span>

<span data-ttu-id="de50b-2693">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-2693">The identifier of the data source to be used.</span></span>

### <a name="method-defaultbutton"></a><span data-ttu-id="de50b-2694">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="de50b-2694">Method defaultButton</span></span>

<span data-ttu-id="de50b-2695">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2695">Determines whether the button should be the default button in the form.</span></span>

    public boolean defaultButton([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2696">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2696">Parameters</span></span>

<span data-ttu-id="de50b-2697">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2697">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2698">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2698">Return Value</span></span>

<span data-ttu-id="de50b-2699">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2699">true if the button should be the default button; otherwise, false.</span></span>

### <a name="method-disabledimage"></a><span data-ttu-id="de50b-2700">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="de50b-2700">Method disabledImage</span></span>

<span data-ttu-id="de50b-2701">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2701">Gets or sets the disabled image of the button.</span></span>

    public str disabledImage([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2702">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2702">Parameters</span></span>

<span data-ttu-id="de50b-2703">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2703">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2704">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2704">Return Value</span></span>

<span data-ttu-id="de50b-2705">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="de50b-2705">The full name of an image file.</span></span> <span data-ttu-id="de50b-2706">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2706">The system supports all of the GDI-supported image formats.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2707">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2707">Remarks</span></span>

<span data-ttu-id="de50b-2708">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2708">This property has precedence over the disabledResource property.</span></span> <span data-ttu-id="de50b-2709">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2709">It is used if both of these properties are set.</span></span>

### <a name="method-disabledimagelocation"></a><span data-ttu-id="de50b-2710">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="de50b-2710">Method disabledImageLocation</span></span>

    public int disabledImageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2711">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2711">Parameters</span></span>

<span data-ttu-id="de50b-2712">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2712">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2713">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2713">Return Value</span></span>

### <a name="method-disabledresource"></a><span data-ttu-id="de50b-2714">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="de50b-2714">Method disabledResource</span></span>

<span data-ttu-id="de50b-2715">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2715">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

    public int disabledResource([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2716">Parameters</span></span>

<span data-ttu-id="de50b-2717">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2717">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2718">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2718">Return Value</span></span>

<span data-ttu-id="de50b-2719">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-2719">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="de50b-2720">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2720">Both icon and bitmap images are supported.</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="de50b-2721">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="de50b-2721">Method displayTarget</span></span>

<span data-ttu-id="de50b-2722">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2722">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2723">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2723">Parameters</span></span>

<span data-ttu-id="de50b-2724">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2724">value</span></span>  
<span data-ttu-id="de50b-2725">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2725">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2726">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2726">Return Value</span></span>

<span data-ttu-id="de50b-2727">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2727">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="de50b-2728">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="de50b-2728">Method dragDrop</span></span>

<span data-ttu-id="de50b-2729">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2729">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2730">Parameters</span></span>

<span data-ttu-id="de50b-2731">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2731">value</span></span>  
<span data-ttu-id="de50b-2732">ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2732">An Integer data type that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2733">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2733">Return Value</span></span>

<span data-ttu-id="de50b-2734">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2734">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2735">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2735">Remarks</span></span>

<span data-ttu-id="de50b-2736">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2736">Use the dragLeave , the dragOver, and the dragOverEx to specify the behavior.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="de50b-2737">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="de50b-2737">Method dragOver</span></span>

<span data-ttu-id="de50b-2738">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2738">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-2739">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2739">Parameters</span></span>

<span data-ttu-id="de50b-2740">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-2740">dragSource</span></span>  
<span data-ttu-id="de50b-2741">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2741">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2742">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-2742">dragMode</span></span>  
<span data-ttu-id="de50b-2743">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2743">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2744">x</span><span class="sxs-lookup"><span data-stu-id="de50b-2744">x</span></span>  
<span data-ttu-id="de50b-2745">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2745">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2746">y</span><span class="sxs-lookup"><span data-stu-id="de50b-2746">y</span></span>  
<span data-ttu-id="de50b-2747">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2747">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2748">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2748">Return Value</span></span>

<span data-ttu-id="de50b-2749">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2749">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="de50b-2750">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="de50b-2750">Method dragOverEx</span></span>

<span data-ttu-id="de50b-2751">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2751">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-2752">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2752">Parameters</span></span>

<span data-ttu-id="de50b-2753">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-2753">dragSource</span></span>  
<span data-ttu-id="de50b-2754">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2754">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2755">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-2755">dragMode</span></span>  
<span data-ttu-id="de50b-2756">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2756">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2757">x</span><span class="sxs-lookup"><span data-stu-id="de50b-2757">x</span></span>  
<span data-ttu-id="de50b-2758">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2758">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-2759">y</span><span class="sxs-lookup"><span data-stu-id="de50b-2759">y</span></span>  
<span data-ttu-id="de50b-2760">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2760">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2761">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2761">Return Value</span></span>

<span data-ttu-id="de50b-2762">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2762">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="de50b-2763">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="de50b-2763">Method dragText</span></span>

<span data-ttu-id="de50b-2764">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2764">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="de50b-2765">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2765">Return Value</span></span>

<span data-ttu-id="de50b-2766">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-2766">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="de50b-2767">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="de50b-2767">Method enabled</span></span>

<span data-ttu-id="de50b-2768">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2768">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2769">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2769">Parameters</span></span>

<span data-ttu-id="de50b-2770">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2770">value</span></span>  
<span data-ttu-id="de50b-2771">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2771">A Boolean value that specifies whether the control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2772">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2772">Return Value</span></span>

<span data-ttu-id="de50b-2773">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2773">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2774">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2774">Remarks</span></span>

<span data-ttu-id="de50b-2775">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2775">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="de50b-2776">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2776">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="de50b-2777">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2777">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-font"></a><span data-ttu-id="de50b-2778">メソッド font</span><span class="sxs-lookup"><span data-stu-id="de50b-2778">Method font</span></span>

<span data-ttu-id="de50b-2779">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2779">Gets or sets the name of the font for the control to use.</span></span>

    public str font([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2780">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2780">Parameters</span></span>

<span data-ttu-id="de50b-2781">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2781">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2782">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2782">Return Value</span></span>

<span data-ttu-id="de50b-2783">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-2783">The name of the font to use, such as Tahoma or Verdana.</span></span>

### <a name="method-fontsize"></a><span data-ttu-id="de50b-2784">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="de50b-2784">Method fontSize</span></span>

<span data-ttu-id="de50b-2785">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2785">Gets or sets the size of the font for the control to use.</span></span>

    public int fontSize([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2786">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2786">Parameters</span></span>

<span data-ttu-id="de50b-2787">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2787">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2788">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2788">Return Value</span></span>

<span data-ttu-id="de50b-2789">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-2789">The height of the font in points.</span></span>

### <a name="method-forcedtooverflow"></a><span data-ttu-id="de50b-2790">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="de50b-2790">Method forcedToOverflow</span></span>

    public boolean forcedToOverflow([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2791">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2791">Parameters</span></span>

<span data-ttu-id="de50b-2792">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2792">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2793">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2793">Return Value</span></span>

### <a name="method-foregroundcolor"></a><span data-ttu-id="de50b-2794">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="de50b-2794">Method foregroundColor</span></span>

<span data-ttu-id="de50b-2795">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2795">Gets or sets the text color for the control to use.</span></span>

    public int foregroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2796">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2796">Parameters</span></span>

<span data-ttu-id="de50b-2797">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2797">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2798">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2798">Return Value</span></span>

<span data-ttu-id="de50b-2799">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-2799">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2800">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2800">Remarks</span></span>

<span data-ttu-id="de50b-2801">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2801">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="de50b-2802">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2802">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="de50b-2803">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2803">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="de50b-2804">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="de50b-2804">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="de50b-2805">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2805">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="de50b-2806">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2806">The maximum value for a single byte is 255.</span></span>

### <a name="method-formviewoption"></a><span data-ttu-id="de50b-2807">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="de50b-2807">Method formViewOption</span></span>

    public int formViewOption([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2808">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2808">Parameters</span></span>

<span data-ttu-id="de50b-2809">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2809">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2810">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2810">Return Value</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="de50b-2811">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="de50b-2811">Method hasChanged</span></span>

<span data-ttu-id="de50b-2812">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2812">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="de50b-2813">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2813">Parameters</span></span>

<span data-ttu-id="de50b-2814">val</span><span class="sxs-lookup"><span data-stu-id="de50b-2814">val</span></span>  
<span data-ttu-id="de50b-2815">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2815">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2816">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2816">Return Value</span></span>

<span data-ttu-id="de50b-2817">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2817">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="de50b-2818">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="de50b-2818">Method hasUserSetting</span></span>

<span data-ttu-id="de50b-2819">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2819">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="de50b-2820">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2820">Return Value</span></span>

<span data-ttu-id="de50b-2821">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2821">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="de50b-2822">メソッド height</span><span class="sxs-lookup"><span data-stu-id="de50b-2822">Method height</span></span>

<span data-ttu-id="de50b-2823">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2823">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-2824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2824">Parameters</span></span>

<span data-ttu-id="de50b-2825">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2825">value</span></span>  
<span data-ttu-id="de50b-2826">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2826">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-2827">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-2827">mode</span></span>  
<span data-ttu-id="de50b-2828">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2828">An Integer that indicates how the height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2829">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2829">Return Value</span></span>

<span data-ttu-id="de50b-2830">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-2830">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2831">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2831">Remarks</span></span>

<span data-ttu-id="de50b-2832">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2832">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="de50b-2833">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-2833">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="de50b-2834">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-2834">Mode.</span></span>            | <span data-ttu-id="de50b-2835">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-2835">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-2836">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-2836">-1 Exact.</span></span>        | <span data-ttu-id="de50b-2837">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2837">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-2838">0 自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-2838">0 Auto.</span></span>          | <span data-ttu-id="de50b-2839">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2839">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-2840">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-2840">1 Column height.</span></span> | <span data-ttu-id="de50b-2841">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-2841">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="de50b-2842">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2842">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="de50b-2843">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="de50b-2843">Method heightMode</span></span>

<span data-ttu-id="de50b-2844">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2844">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2845">Parameters</span></span>

<span data-ttu-id="de50b-2846">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2846">value</span></span>  
<span data-ttu-id="de50b-2847">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2847">An integer value that indicates how control height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2848">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2848">Return Value</span></span>

<span data-ttu-id="de50b-2849">計算モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-2849">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2850">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2850">Remarks</span></span>

<span data-ttu-id="de50b-2851">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-2851">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="de50b-2852">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-2852">Mode.</span></span>          | <span data-ttu-id="de50b-2853">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-2853">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-2854">正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-2854">Exact.</span></span>         | <span data-ttu-id="de50b-2855">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2855">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-2856">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-2856">Auto.</span></span>          | <span data-ttu-id="de50b-2857">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2857">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-2858">列の高さ</span><span class="sxs-lookup"><span data-stu-id="de50b-2858">Column height.</span></span> | <span data-ttu-id="de50b-2859">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-2859">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="de50b-2860">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="de50b-2860">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="de50b-2861">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="de50b-2861">Method heightValue</span></span>

<span data-ttu-id="de50b-2862">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2862">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2863">Parameters</span></span>

<span data-ttu-id="de50b-2864">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2864">value</span></span>  
<span data-ttu-id="de50b-2865">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-2865">An Integer that specifies the height in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2866">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2866">Return Value</span></span>

<span data-ttu-id="de50b-2867">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-2867">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2868">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2868">Remarks</span></span>

<span data-ttu-id="de50b-2869">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2869">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="de50b-2870">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="de50b-2870">Method helpField</span></span>

<span data-ttu-id="de50b-2871">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2871">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="de50b-2872">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2872">Return Value</span></span>

<span data-ttu-id="de50b-2873">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-2873">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2874">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2874">Remarks</span></span>

<span data-ttu-id="de50b-2875">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2875">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="de50b-2876">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2876">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="de50b-2877">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="de50b-2877">Method helpText</span></span>

<span data-ttu-id="de50b-2878">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2878">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2879">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2879">Parameters</span></span>

<span data-ttu-id="de50b-2880">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2880">value</span></span>  
<span data-ttu-id="de50b-2881">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2881">The value that is assigned as the Help text for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2882">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2882">Return Value</span></span>

<span data-ttu-id="de50b-2883">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-2883">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2884">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2884">Remarks</span></span>

<span data-ttu-id="de50b-2885">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2885">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="de50b-2886">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2886">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="de50b-2887">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="de50b-2887">Method hierarchyParent</span></span>

<span data-ttu-id="de50b-2888">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2888">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2889">Parameters</span></span>

<span data-ttu-id="de50b-2890">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2890">value</span></span>  
<span data-ttu-id="de50b-2891">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2891">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2892">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2892">Return Value</span></span>

<span data-ttu-id="de50b-2893">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2893">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="de50b-2894">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="de50b-2894">Method hWnd</span></span>

<span data-ttu-id="de50b-2895">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2895">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="de50b-2896">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2896">Return Value</span></span>

<span data-ttu-id="de50b-2897">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="de50b-2897">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2898">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2898">Remarks</span></span>

<span data-ttu-id="de50b-2899">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2899">The handle can be used with the Windows API.</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="de50b-2900">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="de50b-2900">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2901">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2901">Parameters</span></span>

<span data-ttu-id="de50b-2902">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2902">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2903">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2903">Return Value</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="de50b-2904">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="de50b-2904">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="de50b-2905">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2905">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="de50b-2906">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="de50b-2906">Method isDisplayed</span></span>

<span data-ttu-id="de50b-2907">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2907">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="de50b-2908">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2908">Return Value</span></span>

<span data-ttu-id="de50b-2909">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2909">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2910">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2910">Remarks</span></span>

<span data-ttu-id="de50b-2911">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2911">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="de50b-2912">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="de50b-2912">Method isRestricted</span></span>

<span data-ttu-id="de50b-2913">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2913">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="de50b-2914">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2914">Return Value</span></span>

<span data-ttu-id="de50b-2915">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2915">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="de50b-2916">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="de50b-2916">Method isUserSetupEnabled</span></span>

<span data-ttu-id="de50b-2917">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2917">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="de50b-2918">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2918">Parameters</span></span>

<span data-ttu-id="de50b-2919">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="de50b-2919">neededSetupRights</span></span>  
<span data-ttu-id="de50b-2920">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2920">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2921">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2921">Return Value</span></span>

<span data-ttu-id="de50b-2922">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2922">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2923">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2923">Remarks</span></span>

<span data-ttu-id="de50b-2924">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2924">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-2925">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="de50b-2925">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="de50b-2926">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2926">No changes can be made to the control.</span></span> <span data-ttu-id="de50b-2927">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2927">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="de50b-2928">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="de50b-2928">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="de50b-2929">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2929">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="de50b-2930">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="de50b-2930">The user cannot move the control.</span></span>   |
| <span data-ttu-id="de50b-2931">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="de50b-2931">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="de50b-2932">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2932">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="de50b-2933">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2933">The user can also move the control.</span></span> |

<span data-ttu-id="de50b-2934">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-2934">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="method-italic"></a><span data-ttu-id="de50b-2935">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="de50b-2935">Method italic</span></span>

    public boolean italic([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2936">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2936">Parameters</span></span>

<span data-ttu-id="de50b-2937">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2937">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2938">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2938">Return Value</span></span>

### <a name="method-keytip"></a><span data-ttu-id="de50b-2939">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="de50b-2939">Method keyTip</span></span>

    public str keyTip([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2940">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2940">Parameters</span></span>

<span data-ttu-id="de50b-2941">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2941">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2942">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2942">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="de50b-2943">メソッド left</span><span class="sxs-lookup"><span data-stu-id="de50b-2943">Method left</span></span>

<span data-ttu-id="de50b-2944">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2944">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-2945">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2945">Parameters</span></span>

<span data-ttu-id="de50b-2946">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2946">value</span></span>  
<span data-ttu-id="de50b-2947">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2947">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-2948">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-2948">mode</span></span>  
<span data-ttu-id="de50b-2949">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2949">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2950">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2950">Return Value</span></span>

<span data-ttu-id="de50b-2951">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-2951">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="de50b-2952">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="de50b-2952">Method leftMode</span></span>

<span data-ttu-id="de50b-2953">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2953">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2954">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2954">Parameters</span></span>

<span data-ttu-id="de50b-2955">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2955">value</span></span>  
<span data-ttu-id="de50b-2956">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2956">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2957">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2957">Return Value</span></span>

<span data-ttu-id="de50b-2958">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-2958">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="de50b-2959">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="de50b-2959">Method leftValue</span></span>

<span data-ttu-id="de50b-2960">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-2960">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2961">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2961">Parameters</span></span>

<span data-ttu-id="de50b-2962">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2962">value</span></span>  
<span data-ttu-id="de50b-2963">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-2963">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2964">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2964">Return Value</span></span>

<span data-ttu-id="de50b-2965">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-2965">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="de50b-2966">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="de50b-2966">Method markAsUserAdd</span></span>

<span data-ttu-id="de50b-2967">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="de50b-2967">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2968">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2968">Parameters</span></span>

<span data-ttu-id="de50b-2969">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2969">value</span></span>  
<span data-ttu-id="de50b-2970">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2970">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2971">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2971">Return Value</span></span>

<span data-ttu-id="de50b-2972">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-2972">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-menufunction"></a><span data-ttu-id="de50b-2973">メソッド menufunction</span><span class="sxs-lookup"><span data-stu-id="de50b-2973">Method menufunction</span></span>

    public xMenuFunction menufunction()

#### <a name="return-value"></a><span data-ttu-id="de50b-2974">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2974">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="de50b-2975">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="de50b-2975">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2976">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2976">Parameters</span></span>

<span data-ttu-id="de50b-2977">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2977">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2978">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2978">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="de50b-2979">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="de50b-2979">Method menuItemType</span></span>

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="de50b-2980">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2980">Parameters</span></span>

<span data-ttu-id="de50b-2981">値</span><span class="sxs-lookup"><span data-stu-id="de50b-2981">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-2982">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2982">Return Value</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="de50b-2983">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="de50b-2983">Method mouseDblClick</span></span>

<span data-ttu-id="de50b-2984">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2984">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-2985">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-2985">Parameters</span></span>

<span data-ttu-id="de50b-2986">x</span><span class="sxs-lookup"><span data-stu-id="de50b-2986">x</span></span>  
<span data-ttu-id="de50b-2987">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2987">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-2988">y</span><span class="sxs-lookup"><span data-stu-id="de50b-2988">y</span></span>  
<span data-ttu-id="de50b-2989">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2989">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-2990">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-2990">button</span></span>  
<span data-ttu-id="de50b-2991">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2991">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-2992">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-2992">Ctrl</span></span>  
<span data-ttu-id="de50b-2993">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2993">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-2994">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-2994">Shift</span></span>  
<span data-ttu-id="de50b-2995">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-2995">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-2996">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-2996">Return Value</span></span>

<span data-ttu-id="de50b-2997">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-2997">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-2998">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-2998">Remarks</span></span>

<span data-ttu-id="de50b-2999">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-2999">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="de50b-3000">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="de50b-3000">Method mouseDown</span></span>

<span data-ttu-id="de50b-3001">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3001">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-3002">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3002">Parameters</span></span>

<span data-ttu-id="de50b-3003">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3003">x</span></span>  
<span data-ttu-id="de50b-3004">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3004">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3005">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3005">y</span></span>  
<span data-ttu-id="de50b-3006">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3006">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3007">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-3007">button</span></span>  
<span data-ttu-id="de50b-3008">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3008">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3009">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-3009">Ctrl</span></span>  
<span data-ttu-id="de50b-3010">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3010">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3011">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-3011">Shift</span></span>  
<span data-ttu-id="de50b-3012">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3012">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3013">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3013">Return Value</span></span>

<span data-ttu-id="de50b-3014">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3014">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3015">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3015">Remarks</span></span>

<span data-ttu-id="de50b-3016">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3016">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="de50b-3017">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3017">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="de50b-3018">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="de50b-3018">Method mouseMove</span></span>

<span data-ttu-id="de50b-3019">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3019">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-3020">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3020">Parameters</span></span>

<span data-ttu-id="de50b-3021">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3021">x</span></span>  
<span data-ttu-id="de50b-3022">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3022">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3023">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3023">y</span></span>  
<span data-ttu-id="de50b-3024">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3024">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3025">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-3025">button</span></span>  
<span data-ttu-id="de50b-3026">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3026">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3027">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-3027">Ctrl</span></span>  
<span data-ttu-id="de50b-3028">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3028">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3029">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-3029">Shift</span></span>  
<span data-ttu-id="de50b-3030">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3030">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3031">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3031">Return Value</span></span>

<span data-ttu-id="de50b-3032">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3032">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3033">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3033">Remarks</span></span>

<span data-ttu-id="de50b-3034">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3034">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="de50b-3035">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="de50b-3035">Method mouseUp</span></span>

<span data-ttu-id="de50b-3036">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3036">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-3037">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3037">Parameters</span></span>

<span data-ttu-id="de50b-3038">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3038">x</span></span>  
<span data-ttu-id="de50b-3039">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3039">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3040">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3040">y</span></span>  
<span data-ttu-id="de50b-3041">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3041">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3042">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-3042">button</span></span>  
<span data-ttu-id="de50b-3043">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3043">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3044">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-3044">Ctrl</span></span>  
<span data-ttu-id="de50b-3045">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3045">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3046">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-3046">Shift</span></span>  
<span data-ttu-id="de50b-3047">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3047">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3048">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3048">Return Value</span></span>

<span data-ttu-id="de50b-3049">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3049">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3050">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3050">Remarks</span></span>

<span data-ttu-id="de50b-3051">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3051">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="de50b-3052">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3052">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="de50b-3053">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="de50b-3053">Method multiSelect</span></span>

    public int multiSelect([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3054">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3054">Parameters</span></span>

<span data-ttu-id="de50b-3055">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3055">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3056">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3056">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="de50b-3057">メソッド名</span><span class="sxs-lookup"><span data-stu-id="de50b-3057">Method name</span></span>

<span data-ttu-id="de50b-3058">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3058">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3059">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3059">Parameters</span></span>

<span data-ttu-id="de50b-3060">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3060">value</span></span>  
<span data-ttu-id="de50b-3061">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-3061">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3062">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3062">Return Value</span></span>

<span data-ttu-id="de50b-3063">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-3063">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3064">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3064">Remarks</span></span>

<span data-ttu-id="de50b-3065">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-3065">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="de50b-3066">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-3066">It must begin with a letter.</span></span>
-   <span data-ttu-id="de50b-3067">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3067">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="de50b-3068">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3068">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="de50b-3069">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3069">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="de50b-3070">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3070">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="de50b-3071">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="de50b-3071">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3072">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3072">Parameters</span></span>

<span data-ttu-id="de50b-3073">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3073">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3074">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3074">Return Value</span></span>

### <a name="method-needsrecord"></a><span data-ttu-id="de50b-3075">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="de50b-3075">Method needsRecord</span></span>

    public int needsRecord([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3076">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3076">Parameters</span></span>

<span data-ttu-id="de50b-3077">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3077">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3078">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3078">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="de50b-3079">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="de50b-3079">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3080">Parameters</span></span>

<span data-ttu-id="de50b-3081">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3081">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3082">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3082">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="de50b-3083">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="de50b-3083">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3084">Parameters</span></span>

<span data-ttu-id="de50b-3085">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3085">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3086">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3086">Return Value</span></span>

### <a name="method-openmode"></a><span data-ttu-id="de50b-3087">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="de50b-3087">Method openMode</span></span>

    public int openMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3088">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3088">Parameters</span></span>

<span data-ttu-id="de50b-3089">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3089">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3090">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3090">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="de50b-3091">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="de50b-3091">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="de50b-3092">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3092">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="de50b-3093">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="de50b-3093">Method parameters</span></span>

<span data-ttu-id="de50b-3094">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3094">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3095">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3095">Parameters</span></span>

<span data-ttu-id="de50b-3096">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3096">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3097">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3097">Return Value</span></span>

<span data-ttu-id="de50b-3098">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-3098">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3099">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3099">Remarks</span></span>

<span data-ttu-id="de50b-3100">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="de50b-3100">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="de50b-3101">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3101">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="de50b-3102">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="de50b-3102">Method parentControl</span></span>

<span data-ttu-id="de50b-3103">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3103">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="de50b-3104">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3104">Return Value</span></span>

<span data-ttu-id="de50b-3105">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="de50b-3105">The parent control for the control.</span></span>

### <a name="method-primary"></a><span data-ttu-id="de50b-3106">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="de50b-3106">Method primary</span></span>

    public boolean primary([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3107">Parameters</span></span>

<span data-ttu-id="de50b-3108">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3108">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3109">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3109">Return Value</span></span>

### <a name="method-saverecord"></a><span data-ttu-id="de50b-3110">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="de50b-3110">Method saveRecord</span></span>

    public boolean saveRecord([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3111">Parameters</span></span>

<span data-ttu-id="de50b-3112">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3112">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3113">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3113">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="de50b-3114">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="de50b-3114">Method securityKey</span></span>

<span data-ttu-id="de50b-3115">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3115">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3116">Parameters</span></span>

<span data-ttu-id="de50b-3117">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3117">value</span></span>  
<span data-ttu-id="de50b-3118">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3118">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3119">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3119">Return Value</span></span>

<span data-ttu-id="de50b-3120">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3120">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-sendexternalcontext"></a><span data-ttu-id="de50b-3121">メソッド sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="de50b-3121">Method sendExternalContext</span></span>

    public boolean sendExternalContext([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3122">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3122">Parameters</span></span>

<span data-ttu-id="de50b-3123">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3123">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3124">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3124">Return Value</span></span>

### <a name="method-shortkey"></a><span data-ttu-id="de50b-3125">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="de50b-3125">Method shortkey</span></span>

    public int shortkey([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3126">Parameters</span></span>

<span data-ttu-id="de50b-3127">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3127">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3128">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3128">Return Value</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="de50b-3129">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="de50b-3129">Method showContextMenu</span></span>

<span data-ttu-id="de50b-3130">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3130">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="de50b-3131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3131">Parameters</span></span>

<span data-ttu-id="de50b-3132">menuHandle</span><span class="sxs-lookup"><span data-stu-id="de50b-3132">menuHandle</span></span>  
<span data-ttu-id="de50b-3133">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-3133">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3134">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3134">Return Value</span></span>

<span data-ttu-id="de50b-3135">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3135">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-showshortcut"></a><span data-ttu-id="de50b-3136">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="de50b-3136">Method showShortCut</span></span>

    public boolean showShortCut([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3137">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3137">Parameters</span></span>

<span data-ttu-id="de50b-3138">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3138">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3139">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3139">Return Value</span></span>

### <a name="method-skip"></a><span data-ttu-id="de50b-3140">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="de50b-3140">Method skip</span></span>

<span data-ttu-id="de50b-3141">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3141">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3142">Parameters</span></span>

<span data-ttu-id="de50b-3143">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3143">value</span></span>  
<span data-ttu-id="de50b-3144">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3144">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3145">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3145">Return Value</span></span>

<span data-ttu-id="de50b-3146">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-3146">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3147">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3147">Remarks</span></span>

<span data-ttu-id="de50b-3148">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3148">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="method-sort"></a><span data-ttu-id="de50b-3149">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="de50b-3149">Method sort</span></span>

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a><span data-ttu-id="de50b-3150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3150">Parameters</span></span>

<span data-ttu-id="de50b-3151">sortDirection</span><span class="sxs-lookup"><span data-stu-id="de50b-3151">sortDirection</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3152">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3152">Return Value</span></span>

### <a name="method-style"></a><span data-ttu-id="de50b-3153">メソッド style</span><span class="sxs-lookup"><span data-stu-id="de50b-3153">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3154">Parameters</span></span>

<span data-ttu-id="de50b-3155">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3155">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3156">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3156">Return Value</span></span>

### <a name="method-text"></a><span data-ttu-id="de50b-3157">メソッド text</span><span class="sxs-lookup"><span data-stu-id="de50b-3157">Method text</span></span>

    public str text([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3158">Parameters</span></span>

<span data-ttu-id="de50b-3159">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3159">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3160">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3160">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="de50b-3161">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="de50b-3161">Method toolTip</span></span>

<span data-ttu-id="de50b-3162">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3162">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="de50b-3163">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3163">Return Value</span></span>

<span data-ttu-id="de50b-3164">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-3164">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3165">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3165">Remarks</span></span>

<span data-ttu-id="de50b-3166">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3166">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="de50b-3167">メソッド top</span><span class="sxs-lookup"><span data-stu-id="de50b-3167">Method top</span></span>

<span data-ttu-id="de50b-3168">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3168">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-3169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3169">Parameters</span></span>

<span data-ttu-id="de50b-3170">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3170">value</span></span>  
<span data-ttu-id="de50b-3171">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3171">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-3172">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-3172">mode</span></span>  
<span data-ttu-id="de50b-3173">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3173">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3174">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3174">Return Value</span></span>

<span data-ttu-id="de50b-3175">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-3175">The vertical position of the control in the form.</span></span>

### <a name="method-topmode"></a><span data-ttu-id="de50b-3176">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="de50b-3176">Method topMode</span></span>

<span data-ttu-id="de50b-3177">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3177">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3178">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3178">Parameters</span></span>

<span data-ttu-id="de50b-3179">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3179">value</span></span>  
<span data-ttu-id="de50b-3180">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3180">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3181">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3181">Return Value</span></span>

<span data-ttu-id="de50b-3182">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-3182">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="de50b-3183">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="de50b-3183">Method topValue</span></span>

<span data-ttu-id="de50b-3184">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3184">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3185">Parameters</span></span>

<span data-ttu-id="de50b-3186">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3186">value</span></span>  
<span data-ttu-id="de50b-3187">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3187">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3188">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3188">Return Value</span></span>

<span data-ttu-id="de50b-3189">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-3189">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="de50b-3190">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="de50b-3190">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3191">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3191">Parameters</span></span>

<span data-ttu-id="de50b-3192">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3192">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3193">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3193">Return Value</span></span>

### <a name="method-underline"></a><span data-ttu-id="de50b-3194">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="de50b-3194">Method underline</span></span>

    public boolean underline([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3195">Parameters</span></span>

<span data-ttu-id="de50b-3196">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3196">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3197">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3197">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="de50b-3198">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="de50b-3198">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="de50b-3199">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3199">Parameters</span></span>

<span data-ttu-id="de50b-3200">データ</span><span class="sxs-lookup"><span data-stu-id="de50b-3200">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3201">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3201">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="de50b-3202">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="de50b-3202">Method userData</span></span>

<span data-ttu-id="de50b-3203">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3203">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3204">Parameters</span></span>

<span data-ttu-id="de50b-3205">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3205">value</span></span>  
<span data-ttu-id="de50b-3206">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3206">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3207">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3207">Return Value</span></span>

<span data-ttu-id="de50b-3208">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="de50b-3208">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="de50b-3209">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="de50b-3209">Method userDataItem</span></span>

<span data-ttu-id="de50b-3210">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3210">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3211">Parameters</span></span>

<span data-ttu-id="de50b-3212">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3212">value</span></span>  
<span data-ttu-id="de50b-3213">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3213">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3214">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3214">Return Value</span></span>

<span data-ttu-id="de50b-3215">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="de50b-3215">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="de50b-3216">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="de50b-3216">Method userDataItems</span></span>

<span data-ttu-id="de50b-3217">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3217">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3218">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3218">Parameters</span></span>

<span data-ttu-id="de50b-3219">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3219">value</span></span>  
<span data-ttu-id="de50b-3220">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3220">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3221">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3221">Return Value</span></span>

<span data-ttu-id="de50b-3222">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="de50b-3222">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="de50b-3223">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="de50b-3223">Method userDisable</span></span>

<span data-ttu-id="de50b-3224">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3224">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3225">Parameters</span></span>

<span data-ttu-id="de50b-3226">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3226">value</span></span>  
<span data-ttu-id="de50b-3227">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3227">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3228">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3228">Return Value</span></span>

<span data-ttu-id="de50b-3229">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3229">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="de50b-3230">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="de50b-3230">Method userHeight</span></span>

<span data-ttu-id="de50b-3231">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3231">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3232">Parameters</span></span>

<span data-ttu-id="de50b-3233">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3233">value</span></span>  
<span data-ttu-id="de50b-3234">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3234">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3235">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3235">Return Value</span></span>

<span data-ttu-id="de50b-3236">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-3236">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="de50b-3237">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="de50b-3237">Method userHide</span></span>

<span data-ttu-id="de50b-3238">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3238">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3239">Parameters</span></span>

<span data-ttu-id="de50b-3240">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3240">value</span></span>  
<span data-ttu-id="de50b-3241">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3241">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3242">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3242">Return Value</span></span>

<span data-ttu-id="de50b-3243">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3243">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3244">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3244">Remarks</span></span>

<span data-ttu-id="de50b-3245">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3245">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="de50b-3246">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3246">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="de50b-3247">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3247">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="de50b-3248">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="de50b-3248">Method userOrgContainer</span></span>

<span data-ttu-id="de50b-3249">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3249">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3250">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3250">Parameters</span></span>

<span data-ttu-id="de50b-3251">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3251">value</span></span>  
<span data-ttu-id="de50b-3252">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3252">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3253">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3253">Return Value</span></span>

<span data-ttu-id="de50b-3254">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="de50b-3254">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="de50b-3255">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="de50b-3255">Method userOrgSibling</span></span>

<span data-ttu-id="de50b-3256">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3256">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3257">Parameters</span></span>

<span data-ttu-id="de50b-3258">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3258">value</span></span>  
<span data-ttu-id="de50b-3259">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3259">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3260">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3260">Return Value</span></span>

<span data-ttu-id="de50b-3261">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="de50b-3261">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="de50b-3262">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="de50b-3262">Method userPromptText</span></span>

<span data-ttu-id="de50b-3263">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3263">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3264">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3264">Parameters</span></span>

<span data-ttu-id="de50b-3265">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3265">value</span></span>  
<span data-ttu-id="de50b-3266">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3266">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3267">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3267">Return Value</span></span>

<span data-ttu-id="de50b-3268">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-3268">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="de50b-3269">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="de50b-3269">Method userSecurityLevel</span></span>

<span data-ttu-id="de50b-3270">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3270">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3271">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3271">Parameters</span></span>

<span data-ttu-id="de50b-3272">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3272">value</span></span>  
<span data-ttu-id="de50b-3273">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3273">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3274">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3274">Return Value</span></span>

<span data-ttu-id="de50b-3275">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="de50b-3275">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="de50b-3276">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="de50b-3276">Method userSkip</span></span>

<span data-ttu-id="de50b-3277">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3277">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3278">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3278">Parameters</span></span>

<span data-ttu-id="de50b-3279">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3279">value</span></span>  
<span data-ttu-id="de50b-3280">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3280">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="de50b-3281">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3281">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3282">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3282">Return Value</span></span>

<span data-ttu-id="de50b-3283">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3283">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="de50b-3284">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="de50b-3284">Method userWidth</span></span>

<span data-ttu-id="de50b-3285">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3285">Sets or returns the width of the control in pixels.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3286">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3286">Parameters</span></span>

<span data-ttu-id="de50b-3287">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3287">value</span></span>  
<span data-ttu-id="de50b-3288">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3288">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3289">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3289">Return Value</span></span>

<span data-ttu-id="de50b-3290">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3290">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3291">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3291">Remarks</span></span>

<span data-ttu-id="de50b-3292">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3292">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="de50b-3293">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="de50b-3293">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="de50b-3294">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3294">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-value"></a><span data-ttu-id="de50b-3295">メソッド value</span><span class="sxs-lookup"><span data-stu-id="de50b-3295">Method value</span></span>

    public boolean value([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3296">Parameters</span></span>

<span data-ttu-id="de50b-3297">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3297">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3298">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3298">Return Value</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="de50b-3299">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="de50b-3299">Method verticalSpacing</span></span>

<span data-ttu-id="de50b-3300">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3300">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-3301">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3301">Parameters</span></span>

<span data-ttu-id="de50b-3302">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3302">value</span></span>  
<span data-ttu-id="de50b-3303">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3303">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-3304">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-3304">mode</span></span>  
<span data-ttu-id="de50b-3305">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3305">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3306">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3306">Return Value</span></span>

<span data-ttu-id="de50b-3307">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="de50b-3307">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="de50b-3308">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="de50b-3308">Method verticalSpacingMode</span></span>

<span data-ttu-id="de50b-3309">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3309">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-3310">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3310">Parameters</span></span>

<span data-ttu-id="de50b-3311">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-3311">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3312">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3312">Return Value</span></span>

<span data-ttu-id="de50b-3313">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-3313">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="de50b-3314">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="de50b-3314">Method verticalSpacingValue</span></span>

<span data-ttu-id="de50b-3315">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3315">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3316">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3316">Parameters</span></span>

<span data-ttu-id="de50b-3317">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3317">value</span></span>  
<span data-ttu-id="de50b-3318">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3318">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3319">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3319">Return Value</span></span>

<span data-ttu-id="de50b-3320">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="de50b-3320">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="de50b-3321">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="de50b-3321">Method visible</span></span>

<span data-ttu-id="de50b-3322">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3322">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3323">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3323">Parameters</span></span>

<span data-ttu-id="de50b-3324">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3324">value</span></span>  
<span data-ttu-id="de50b-3325">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3325">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3326">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3326">Return Value</span></span>

<span data-ttu-id="de50b-3327">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-3327">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="de50b-3328">メソッド width</span><span class="sxs-lookup"><span data-stu-id="de50b-3328">Method width</span></span>

<span data-ttu-id="de50b-3329">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3329">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-3330">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3330">Parameters</span></span>

<span data-ttu-id="de50b-3331">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3331">value</span></span>  
<span data-ttu-id="de50b-3332">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3332">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-3333">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-3333">mode</span></span>  
<span data-ttu-id="de50b-3334">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3334">An Integer that indicates how the width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3335">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3335">Return Value</span></span>

<span data-ttu-id="de50b-3336">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-3336">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3337">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3337">Remarks</span></span>

<span data-ttu-id="de50b-3338">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3338">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="de50b-3339">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-3339">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="de50b-3340">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-3340">Mode.</span></span>           | <span data-ttu-id="de50b-3341">幅計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-3341">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-3342">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-3342">-1 Exact.</span></span>       | <span data-ttu-id="de50b-3343">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3343">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-3344">0 自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-3344">0 Auto.</span></span>         | <span data-ttu-id="de50b-3345">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3345">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-3346">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-3346">1 Column width.</span></span> | <span data-ttu-id="de50b-3347">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-3347">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="de50b-3348">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3348">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="de50b-3349">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="de50b-3349">Method widthMode</span></span>

<span data-ttu-id="de50b-3350">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3350">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3351">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3351">Parameters</span></span>

<span data-ttu-id="de50b-3352">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3352">value</span></span>  
<span data-ttu-id="de50b-3353">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3353">An integer value that indicates how control width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3354">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3354">Return Value</span></span>

<span data-ttu-id="de50b-3355">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3355">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3356">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3356">Remarks</span></span>

<span data-ttu-id="de50b-3357">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-3357">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="de50b-3358">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-3358">Mode.</span></span>         | <span data-ttu-id="de50b-3359">幅計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-3359">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-3360">正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-3360">Exact.</span></span>        | <span data-ttu-id="de50b-3361">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3361">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-3362">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-3362">Auto.</span></span>         | <span data-ttu-id="de50b-3363">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3363">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-3364">列の幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-3364">Column width.</span></span> | <span data-ttu-id="de50b-3365">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-3365">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="de50b-3366">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="de50b-3366">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="de50b-3367">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="de50b-3367">Method widthValue</span></span>

<span data-ttu-id="de50b-3368">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3368">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3369">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3369">Parameters</span></span>

<span data-ttu-id="de50b-3370">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3370">value</span></span>  
<span data-ttu-id="de50b-3371">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3371">An Integer that specifies the width in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3372">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3372">Return Value</span></span>

<span data-ttu-id="de50b-3373">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-3373">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3374">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3374">Remarks</span></span>

<span data-ttu-id="de50b-3375">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3375">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-prefcolumnsize"></a><span data-ttu-id="de50b-3376">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="de50b-3376">Method prefColumnSize</span></span>

<span data-ttu-id="de50b-3377">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3377">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="de50b-3378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3378">Parameters</span></span>

<span data-ttu-id="de50b-3379">width</span><span class="sxs-lookup"><span data-stu-id="de50b-3379">width</span></span>  
<span data-ttu-id="de50b-3380">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="de50b-3380">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="de50b-3381">height</span><span class="sxs-lookup"><span data-stu-id="de50b-3381">height</span></span>  
<span data-ttu-id="de50b-3382">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="de50b-3382">The preferred height of the control.</span></span>

### <a name="method-lostfocus"></a><span data-ttu-id="de50b-3383">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-3383">Method lostFocus</span></span>

<span data-ttu-id="de50b-3384">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3384">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-resetusersetting"></a><span data-ttu-id="de50b-3385">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="de50b-3385">Method resetUserSetting</span></span>

<span data-ttu-id="de50b-3386">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="de50b-3386">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-context"></a><span data-ttu-id="de50b-3387">メソッド context</span><span class="sxs-lookup"><span data-stu-id="de50b-3387">Method context</span></span>

<span data-ttu-id="de50b-3388">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3388">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-drop"></a><span data-ttu-id="de50b-3389">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="de50b-3389">Method drop</span></span>

<span data-ttu-id="de50b-3390">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3390">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-3391">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3391">Parameters</span></span>

<span data-ttu-id="de50b-3392">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-3392">dragSource</span></span>  
<span data-ttu-id="de50b-3393">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3393">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3394">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-3394">dragMode</span></span>  
<span data-ttu-id="de50b-3395">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3395">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3396">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3396">x</span></span>  
<span data-ttu-id="de50b-3397">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3397">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3398">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3398">y</span></span>  
<span data-ttu-id="de50b-3399">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3399">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-onlostfocus"></a><span data-ttu-id="de50b-3400">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-3400">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-3401">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3401">Parameters</span></span>

<span data-ttu-id="de50b-3402">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-3402">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-3403">e</span><span class="sxs-lookup"><span data-stu-id="de50b-3403">e</span></span>  

### <a name="method-gotfocus"></a><span data-ttu-id="de50b-3404">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-3404">Method gotFocus</span></span>

<span data-ttu-id="de50b-3405">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3405">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-mouseenter"></a><span data-ttu-id="de50b-3406">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="de50b-3406">Method mouseEnter</span></span>

<span data-ttu-id="de50b-3407">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3407">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-3408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3408">Parameters</span></span>

<span data-ttu-id="de50b-3409">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3409">x</span></span>  
<span data-ttu-id="de50b-3410">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3410">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3411">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3411">y</span></span>  
<span data-ttu-id="de50b-3412">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3412">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3413">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-3413">button</span></span>  
<span data-ttu-id="de50b-3414">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3414">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3415">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-3415">Ctrl</span></span>  
<span data-ttu-id="de50b-3416">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3416">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-3417">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-3417">Shift</span></span>  
<span data-ttu-id="de50b-3418">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3418">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-paste"></a><span data-ttu-id="de50b-3419">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="de50b-3419">Method paste</span></span>

<span data-ttu-id="de50b-3420">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3420">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-ongotfocus"></a><span data-ttu-id="de50b-3421">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-3421">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-3422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3422">Parameters</span></span>

<span data-ttu-id="de50b-3423">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-3423">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-3424">e</span><span class="sxs-lookup"><span data-stu-id="de50b-3424">e</span></span>  

### <a name="method-enddrag"></a><span data-ttu-id="de50b-3425">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="de50b-3425">Method endDrag</span></span>

<span data-ttu-id="de50b-3426">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3426">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="de50b-3427">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3427">Remarks</span></span>

<span data-ttu-id="de50b-3428">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3428">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="de50b-3429">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3429">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-cut"></a><span data-ttu-id="de50b-3430">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="de50b-3430">Method cut</span></span>

<span data-ttu-id="de50b-3431">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="de50b-3431">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-filter"></a><span data-ttu-id="de50b-3432">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="de50b-3432">Method filter</span></span>

    public void filter([str filterStr])

#### <a name="parameters"></a><span data-ttu-id="de50b-3433">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3433">Parameters</span></span>

<span data-ttu-id="de50b-3434">filterStr</span><span class="sxs-lookup"><span data-stu-id="de50b-3434">filterStr</span></span>  

### <a name="method-displaycontrol"></a><span data-ttu-id="de50b-3435">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="de50b-3435">Method displayControl</span></span>

<span data-ttu-id="de50b-3436">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3436">Displays the control.</span></span>

    public void displayControl()

### <a name="method-inputsearch"></a><span data-ttu-id="de50b-3437">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="de50b-3437">Method inputSearch</span></span>

<span data-ttu-id="de50b-3438">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3438">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="de50b-3439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3439">Parameters</span></span>

<span data-ttu-id="de50b-3440">searchStr</span><span class="sxs-lookup"><span data-stu-id="de50b-3440">searchStr</span></span>  
<span data-ttu-id="de50b-3441">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3441">The string value to use to filter data; optional.</span></span>

### <a name="method-copy"></a><span data-ttu-id="de50b-3442">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="de50b-3442">Method copy</span></span>

<span data-ttu-id="de50b-3443">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="de50b-3443">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-clicked"></a><span data-ttu-id="de50b-3444">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="de50b-3444">Method clicked</span></span>

    public void clicked()

### <a name="method-onclicked"></a><span data-ttu-id="de50b-3445">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="de50b-3445">Method OnClicked</span></span>

    private void OnClicked([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-3446">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3446">Parameters</span></span>

<span data-ttu-id="de50b-3447">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-3447">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-3448">e</span><span class="sxs-lookup"><span data-stu-id="de50b-3448">e</span></span>  

### <a name="method-dropex"></a><span data-ttu-id="de50b-3449">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="de50b-3449">Method dropEx</span></span>

<span data-ttu-id="de50b-3450">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3450">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-3451">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3451">Parameters</span></span>

<span data-ttu-id="de50b-3452">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-3452">dragSource</span></span>  
<span data-ttu-id="de50b-3453">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3453">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3454">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-3454">dragMode</span></span>  
<span data-ttu-id="de50b-3455">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3455">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3456">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3456">x</span></span>  
<span data-ttu-id="de50b-3457">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3457">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3458">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3458">y</span></span>  
<span data-ttu-id="de50b-3459">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3459">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-mouseleave"></a><span data-ttu-id="de50b-3460">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="de50b-3460">Method mouseLeave</span></span>

<span data-ttu-id="de50b-3461">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3461">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-setfocus"></a><span data-ttu-id="de50b-3462">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-3462">Method setFocus</span></span>

<span data-ttu-id="de50b-3463">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3463">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-dragleave"></a><span data-ttu-id="de50b-3464">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="de50b-3464">Method dragLeave</span></span>

<span data-ttu-id="de50b-3465">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3465">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-jumpref"></a><span data-ttu-id="de50b-3466">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="de50b-3466">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-registeroverridemethod"></a><span data-ttu-id="de50b-3467">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="de50b-3467">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="de50b-3468">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3468">Parameters</span></span>

<span data-ttu-id="de50b-3469">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="de50b-3469">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="de50b-3470">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="de50b-3470">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="de50b-3471">overrideObject</span><span class="sxs-lookup"><span data-stu-id="de50b-3471">overrideObject</span></span>  

## <a name="class-formgridcontrol"></a><span data-ttu-id="de50b-3472">クラス FormGridControl</span><span class="sxs-lookup"><span data-stu-id="de50b-3472">Class FormGridControl</span></span>
    class FormGridControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="de50b-3473">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3473">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="de50b-3474">例</span><span class="sxs-lookup"><span data-stu-id="de50b-3474">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="de50b-3475">メソッド</span><span class="sxs-lookup"><span data-stu-id="de50b-3475">Methods</span></span>

| <span data-ttu-id="de50b-3476">方法</span><span class="sxs-lookup"><span data-stu-id="de50b-3476">Method</span></span>                                                                                                              | <span data-ttu-id="de50b-3477">説明</span><span class="sxs-lookup"><span data-stu-id="de50b-3477">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-3478">public int activeBackColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3478">public int activeBackColor(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3479">public int activeForeColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3479">public int activeForeColor(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3480">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3480">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3481">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3481">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3482">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3482">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3483">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3483">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="de50b-3484">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3484">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-3485">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3485">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="de50b-3486">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3486">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-3487">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="de50b-3487">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="de50b-3488">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3488">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="de50b-3489">public int alternateRowShading(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3489">public int alternateRowShading(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3490">public boolean autoDataGroup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3490">public boolean autoDataGroup(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3491">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3491">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="de50b-3492">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3492">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="de50b-3493">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3493">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="de50b-3494">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3494">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="de50b-3495">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3495">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="de50b-3496">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3496">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-3497">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-3497">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="de50b-3498">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3498">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-3499">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3499">public int border(\[int value\])</span></span>                                                                                    | <span data-ttu-id="de50b-3500">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3500">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="de50b-3501">public int bottomMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3501">public int bottomMargin(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3502">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="de50b-3502">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="de50b-3503">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3503">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="de50b-3504">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3504">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3505">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="de50b-3505">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3506">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3506">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="de50b-3507">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3507">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-3508">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3508">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="de50b-3509">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3509">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-3510">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="de50b-3510">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="de50b-3511">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3511">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="de50b-3512">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="de50b-3512">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3513">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="de50b-3513">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3514">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="de50b-3514">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3515">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3515">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="de50b-3516">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3516">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="de50b-3517">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3517">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3518">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3518">public str dataGroup(\[str value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3519">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3519">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="de50b-3520">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3520">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="de50b-3521">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3521">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="de50b-3522">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3522">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-3523">public str defaultAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3523">public str defaultAction(\[str value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3524">public str defaultActionLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3524">public str defaultActionLabel(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3525">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3525">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="de50b-3526">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3526">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span> |
| <span data-ttu-id="de50b-3527">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3527">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="de50b-3528">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3528">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="de50b-3529">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-3529">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="de50b-3530">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3530">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="de50b-3531">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-3531">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="de50b-3532">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3532">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="de50b-3533">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="de50b-3533">public str dragText()</span></span>                                                                                               | <span data-ttu-id="de50b-3534">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3534">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-3535">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3535">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="de50b-3536">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3536">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-3537">public boolean exportAllowed(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3537">public boolean exportAllowed(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3538">public str exportLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3538">public str exportLabel(\[str value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3539">public Struct getLineData(int lineNumber)</span><span class="sxs-lookup"><span data-stu-id="de50b-3539">public Struct getLineData(int lineNumber)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3540">public Struct getSelectedData()</span><span class="sxs-lookup"><span data-stu-id="de50b-3540">public Struct getSelectedData()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3541">public boolean gridLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3541">public boolean gridLines(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3542">public int gridLinesStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3542">public int gridLinesStyle(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3543">public str groupBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3543">public str groupBy(\[str value\])</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3544">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3544">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="de50b-3545">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3545">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="de50b-3546">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="de50b-3546">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="de50b-3547">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3547">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="de50b-3548">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3548">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="de50b-3549">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3549">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-3550">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3550">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="de50b-3551">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3551">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-3552">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3552">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="de50b-3553">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3553">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="de50b-3554">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="de50b-3554">public str helpField()</span></span>                                                                                              | <span data-ttu-id="de50b-3555">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3555">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-3556">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3556">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="de50b-3557">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3557">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="de50b-3558">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3558">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="de50b-3559">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3559">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="de50b-3560">public boolean highlightActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3560">public boolean highlightActive(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3561">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="de50b-3561">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="de50b-3562">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3562">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-3563">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="de50b-3563">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3564">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="de50b-3564">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="de50b-3565">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3565">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="de50b-3566">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="de50b-3566">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="de50b-3567">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3567">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="de50b-3568">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="de50b-3568">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="de50b-3569">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3569">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="de50b-3570">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="de50b-3570">public boolean leave()</span></span>                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3571">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3571">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="de50b-3572">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3572">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="de50b-3573">public int leftMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3573">public int leftMargin(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3574">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3574">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="de50b-3575">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3575">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-3576">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3576">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="de50b-3577">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3577">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="de50b-3578">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3578">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="de50b-3579">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="de50b-3579">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="de50b-3580">public int moreRowsIndicator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3580">public int moreRowsIndicator(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3581">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-3581">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="de50b-3582">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3582">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="de50b-3583">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-3583">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="de50b-3584">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3584">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-3585">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-3585">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="de50b-3586">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3586">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="de50b-3587">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-3587">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="de50b-3588">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3588">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="de50b-3589">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3589">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3590">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3590">public boolean multiSelect(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3591">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3591">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="de50b-3592">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3592">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="de50b-3593">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3593">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3594">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="de50b-3594">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3595">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="de50b-3595">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="de50b-3596">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3596">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="de50b-3597">public int rightMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3597">public int rightMargin(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3598">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3598">public int scrollbars(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3599">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3599">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="de50b-3600">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3600">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-3601">public boolean showColLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3601">public boolean showColLabels(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3602">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="de50b-3602">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="de50b-3603">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3603">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-3604">public boolean showRowLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3604">public boolean showRowLabels(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3605">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3605">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="de50b-3606">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3606">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="de50b-3607">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3607">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3608">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3608">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3609">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="de50b-3609">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="de50b-3610">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3610">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-3611">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3611">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="de50b-3612">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3612">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-3613">public int topMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3613">public int topMargin(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3614">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3614">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="de50b-3615">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3615">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-3616">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3616">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="de50b-3617">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3617">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-3618">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3618">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3619">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="de50b-3619">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3620">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3620">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="de50b-3621">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3621">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="de50b-3622">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3622">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="de50b-3623">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3623">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="de50b-3624">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3624">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="de50b-3625">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3625">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-3626">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3626">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="de50b-3627">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3627">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="de50b-3628">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3628">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="de50b-3629">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3629">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="de50b-3630">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3630">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="de50b-3631">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3631">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="de50b-3632">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3632">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="de50b-3633">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3633">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="de50b-3634">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3634">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="de50b-3635">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3635">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-3636">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3636">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="de50b-3637">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3637">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="de50b-3638">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3638">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="de50b-3639">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3639">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="de50b-3640">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3640">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="de50b-3641">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3641">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="de50b-3642">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3642">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="de50b-3643">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3643">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="de50b-3644">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3644">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3645">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3645">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="de50b-3646">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3646">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-3647">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3647">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="de50b-3648">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3648">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="de50b-3649">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3649">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="de50b-3650">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3650">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-3651">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3651">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="de50b-3652">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3652">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-3653">public int visibleCols(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3653">public int visibleCols(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3654">public AutoMode visibleColsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3654">public AutoMode visibleColsMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3655">public int visibleColsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3655">public int visibleColsValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3656">public int visibleRows(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3656">public int visibleRows(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3657">public AutoMode visibleRowsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3657">public AutoMode visibleRowsMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3658">public int visibleRowsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3658">public int visibleRowsValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3659">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3659">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="de50b-3660">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3660">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="de50b-3661">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3661">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="de50b-3662">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3662">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="de50b-3663">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3663">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="de50b-3664">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3664">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="de50b-3665">public void cut()</span><span class="sxs-lookup"><span data-stu-id="de50b-3665">public void cut()</span></span>                                                                                                   | <span data-ttu-id="de50b-3666">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="de50b-3666">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="de50b-3667">public void applyQuickFilter(\[int controlId\], \[str filterValue\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3667">public void applyQuickFilter(\[int controlId\], \[str filterValue\])</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3668">public void autoSizeColumns(\[boolean autoSizeColumns\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3668">public void autoSizeColumns(\[boolean autoSizeColumns\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3669">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-3669">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="de50b-3670">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3670">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="de50b-3671">public void context()</span><span class="sxs-lookup"><span data-stu-id="de50b-3671">public void context()</span></span>                                                                                               | <span data-ttu-id="de50b-3672">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3672">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="de50b-3673">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="de50b-3673">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3674">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3674">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                           |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3675">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3675">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3676">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3676">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3677">public void copy()</span><span class="sxs-lookup"><span data-stu-id="de50b-3677">public void copy()</span></span>                                                                                                  | <span data-ttu-id="de50b-3678">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="de50b-3678">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="de50b-3679">public void enter()</span><span class="sxs-lookup"><span data-stu-id="de50b-3679">public void enter()</span></span>                                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3680">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="de50b-3680">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="de50b-3681">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3681">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="de50b-3682">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="de50b-3682">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="de50b-3683">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3683">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="de50b-3684">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3684">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3685">public void paste()</span><span class="sxs-lookup"><span data-stu-id="de50b-3685">public void paste()</span></span>                                                                                                 | <span data-ttu-id="de50b-3686">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3686">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-3687">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="de50b-3687">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="de50b-3688">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="de50b-3688">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="de50b-3689">public void quickFilterProvider(\[GridQuickFilterProvider quickFilterProvider\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3689">public void quickFilterProvider(\[GridQuickFilterProvider quickFilterProvider\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3690">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="de50b-3690">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="de50b-3691">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3691">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="de50b-3692">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3692">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3693">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="de50b-3693">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="de50b-3694">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3694">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="de50b-3695">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3695">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3696">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="de50b-3696">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="de50b-3697">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3697">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="de50b-3698">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="de50b-3698">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="de50b-3699">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3699">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="de50b-3700">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="de50b-3700">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3701">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-3701">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="de50b-3702">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3702">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="de50b-3703">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="de50b-3703">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="de50b-3704">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3704">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="de50b-3705">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="de50b-3705">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="de50b-3706">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-3706">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="de50b-3707">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3707">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="de50b-3708">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="de50b-3708">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="de50b-3709">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3709">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="de50b-3710">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="de50b-3710">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="de50b-3711">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3711">Sets the focus on the control.</span></span>                                                                                                                                          |

### <a name="method-activebackcolor"></a><span data-ttu-id="de50b-3712">メソッド activeBackColor</span><span class="sxs-lookup"><span data-stu-id="de50b-3712">Method activeBackColor</span></span>

    public int activeBackColor([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3713">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3713">Parameters</span></span>

<span data-ttu-id="de50b-3714">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3714">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3715">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3715">Return Value</span></span>

### <a name="method-activeforecolor"></a><span data-ttu-id="de50b-3716">メソッド activeForeColor</span><span class="sxs-lookup"><span data-stu-id="de50b-3716">Method activeForeColor</span></span>

    public int activeForeColor([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3717">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3717">Parameters</span></span>

<span data-ttu-id="de50b-3718">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3718">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3719">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3719">Return Value</span></span>

### <a name="method-addcontrol"></a><span data-ttu-id="de50b-3720">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="de50b-3720">Method addControl</span></span>

    public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a><span data-ttu-id="de50b-3721">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3721">Parameters</span></span>

<span data-ttu-id="de50b-3722">controlType</span><span class="sxs-lookup"><span data-stu-id="de50b-3722">controlType</span></span>  

<!-- -->

<span data-ttu-id="de50b-3723">controlName</span><span class="sxs-lookup"><span data-stu-id="de50b-3723">controlName</span></span>  

<!-- -->

<span data-ttu-id="de50b-3724">insertAfter</span><span class="sxs-lookup"><span data-stu-id="de50b-3724">insertAfter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3725">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3725">Return Value</span></span>

### <a name="method-addcontrolex"></a><span data-ttu-id="de50b-3726">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="de50b-3726">Method addControlEx</span></span>

    public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a><span data-ttu-id="de50b-3727">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3727">Parameters</span></span>

<span data-ttu-id="de50b-3728">controlClass</span><span class="sxs-lookup"><span data-stu-id="de50b-3728">controlClass</span></span>  

<!-- -->

<span data-ttu-id="de50b-3729">controlName</span><span class="sxs-lookup"><span data-stu-id="de50b-3729">controlName</span></span>  

<!-- -->

<span data-ttu-id="de50b-3730">insertAfter</span><span class="sxs-lookup"><span data-stu-id="de50b-3730">insertAfter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3731">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3731">Return Value</span></span>

### <a name="method-adddatafield"></a><span data-ttu-id="de50b-3732">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="de50b-3732">Method addDataField</span></span>

    public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="de50b-3733">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3733">Parameters</span></span>

<span data-ttu-id="de50b-3734">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="de50b-3734">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="de50b-3735">fieldId</span><span class="sxs-lookup"><span data-stu-id="de50b-3735">fieldId</span></span>  

<!-- -->

<span data-ttu-id="de50b-3736">insertAfter</span><span class="sxs-lookup"><span data-stu-id="de50b-3736">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="de50b-3737">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="de50b-3737">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3738">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3738">Return Value</span></span>

### <a name="method-aligncontrol"></a><span data-ttu-id="de50b-3739">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="de50b-3739">Method alignControl</span></span>

<span data-ttu-id="de50b-3740">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3740">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3741">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3741">Parameters</span></span>

<span data-ttu-id="de50b-3742">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3742">value</span></span>  
<span data-ttu-id="de50b-3743">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3743">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3744">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3744">Return Value</span></span>

<span data-ttu-id="de50b-3745">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-3745">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3746">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3746">Remarks</span></span>

<span data-ttu-id="de50b-3747">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3747">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="de50b-3748">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="de50b-3748">Method allowEdit</span></span>

<span data-ttu-id="de50b-3749">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3749">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3750">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3750">Parameters</span></span>

<span data-ttu-id="de50b-3751">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3751">value</span></span>  
<span data-ttu-id="de50b-3752">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3752">The value to assign to the allowEdit property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3753">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3753">Return Value</span></span>

<span data-ttu-id="de50b-3754">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-3754">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3755">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3755">Remarks</span></span>

<span data-ttu-id="de50b-3756">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="de50b-3756">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="de50b-3757">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="de50b-3757">Method allowSysSetup</span></span>

<span data-ttu-id="de50b-3758">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3758">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="de50b-3759">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3759">Return Value</span></span>

<span data-ttu-id="de50b-3760">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-3760">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-alternaterowshading"></a><span data-ttu-id="de50b-3761">メソッド alternateRowShading</span><span class="sxs-lookup"><span data-stu-id="de50b-3761">Method alternateRowShading</span></span>

    public int alternateRowShading([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3762">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3762">Parameters</span></span>

<span data-ttu-id="de50b-3763">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3763">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3764">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3764">Return Value</span></span>

### <a name="method-autodatagroup"></a><span data-ttu-id="de50b-3765">メソッド autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="de50b-3765">Method autoDataGroup</span></span>

    public boolean autoDataGroup([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3766">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3766">Parameters</span></span>

<span data-ttu-id="de50b-3767">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3767">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3768">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3768">Return Value</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="de50b-3769">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="de50b-3769">Method autoDeclaration</span></span>

<span data-ttu-id="de50b-3770">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3770">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3771">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3771">Parameters</span></span>

<span data-ttu-id="de50b-3772">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3772">value</span></span>  
<span data-ttu-id="de50b-3773">プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3773">The value to assign to the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3774">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3774">Return Value</span></span>

<span data-ttu-id="de50b-3775">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-3775">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3776">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3776">Remarks</span></span>

<span data-ttu-id="de50b-3777">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3777">Controls cannot have identical names.</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="de50b-3778">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="de50b-3778">Method backgroundColor</span></span>

<span data-ttu-id="de50b-3779">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3779">Gets or sets the background color of the control.</span></span>

    public int backgroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3780">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3780">Parameters</span></span>

<span data-ttu-id="de50b-3781">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3781">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3782">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3782">Return Value</span></span>

<span data-ttu-id="de50b-3783">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-3783">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3784">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3784">Remarks</span></span>

<span data-ttu-id="de50b-3785">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3785">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="de50b-3786">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de50b-3786">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="de50b-3787">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="de50b-3787">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="de50b-3788">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="de50b-3788">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="de50b-3789">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3789">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="de50b-3790">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3790">The maximum value for a single byte is 255.</span></span>

### <a name="method-backstyle"></a><span data-ttu-id="de50b-3791">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="de50b-3791">Method backStyle</span></span>

<span data-ttu-id="de50b-3792">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3792">Determines whether the control background can be transparent.</span></span>

    public int backStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3793">Parameters</span></span>

<span data-ttu-id="de50b-3794">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3794">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3795">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3795">Return Value</span></span>

<span data-ttu-id="de50b-3796">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3796">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="de50b-3797">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="de50b-3797">Method beginDrag</span></span>

<span data-ttu-id="de50b-3798">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3798">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-3799">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3799">Parameters</span></span>

<span data-ttu-id="de50b-3800">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3800">x</span></span>  
<span data-ttu-id="de50b-3801">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3801">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="de50b-3802">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-3802">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="de50b-3803">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3803">y</span></span>  
<span data-ttu-id="de50b-3804">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3804">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="de50b-3805">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="de50b-3805">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3806">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3806">Return Value</span></span>

<span data-ttu-id="de50b-3807">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3807">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3808">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3808">Remarks</span></span>

<span data-ttu-id="de50b-3809">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3809">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="de50b-3810">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3810">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-border"></a><span data-ttu-id="de50b-3811">メソッド border</span><span class="sxs-lookup"><span data-stu-id="de50b-3811">Method border</span></span>

<span data-ttu-id="de50b-3812">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3812">Gets or sets the style of the borderline of the control.</span></span>

    public int border([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3813">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3813">Parameters</span></span>

<span data-ttu-id="de50b-3814">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3814">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3815">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3815">Return Value</span></span>

<span data-ttu-id="de50b-3816">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-3816">An integer between zero and four, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3817">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3817">Remarks</span></span>

<span data-ttu-id="de50b-3818">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3818">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="de50b-3819">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3819">Value.</span></span> | <span data-ttu-id="de50b-3820">説明。</span><span class="sxs-lookup"><span data-stu-id="de50b-3820">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="de50b-3821">0</span><span class="sxs-lookup"><span data-stu-id="de50b-3821">0</span></span>      | <span data-ttu-id="de50b-3822">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-3822">Auto.</span></span>        |
| <span data-ttu-id="de50b-3823">1</span><span class="sxs-lookup"><span data-stu-id="de50b-3823">1</span></span>      | <span data-ttu-id="de50b-3824">3D。</span><span class="sxs-lookup"><span data-stu-id="de50b-3824">3D.</span></span>          |
| <span data-ttu-id="de50b-3825">2</span><span class="sxs-lookup"><span data-stu-id="de50b-3825">2</span></span>      | <span data-ttu-id="de50b-3826">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="de50b-3826">Single line.</span></span> |
| <span data-ttu-id="de50b-3827">3</span><span class="sxs-lookup"><span data-stu-id="de50b-3827">3</span></span>      | <span data-ttu-id="de50b-3828">均一。</span><span class="sxs-lookup"><span data-stu-id="de50b-3828">Flat.</span></span>        |
| <span data-ttu-id="de50b-3829">4</span><span class="sxs-lookup"><span data-stu-id="de50b-3829">4</span></span>      | <span data-ttu-id="de50b-3830">なし。</span><span class="sxs-lookup"><span data-stu-id="de50b-3830">None.</span></span>        |

### <a name="method-bottommargin"></a><span data-ttu-id="de50b-3831">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="de50b-3831">Method bottomMargin</span></span>

    public int bottomMargin([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3832">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3832">Parameters</span></span>

<span data-ttu-id="de50b-3833">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3833">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3834">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3834">Return Value</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="de50b-3835">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="de50b-3835">Method calcControlSize</span></span>

<span data-ttu-id="de50b-3836">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3836">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="de50b-3837">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3837">Parameters</span></span>

<span data-ttu-id="de50b-3838">chars</span><span class="sxs-lookup"><span data-stu-id="de50b-3838">chars</span></span>  
<span data-ttu-id="de50b-3839">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="de50b-3839">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="de50b-3840">明細行</span><span class="sxs-lookup"><span data-stu-id="de50b-3840">lines</span></span>  
<span data-ttu-id="de50b-3841">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="de50b-3841">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3842">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3842">Return Value</span></span>

<span data-ttu-id="de50b-3843">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="de50b-3843">The container that holds the width and height.</span></span>

### <a name="method-canadddatafield"></a><span data-ttu-id="de50b-3844">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="de50b-3844">Method canAddDataField</span></span>

    public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="de50b-3845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3845">Parameters</span></span>

<span data-ttu-id="de50b-3846">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="de50b-3846">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="de50b-3847">fieldId</span><span class="sxs-lookup"><span data-stu-id="de50b-3847">fieldId</span></span>  

<!-- -->

<span data-ttu-id="de50b-3848">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="de50b-3848">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3849">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3849">Return Value</span></span>

### <a name="method-cancontain"></a><span data-ttu-id="de50b-3850">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="de50b-3850">Method canContain</span></span>

    public boolean canContain(FormControl control)

#### <a name="parameters"></a><span data-ttu-id="de50b-3851">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3851">Parameters</span></span>

<span data-ttu-id="de50b-3852">control</span><span class="sxs-lookup"><span data-stu-id="de50b-3852">control</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3853">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3853">Return Value</span></span>

### <a name="method-colorscheme"></a><span data-ttu-id="de50b-3854">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="de50b-3854">Method colorScheme</span></span>

<span data-ttu-id="de50b-3855">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3855">Gets or sets the color scheme of the control.</span></span>

    public int colorScheme([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3856">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3856">Parameters</span></span>

<span data-ttu-id="de50b-3857">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3857">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3858">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3858">Return Value</span></span>

<span data-ttu-id="de50b-3859">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="de50b-3859">An integer between zero and two, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3860">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3860">Remarks</span></span>

<span data-ttu-id="de50b-3861">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3861">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="de50b-3862">値です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3862">Value.</span></span> | <span data-ttu-id="de50b-3863">スタイル。</span><span class="sxs-lookup"><span data-stu-id="de50b-3863">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="de50b-3864">0</span><span class="sxs-lookup"><span data-stu-id="de50b-3864">0</span></span>      | <span data-ttu-id="de50b-3865">既定。</span><span class="sxs-lookup"><span data-stu-id="de50b-3865">Default.</span></span>                      |
| <span data-ttu-id="de50b-3866">1</span><span class="sxs-lookup"><span data-stu-id="de50b-3866">1</span></span>      | <span data-ttu-id="de50b-3867">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="de50b-3867">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="de50b-3868">2</span><span class="sxs-lookup"><span data-stu-id="de50b-3868">2</span></span>      | <span data-ttu-id="de50b-3869">真の配色。</span><span class="sxs-lookup"><span data-stu-id="de50b-3869">The true-color scheme.</span></span>        |

### <a name="method-configurationkey"></a><span data-ttu-id="de50b-3870">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="de50b-3870">Method configurationKey</span></span>

<span data-ttu-id="de50b-3871">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3871">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3872">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3872">Parameters</span></span>

<span data-ttu-id="de50b-3873">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3873">value</span></span>  
<span data-ttu-id="de50b-3874">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3874">The ID of the configuration key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3875">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3875">Return Value</span></span>

<span data-ttu-id="de50b-3876">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-3876">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3877">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3877">Remarks</span></span>

<span data-ttu-id="de50b-3878">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3878">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="de50b-3879">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3879">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="de50b-3880">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="de50b-3880">Method configurationKeyEx</span></span>

<span data-ttu-id="de50b-3881">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3881">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="de50b-3882">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3882">Return Value</span></span>

<span data-ttu-id="de50b-3883">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="de50b-3883">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3884">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3884">Remarks</span></span>

<span data-ttu-id="de50b-3885">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="de50b-3885">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="de50b-3886">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3886">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="de50b-3887">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3887">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-contains"></a><span data-ttu-id="de50b-3888">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="de50b-3888">Method contains</span></span>

    public boolean contains(FormControl control)

#### <a name="parameters"></a><span data-ttu-id="de50b-3889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3889">Parameters</span></span>

<span data-ttu-id="de50b-3890">control</span><span class="sxs-lookup"><span data-stu-id="de50b-3890">control</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3891">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3891">Return Value</span></span>

### <a name="method-controlcount"></a><span data-ttu-id="de50b-3892">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="de50b-3892">Method controlCount</span></span>

    public int controlCount()

#### <a name="return-value"></a><span data-ttu-id="de50b-3893">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3893">Return Value</span></span>

### <a name="method-controlnum"></a><span data-ttu-id="de50b-3894">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="de50b-3894">Method controlNum</span></span>

    public FormControl controlNum(int controlNo)

#### <a name="parameters"></a><span data-ttu-id="de50b-3895">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3895">Parameters</span></span>

<span data-ttu-id="de50b-3896">controlNo</span><span class="sxs-lookup"><span data-stu-id="de50b-3896">controlNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3897">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3897">Return Value</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="de50b-3898">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="de50b-3898">Method countryRegionCodes</span></span>

<span data-ttu-id="de50b-3899">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3899">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3900">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3900">Parameters</span></span>

<span data-ttu-id="de50b-3901">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3901">value</span></span>  
<span data-ttu-id="de50b-3902">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3902">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3903">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3903">Return Value</span></span>

<span data-ttu-id="de50b-3904">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-3904">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-countryregioncontextfield"></a><span data-ttu-id="de50b-3905">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="de50b-3905">Method countryRegionContextField</span></span>

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3906">Parameters</span></span>

<span data-ttu-id="de50b-3907">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3907">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3908">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3908">Return Value</span></span>

### <a name="method-datagroup"></a><span data-ttu-id="de50b-3909">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="de50b-3909">Method dataGroup</span></span>

    public str dataGroup([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3910">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3910">Parameters</span></span>

<span data-ttu-id="de50b-3911">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3911">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3912">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3912">Return Value</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="de50b-3913">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="de50b-3913">Method dataRelationPath</span></span>

<span data-ttu-id="de50b-3914">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3914">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3915">Parameters</span></span>

<span data-ttu-id="de50b-3916">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3916">value</span></span>  
<span data-ttu-id="de50b-3917">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-3917">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3918">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3918">Return Value</span></span>

<span data-ttu-id="de50b-3919">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="de50b-3919">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3920">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3920">Remarks</span></span>

<span data-ttu-id="de50b-3921">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3921">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="de50b-3922">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="de50b-3922">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-datasource"></a><span data-ttu-id="de50b-3923">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="de50b-3923">Method dataSource</span></span>

<span data-ttu-id="de50b-3924">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3924">Gets or sets a data source to be used by the control or the form.</span></span>

    public int dataSource([AnyType value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3925">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3925">Parameters</span></span>

<span data-ttu-id="de50b-3926">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3926">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3927">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3927">Return Value</span></span>

<span data-ttu-id="de50b-3928">使用する必要のあるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-3928">The identifier of the data source that must be used.</span></span>

### <a name="method-defaultaction"></a><span data-ttu-id="de50b-3929">メソッド defaultAction</span><span class="sxs-lookup"><span data-stu-id="de50b-3929">Method defaultAction</span></span>

    public str defaultAction([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3930">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3930">Parameters</span></span>

<span data-ttu-id="de50b-3931">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3931">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3932">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3932">Return Value</span></span>

### <a name="method-defaultactionlabel"></a><span data-ttu-id="de50b-3933">メソッド defaultActionLabel</span><span class="sxs-lookup"><span data-stu-id="de50b-3933">Method defaultActionLabel</span></span>

    public str defaultActionLabel([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3934">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3934">Parameters</span></span>

<span data-ttu-id="de50b-3935">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3935">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3936">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3936">Return Value</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="de50b-3937">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="de50b-3937">Method displayTarget</span></span>

<span data-ttu-id="de50b-3938">クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3938">Gets or sets the value that indicates whether the control is displayed in the  client, in Enterprise Portal, Finance and Operations, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3939">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3939">Parameters</span></span>

<span data-ttu-id="de50b-3940">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3940">value</span></span>  
<span data-ttu-id="de50b-3941">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3941">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3942">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3942">Return Value</span></span>

<span data-ttu-id="de50b-3943">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3943">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="de50b-3944">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="de50b-3944">Method dragDrop</span></span>

<span data-ttu-id="de50b-3945">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3945">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3946">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3946">Parameters</span></span>

<span data-ttu-id="de50b-3947">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3947">value</span></span>  
<span data-ttu-id="de50b-3948">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3948">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3949">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3949">Return Value</span></span>

<span data-ttu-id="de50b-3950">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="de50b-3950">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3951">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3951">Remarks</span></span>

<span data-ttu-id="de50b-3952">dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3952">Use the dragLeave Method, dragOver Method, and dragOverEx Method methods to specify the behavior.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="de50b-3953">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="de50b-3953">Method dragOver</span></span>

<span data-ttu-id="de50b-3954">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3954">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-3955">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3955">Parameters</span></span>

<span data-ttu-id="de50b-3956">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-3956">dragSource</span></span>  
<span data-ttu-id="de50b-3957">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3957">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3958">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-3958">dragMode</span></span>  
<span data-ttu-id="de50b-3959">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3959">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3960">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3960">x</span></span>  
<span data-ttu-id="de50b-3961">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3961">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3962">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3962">y</span></span>  
<span data-ttu-id="de50b-3963">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3963">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3964">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3964">Return Value</span></span>

<span data-ttu-id="de50b-3965">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3965">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="de50b-3966">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="de50b-3966">Method dragOverEx</span></span>

<span data-ttu-id="de50b-3967">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3967">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-3968">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3968">Parameters</span></span>

<span data-ttu-id="de50b-3969">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-3969">dragSource</span></span>  
<span data-ttu-id="de50b-3970">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3970">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3971">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-3971">dragMode</span></span>  
<span data-ttu-id="de50b-3972">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3972">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3973">x</span><span class="sxs-lookup"><span data-stu-id="de50b-3973">x</span></span>  
<span data-ttu-id="de50b-3974">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3974">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-3975">y</span><span class="sxs-lookup"><span data-stu-id="de50b-3975">y</span></span>  
<span data-ttu-id="de50b-3976">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3976">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3977">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3977">Return Value</span></span>

<span data-ttu-id="de50b-3978">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="de50b-3978">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="de50b-3979">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="de50b-3979">Method dragText</span></span>

<span data-ttu-id="de50b-3980">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3980">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="de50b-3981">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3981">Return Value</span></span>

<span data-ttu-id="de50b-3982">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-3982">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="de50b-3983">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="de50b-3983">Method enabled</span></span>

<span data-ttu-id="de50b-3984">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-3984">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3985">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3985">Parameters</span></span>

<span data-ttu-id="de50b-3986">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3986">value</span></span>  
<span data-ttu-id="de50b-3987">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-3987">A Boolean value that indicates whether the control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-3988">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3988">Return Value</span></span>

<span data-ttu-id="de50b-3989">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-3989">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-3990">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-3990">Remarks</span></span>

<span data-ttu-id="de50b-3991">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3991">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="de50b-3992">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3992">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="de50b-3993">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-3993">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-exportallowed"></a><span data-ttu-id="de50b-3994">メソッド exportAllowed</span><span class="sxs-lookup"><span data-stu-id="de50b-3994">Method exportAllowed</span></span>

    public boolean exportAllowed([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3995">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3995">Parameters</span></span>

<span data-ttu-id="de50b-3996">値</span><span class="sxs-lookup"><span data-stu-id="de50b-3996">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-3997">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-3997">Return Value</span></span>

### <a name="method-exportlabel"></a><span data-ttu-id="de50b-3998">メソッド exportLabel</span><span class="sxs-lookup"><span data-stu-id="de50b-3998">Method exportLabel</span></span>

    public str exportLabel([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-3999">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-3999">Parameters</span></span>

<span data-ttu-id="de50b-4000">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4000">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4001">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4001">Return Value</span></span>

### <a name="method-getlinedata"></a><span data-ttu-id="de50b-4002">メソッド getLineData</span><span class="sxs-lookup"><span data-stu-id="de50b-4002">Method getLineData</span></span>

    public Struct getLineData(int lineNumber)

#### <a name="parameters"></a><span data-ttu-id="de50b-4003">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4003">Parameters</span></span>

<span data-ttu-id="de50b-4004">lineNumber</span><span class="sxs-lookup"><span data-stu-id="de50b-4004">lineNumber</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4005">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4005">Return Value</span></span>

### <a name="method-getselecteddata"></a><span data-ttu-id="de50b-4006">メソッド getSelectedData</span><span class="sxs-lookup"><span data-stu-id="de50b-4006">Method getSelectedData</span></span>

    public Struct getSelectedData()

#### <a name="return-value"></a><span data-ttu-id="de50b-4007">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4007">Return Value</span></span>

### <a name="method-gridlines"></a><span data-ttu-id="de50b-4008">メソッド gridLines</span><span class="sxs-lookup"><span data-stu-id="de50b-4008">Method gridLines</span></span>

    public boolean gridLines([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4009">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4009">Parameters</span></span>

<span data-ttu-id="de50b-4010">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4010">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4011">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4011">Return Value</span></span>

### <a name="method-gridlinesstyle"></a><span data-ttu-id="de50b-4012">メソッド gridLinesStyle</span><span class="sxs-lookup"><span data-stu-id="de50b-4012">Method gridLinesStyle</span></span>

    public int gridLinesStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4013">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4013">Parameters</span></span>

<span data-ttu-id="de50b-4014">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4014">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4015">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4015">Return Value</span></span>

### <a name="method-groupby"></a><span data-ttu-id="de50b-4016">メソッド groupBy</span><span class="sxs-lookup"><span data-stu-id="de50b-4016">Method groupBy</span></span>

    public str groupBy([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4017">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4017">Parameters</span></span>

<span data-ttu-id="de50b-4018">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4018">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4019">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4019">Return Value</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="de50b-4020">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="de50b-4020">Method hasChanged</span></span>

<span data-ttu-id="de50b-4021">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4021">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="de50b-4022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4022">Parameters</span></span>

<span data-ttu-id="de50b-4023">val</span><span class="sxs-lookup"><span data-stu-id="de50b-4023">val</span></span>  
<span data-ttu-id="de50b-4024">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4024">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4025">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4025">Return Value</span></span>

<span data-ttu-id="de50b-4026">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-4026">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="de50b-4027">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="de50b-4027">Method hasUserSetting</span></span>

<span data-ttu-id="de50b-4028">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4028">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="de50b-4029">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4029">Return Value</span></span>

<span data-ttu-id="de50b-4030">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-4030">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="de50b-4031">メソッド height</span><span class="sxs-lookup"><span data-stu-id="de50b-4031">Method height</span></span>

<span data-ttu-id="de50b-4032">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4032">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4033">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4033">Parameters</span></span>

<span data-ttu-id="de50b-4034">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4034">value</span></span>  
<span data-ttu-id="de50b-4035">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4035">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-4036">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4036">mode</span></span>  
<span data-ttu-id="de50b-4037">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4037">An integer that indicates how the height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4038">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4038">Return Value</span></span>

<span data-ttu-id="de50b-4039">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-4039">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4040">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4040">Remarks</span></span>

<span data-ttu-id="de50b-4041">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4041">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="de50b-4042">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-4042">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="de50b-4043">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-4043">Mode.</span></span>            | <span data-ttu-id="de50b-4044">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-4044">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-4045">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-4045">-1 Exact.</span></span>        | <span data-ttu-id="de50b-4046">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4046">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-4047">0 自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-4047">0 Auto.</span></span>          | <span data-ttu-id="de50b-4048">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4048">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-4049">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-4049">1 Column height.</span></span> | <span data-ttu-id="de50b-4050">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4050">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="de50b-4051">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4051">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="de50b-4052">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4052">Method heightMode</span></span>

<span data-ttu-id="de50b-4053">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4053">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4054">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4054">Parameters</span></span>

<span data-ttu-id="de50b-4055">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4055">value</span></span>  
<span data-ttu-id="de50b-4056">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4056">An integer value that indicates how control height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4057">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4057">Return Value</span></span>

<span data-ttu-id="de50b-4058">計算モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-4058">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4059">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4059">Remarks</span></span>

<span data-ttu-id="de50b-4060">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-4060">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="de50b-4061">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-4061">Mode.</span></span>          | <span data-ttu-id="de50b-4062">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-4062">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-4063">正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-4063">Exact.</span></span>         | <span data-ttu-id="de50b-4064">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4064">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-4065">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-4065">Auto.</span></span>          | <span data-ttu-id="de50b-4066">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4066">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-4067">列の高さ</span><span class="sxs-lookup"><span data-stu-id="de50b-4067">Column height.</span></span> | <span data-ttu-id="de50b-4068">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4068">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="de50b-4069">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4069">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="de50b-4070">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="de50b-4070">Method heightValue</span></span>

<span data-ttu-id="de50b-4071">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4071">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4072">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4072">Parameters</span></span>

<span data-ttu-id="de50b-4073">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4073">value</span></span>  
<span data-ttu-id="de50b-4074">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4074">An Integer that specifies the height in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4075">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4075">Return Value</span></span>

<span data-ttu-id="de50b-4076">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-4076">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4077">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4077">Remarks</span></span>

<span data-ttu-id="de50b-4078">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4078">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="de50b-4079">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="de50b-4079">Method helpField</span></span>

<span data-ttu-id="de50b-4080">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4080">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="de50b-4081">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4081">Return Value</span></span>

<span data-ttu-id="de50b-4082">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-4082">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4083">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4083">Remarks</span></span>

<span data-ttu-id="de50b-4084">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4084">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="de50b-4085">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4085">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="de50b-4086">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="de50b-4086">Method helpText</span></span>

<span data-ttu-id="de50b-4087">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4087">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4088">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4088">Parameters</span></span>

<span data-ttu-id="de50b-4089">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4089">value</span></span>  
<span data-ttu-id="de50b-4090">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4090">The value that is assigned as the Help text for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4091">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4091">Return Value</span></span>

<span data-ttu-id="de50b-4092">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-4092">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4093">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4093">Remarks</span></span>

<span data-ttu-id="de50b-4094">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4094">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="de50b-4095">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4095">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="de50b-4096">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="de50b-4096">Method hierarchyParent</span></span>

<span data-ttu-id="de50b-4097">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4097">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4098">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4098">Parameters</span></span>

<span data-ttu-id="de50b-4099">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4099">value</span></span>  
<span data-ttu-id="de50b-4100">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4100">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4101">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4101">Return Value</span></span>

<span data-ttu-id="de50b-4102">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4102">The HierarchyParent property value of the control.</span></span>

### <a name="method-highlightactive"></a><span data-ttu-id="de50b-4103">メソッド highlightActive</span><span class="sxs-lookup"><span data-stu-id="de50b-4103">Method highlightActive</span></span>

    public boolean highlightActive([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4104">Parameters</span></span>

<span data-ttu-id="de50b-4105">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4105">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4106">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4106">Return Value</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="de50b-4107">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="de50b-4107">Method hWnd</span></span>

<span data-ttu-id="de50b-4108">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4108">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="de50b-4109">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4109">Return Value</span></span>

<span data-ttu-id="de50b-4110">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="de50b-4110">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4111">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4111">Remarks</span></span>

<span data-ttu-id="de50b-4112">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4112">The handle can be used with the Windows API.</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="de50b-4113">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="de50b-4113">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="de50b-4114">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4114">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="de50b-4115">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="de50b-4115">Method isDisplayed</span></span>

<span data-ttu-id="de50b-4116">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4116">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="de50b-4117">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4117">Return Value</span></span>

<span data-ttu-id="de50b-4118">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-4118">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4119">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4119">Remarks</span></span>

<span data-ttu-id="de50b-4120">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4120">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="de50b-4121">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="de50b-4121">Method isRestricted</span></span>

<span data-ttu-id="de50b-4122">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4122">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="de50b-4123">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4123">Return Value</span></span>

<span data-ttu-id="de50b-4124">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-4124">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="de50b-4125">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="de50b-4125">Method isUserSetupEnabled</span></span>

<span data-ttu-id="de50b-4126">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4126">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="de50b-4127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4127">Parameters</span></span>

<span data-ttu-id="de50b-4128">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="de50b-4128">neededSetupRights</span></span>  
<span data-ttu-id="de50b-4129">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4129">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4130">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4130">Return Value</span></span>

<span data-ttu-id="de50b-4131">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-4131">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="de50b-4132">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4132">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4133">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4133">Remarks</span></span>

<span data-ttu-id="de50b-4134">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4134">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-4135">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="de50b-4135">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="de50b-4136">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4136">No changes can be made to the control.</span></span> <span data-ttu-id="de50b-4137">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4137">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="de50b-4138">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="de50b-4138">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="de50b-4139">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4139">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="de50b-4140">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4140">The user cannot move the control.</span></span>   |
| <span data-ttu-id="de50b-4141">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="de50b-4141">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="de50b-4142">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4142">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="de50b-4143">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4143">The user can also move the control.</span></span> |

### <a name="method-leave"></a><span data-ttu-id="de50b-4144">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="de50b-4144">Method leave</span></span>

    public boolean leave()

#### <a name="return-value"></a><span data-ttu-id="de50b-4145">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4145">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="de50b-4146">メソッド left</span><span class="sxs-lookup"><span data-stu-id="de50b-4146">Method left</span></span>

<span data-ttu-id="de50b-4147">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4147">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4148">Parameters</span></span>

<span data-ttu-id="de50b-4149">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4149">value</span></span>  
<span data-ttu-id="de50b-4150">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4150">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-4151">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4151">mode</span></span>  
<span data-ttu-id="de50b-4152">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4152">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4153">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4153">Return Value</span></span>

<span data-ttu-id="de50b-4154">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-4154">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="de50b-4155">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="de50b-4155">Method leftMargin</span></span>

    public int leftMargin([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4156">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4156">Parameters</span></span>

<span data-ttu-id="de50b-4157">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4157">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4158">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4158">Return Value</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="de50b-4159">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4159">Method leftMode</span></span>

<span data-ttu-id="de50b-4160">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4160">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4161">Parameters</span></span>

<span data-ttu-id="de50b-4162">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4162">value</span></span>  
<span data-ttu-id="de50b-4163">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4163">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4164">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4164">Return Value</span></span>

<span data-ttu-id="de50b-4165">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-4165">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="de50b-4166">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="de50b-4166">Method leftValue</span></span>

<span data-ttu-id="de50b-4167">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4167">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4168">Parameters</span></span>

<span data-ttu-id="de50b-4169">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4169">value</span></span>  
<span data-ttu-id="de50b-4170">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4170">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4171">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4171">Return Value</span></span>

<span data-ttu-id="de50b-4172">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-4172">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="de50b-4173">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="de50b-4173">Method markAsUserAdd</span></span>

<span data-ttu-id="de50b-4174">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="de50b-4174">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4175">Parameters</span></span>

<span data-ttu-id="de50b-4176">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4176">value</span></span>  
<span data-ttu-id="de50b-4177">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4177">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4178">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4178">Return Value</span></span>

<span data-ttu-id="de50b-4179">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-4179">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-morerowsindicator"></a><span data-ttu-id="de50b-4180">メソッド moreRowsIndicator</span><span class="sxs-lookup"><span data-stu-id="de50b-4180">Method moreRowsIndicator</span></span>

    public int moreRowsIndicator([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4181">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4181">Parameters</span></span>

<span data-ttu-id="de50b-4182">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4182">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4183">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4183">Return Value</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="de50b-4184">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="de50b-4184">Method mouseDblClick</span></span>

<span data-ttu-id="de50b-4185">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4185">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-4186">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4186">Parameters</span></span>

<span data-ttu-id="de50b-4187">x</span><span class="sxs-lookup"><span data-stu-id="de50b-4187">x</span></span>  
<span data-ttu-id="de50b-4188">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4188">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4189">y</span><span class="sxs-lookup"><span data-stu-id="de50b-4189">y</span></span>  
<span data-ttu-id="de50b-4190">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4190">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4191">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-4191">button</span></span>  
<span data-ttu-id="de50b-4192">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4192">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4193">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-4193">Ctrl</span></span>  
<span data-ttu-id="de50b-4194">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4194">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4195">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-4195">Shift</span></span>  
<span data-ttu-id="de50b-4196">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4196">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4197">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4197">Return Value</span></span>

<span data-ttu-id="de50b-4198">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-4198">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4199">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4199">Remarks</span></span>

<span data-ttu-id="de50b-4200">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4200">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="de50b-4201">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="de50b-4201">Method mouseDown</span></span>

<span data-ttu-id="de50b-4202">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4202">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-4203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4203">Parameters</span></span>

<span data-ttu-id="de50b-4204">x</span><span class="sxs-lookup"><span data-stu-id="de50b-4204">x</span></span>  
<span data-ttu-id="de50b-4205">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4205">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4206">y</span><span class="sxs-lookup"><span data-stu-id="de50b-4206">y</span></span>  
<span data-ttu-id="de50b-4207">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4207">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4208">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-4208">button</span></span>  
<span data-ttu-id="de50b-4209">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4209">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4210">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-4210">Ctrl</span></span>  
<span data-ttu-id="de50b-4211">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4211">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4212">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-4212">Shift</span></span>  
<span data-ttu-id="de50b-4213">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4213">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4214">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4214">Return Value</span></span>

<span data-ttu-id="de50b-4215">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-4215">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4216">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4216">Remarks</span></span>

<span data-ttu-id="de50b-4217">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4217">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="de50b-4218">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4218">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="de50b-4219">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="de50b-4219">Method mouseMove</span></span>

<span data-ttu-id="de50b-4220">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4220">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-4221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4221">Parameters</span></span>

<span data-ttu-id="de50b-4222">x</span><span class="sxs-lookup"><span data-stu-id="de50b-4222">x</span></span>  
<span data-ttu-id="de50b-4223">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4223">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4224">y</span><span class="sxs-lookup"><span data-stu-id="de50b-4224">y</span></span>  
<span data-ttu-id="de50b-4225">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4225">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4226">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-4226">button</span></span>  
<span data-ttu-id="de50b-4227">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4227">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4228">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-4228">Ctrl</span></span>  
<span data-ttu-id="de50b-4229">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4229">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4230">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-4230">Shift</span></span>  
<span data-ttu-id="de50b-4231">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4231">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4232">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4232">Return Value</span></span>

<span data-ttu-id="de50b-4233">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-4233">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4234">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4234">Remarks</span></span>

<span data-ttu-id="de50b-4235">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4235">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="de50b-4236">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="de50b-4236">Method mouseUp</span></span>

<span data-ttu-id="de50b-4237">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4237">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-4238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4238">Parameters</span></span>

<span data-ttu-id="de50b-4239">x</span><span class="sxs-lookup"><span data-stu-id="de50b-4239">x</span></span>  
<span data-ttu-id="de50b-4240">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4240">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4241">y</span><span class="sxs-lookup"><span data-stu-id="de50b-4241">y</span></span>  
<span data-ttu-id="de50b-4242">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4242">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4243">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-4243">button</span></span>  
<span data-ttu-id="de50b-4244">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4244">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4245">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-4245">Ctrl</span></span>  
<span data-ttu-id="de50b-4246">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4246">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4247">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-4247">Shift</span></span>  
<span data-ttu-id="de50b-4248">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4248">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4249">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4249">Return Value</span></span>

<span data-ttu-id="de50b-4250">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="de50b-4250">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4251">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4251">Remarks</span></span>

<span data-ttu-id="de50b-4252">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4252">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="de50b-4253">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4253">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-movecontrol"></a><span data-ttu-id="de50b-4254">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="de50b-4254">Method moveControl</span></span>

    public int moveControl(int controlId, [int insertAfterId])

#### <a name="parameters"></a><span data-ttu-id="de50b-4255">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4255">Parameters</span></span>

<span data-ttu-id="de50b-4256">controlId</span><span class="sxs-lookup"><span data-stu-id="de50b-4256">controlId</span></span>  

<!-- -->

<span data-ttu-id="de50b-4257">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="de50b-4257">insertAfterId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4258">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4258">Return Value</span></span>

### <a name="method-multiselect"></a><span data-ttu-id="de50b-4259">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="de50b-4259">Method multiSelect</span></span>

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4260">Parameters</span></span>

<span data-ttu-id="de50b-4261">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4261">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4262">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4262">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="de50b-4263">メソッド名</span><span class="sxs-lookup"><span data-stu-id="de50b-4263">Method name</span></span>

<span data-ttu-id="de50b-4264">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4264">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4265">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4265">Parameters</span></span>

<span data-ttu-id="de50b-4266">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4266">value</span></span>  
<span data-ttu-id="de50b-4267">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-4267">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4268">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4268">Return Value</span></span>

<span data-ttu-id="de50b-4269">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="de50b-4269">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4270">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4270">Remarks</span></span>

<span data-ttu-id="de50b-4271">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4271">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="de50b-4272">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4272">It must begin with a letter.</span></span>
-   <span data-ttu-id="de50b-4273">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4273">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="de50b-4274">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4274">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="de50b-4275">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4275">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="de50b-4276">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4276">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="de50b-4277">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="de50b-4277">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4278">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4278">Parameters</span></span>

<span data-ttu-id="de50b-4279">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4279">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4280">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4280">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="de50b-4281">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="de50b-4281">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="de50b-4282">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4282">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="de50b-4283">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="de50b-4283">Method parentControl</span></span>

<span data-ttu-id="de50b-4284">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4284">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="de50b-4285">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4285">Return Value</span></span>

<span data-ttu-id="de50b-4286">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="de50b-4286">The parent control for the control.</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="de50b-4287">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="de50b-4287">Method rightMargin</span></span>

    public int rightMargin([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4288">Parameters</span></span>

<span data-ttu-id="de50b-4289">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4289">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4290">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4290">Return Value</span></span>

### <a name="method-scrollbars"></a><span data-ttu-id="de50b-4291">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="de50b-4291">Method scrollbars</span></span>

    public int scrollbars([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4292">Parameters</span></span>

<span data-ttu-id="de50b-4293">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4293">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4294">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4294">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="de50b-4295">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="de50b-4295">Method securityKey</span></span>

<span data-ttu-id="de50b-4296">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4296">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4297">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4297">Parameters</span></span>

<span data-ttu-id="de50b-4298">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4298">value</span></span>  
<span data-ttu-id="de50b-4299">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4299">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4300">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4300">Return Value</span></span>

<span data-ttu-id="de50b-4301">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4301">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-showcollabels"></a><span data-ttu-id="de50b-4302">メソッド showColLabels</span><span class="sxs-lookup"><span data-stu-id="de50b-4302">Method showColLabels</span></span>

    public boolean showColLabels([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4303">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4303">Parameters</span></span>

<span data-ttu-id="de50b-4304">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4304">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4305">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4305">Return Value</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="de50b-4306">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="de50b-4306">Method showContextMenu</span></span>

<span data-ttu-id="de50b-4307">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4307">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="de50b-4308">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4308">Parameters</span></span>

<span data-ttu-id="de50b-4309">menuHandle</span><span class="sxs-lookup"><span data-stu-id="de50b-4309">menuHandle</span></span>  
<span data-ttu-id="de50b-4310">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="de50b-4310">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4311">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4311">Return Value</span></span>

<span data-ttu-id="de50b-4312">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4312">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-showrowlabels"></a><span data-ttu-id="de50b-4313">メソッド showRowLabels</span><span class="sxs-lookup"><span data-stu-id="de50b-4313">Method showRowLabels</span></span>

    public boolean showRowLabels([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4314">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4314">Parameters</span></span>

<span data-ttu-id="de50b-4315">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4315">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4316">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4316">Return Value</span></span>

### <a name="method-skip"></a><span data-ttu-id="de50b-4317">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="de50b-4317">Method skip</span></span>

<span data-ttu-id="de50b-4318">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4318">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4319">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4319">Parameters</span></span>

<span data-ttu-id="de50b-4320">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4320">value</span></span>  
<span data-ttu-id="de50b-4321">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4321">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4322">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4322">Return Value</span></span>

<span data-ttu-id="de50b-4323">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="de50b-4323">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="method-sort"></a><span data-ttu-id="de50b-4324">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="de50b-4324">Method sort</span></span>

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a><span data-ttu-id="de50b-4325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4325">Parameters</span></span>

<span data-ttu-id="de50b-4326">sortDirection</span><span class="sxs-lookup"><span data-stu-id="de50b-4326">sortDirection</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4327">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4327">Return Value</span></span>

### <a name="method-style"></a><span data-ttu-id="de50b-4328">メソッド style</span><span class="sxs-lookup"><span data-stu-id="de50b-4328">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4329">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4329">Parameters</span></span>

<span data-ttu-id="de50b-4330">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4330">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4331">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4331">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="de50b-4332">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="de50b-4332">Method toolTip</span></span>

<span data-ttu-id="de50b-4333">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4333">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="de50b-4334">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4334">Return Value</span></span>

<span data-ttu-id="de50b-4335">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="de50b-4335">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4336">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4336">Remarks</span></span>

<span data-ttu-id="de50b-4337">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4337">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="de50b-4338">メソッド top</span><span class="sxs-lookup"><span data-stu-id="de50b-4338">Method top</span></span>

<span data-ttu-id="de50b-4339">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4339">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4340">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4340">Parameters</span></span>

<span data-ttu-id="de50b-4341">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4341">value</span></span>  
<span data-ttu-id="de50b-4342">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4342">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-4343">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4343">mode</span></span>  
<span data-ttu-id="de50b-4344">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4344">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4345">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4345">Return Value</span></span>

<span data-ttu-id="de50b-4346">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-4346">The vertical position of the control in the form.</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="de50b-4347">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="de50b-4347">Method topMargin</span></span>

    public int topMargin([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4348">Parameters</span></span>

<span data-ttu-id="de50b-4349">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4349">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4350">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4350">Return Value</span></span>

### <a name="method-topmode"></a><span data-ttu-id="de50b-4351">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4351">Method topMode</span></span>

<span data-ttu-id="de50b-4352">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4352">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4353">Parameters</span></span>

<span data-ttu-id="de50b-4354">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4354">value</span></span>  
<span data-ttu-id="de50b-4355">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4355">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4356">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4356">Return Value</span></span>

<span data-ttu-id="de50b-4357">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-4357">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="de50b-4358">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="de50b-4358">Method topValue</span></span>

<span data-ttu-id="de50b-4359">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4359">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4360">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4360">Parameters</span></span>

<span data-ttu-id="de50b-4361">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4361">value</span></span>  
<span data-ttu-id="de50b-4362">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4362">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4363">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4363">Return Value</span></span>

<span data-ttu-id="de50b-4364">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="de50b-4364">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="de50b-4365">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="de50b-4365">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4366">Parameters</span></span>

<span data-ttu-id="de50b-4367">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4368">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4368">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="de50b-4369">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="de50b-4369">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="de50b-4370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4370">Parameters</span></span>

<span data-ttu-id="de50b-4371">データ</span><span class="sxs-lookup"><span data-stu-id="de50b-4371">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4372">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4372">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="de50b-4373">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="de50b-4373">Method userData</span></span>

<span data-ttu-id="de50b-4374">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4374">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4375">Parameters</span></span>

<span data-ttu-id="de50b-4376">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4376">value</span></span>  
<span data-ttu-id="de50b-4377">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4377">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4378">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4378">Return Value</span></span>

<span data-ttu-id="de50b-4379">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="de50b-4379">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="de50b-4380">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="de50b-4380">Method userDataItem</span></span>

<span data-ttu-id="de50b-4381">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4381">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4382">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4382">Parameters</span></span>

<span data-ttu-id="de50b-4383">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4383">value</span></span>  
<span data-ttu-id="de50b-4384">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4384">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4385">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4385">Return Value</span></span>

<span data-ttu-id="de50b-4386">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="de50b-4386">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="de50b-4387">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="de50b-4387">Method userDataItems</span></span>

<span data-ttu-id="de50b-4388">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4388">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4389">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4389">Parameters</span></span>

<span data-ttu-id="de50b-4390">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4390">value</span></span>  
<span data-ttu-id="de50b-4391">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4391">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4392">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4392">Return Value</span></span>

<span data-ttu-id="de50b-4393">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="de50b-4393">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="de50b-4394">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="de50b-4394">Method userDisable</span></span>

<span data-ttu-id="de50b-4395">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4395">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4396">Parameters</span></span>

<span data-ttu-id="de50b-4397">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4397">value</span></span>  
<span data-ttu-id="de50b-4398">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4398">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4399">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4399">Return Value</span></span>

<span data-ttu-id="de50b-4400">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-4400">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="de50b-4401">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="de50b-4401">Method userHeight</span></span>

<span data-ttu-id="de50b-4402">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4402">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4403">Parameters</span></span>

<span data-ttu-id="de50b-4404">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4404">value</span></span>  
<span data-ttu-id="de50b-4405">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4405">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4406">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4406">Return Value</span></span>

<span data-ttu-id="de50b-4407">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="de50b-4407">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="de50b-4408">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="de50b-4408">Method userHide</span></span>

<span data-ttu-id="de50b-4409">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4409">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4410">Parameters</span></span>

<span data-ttu-id="de50b-4411">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4411">value</span></span>  
<span data-ttu-id="de50b-4412">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4412">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4413">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4413">Return Value</span></span>

<span data-ttu-id="de50b-4414">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-4414">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4415">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4415">Remarks</span></span>

<span data-ttu-id="de50b-4416">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4416">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="de50b-4417">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4417">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="de50b-4418">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4418">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="de50b-4419">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="de50b-4419">Method userOrgContainer</span></span>

<span data-ttu-id="de50b-4420">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4420">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4421">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4421">Parameters</span></span>

<span data-ttu-id="de50b-4422">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4422">value</span></span>  
<span data-ttu-id="de50b-4423">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4423">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4424">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4424">Return Value</span></span>

<span data-ttu-id="de50b-4425">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="de50b-4425">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="de50b-4426">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="de50b-4426">Method userOrgSibling</span></span>

<span data-ttu-id="de50b-4427">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4427">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4428">Parameters</span></span>

<span data-ttu-id="de50b-4429">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4429">value</span></span>  
<span data-ttu-id="de50b-4430">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4430">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4431">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4431">Return Value</span></span>

<span data-ttu-id="de50b-4432">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="de50b-4432">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="de50b-4433">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="de50b-4433">Method userPromptText</span></span>

<span data-ttu-id="de50b-4434">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4434">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4435">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4435">Parameters</span></span>

<span data-ttu-id="de50b-4436">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4436">value</span></span>  
<span data-ttu-id="de50b-4437">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4437">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4438">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4438">Return Value</span></span>

<span data-ttu-id="de50b-4439">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="de50b-4439">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="de50b-4440">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="de50b-4440">Method userSecurityLevel</span></span>

<span data-ttu-id="de50b-4441">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4441">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4442">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4442">Parameters</span></span>

<span data-ttu-id="de50b-4443">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4443">value</span></span>  
<span data-ttu-id="de50b-4444">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4444">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4445">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4445">Return Value</span></span>

<span data-ttu-id="de50b-4446">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="de50b-4446">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="de50b-4447">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="de50b-4447">Method userSkip</span></span>

<span data-ttu-id="de50b-4448">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4448">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4449">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4449">Parameters</span></span>

<span data-ttu-id="de50b-4450">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4450">value</span></span>  
<span data-ttu-id="de50b-4451">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4451">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="de50b-4452">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-4452">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4453">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4453">Return Value</span></span>

<span data-ttu-id="de50b-4454">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="de50b-4454">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="de50b-4455">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="de50b-4455">Method userWidth</span></span>

<span data-ttu-id="de50b-4456">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4456">Sets or returns the width of the control in pixels.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4457">Parameters</span></span>

<span data-ttu-id="de50b-4458">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4458">value</span></span>  
<span data-ttu-id="de50b-4459">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4459">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4460">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4460">Return Value</span></span>

<span data-ttu-id="de50b-4461">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4461">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4462">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4462">Remarks</span></span>

<span data-ttu-id="de50b-4463">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4463">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="de50b-4464">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4464">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="de50b-4465">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4465">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-useuserlayout"></a><span data-ttu-id="de50b-4466">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="de50b-4466">Method useUserLayout</span></span>

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4467">Parameters</span></span>

<span data-ttu-id="de50b-4468">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4468">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4469">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4469">Return Value</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="de50b-4470">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="de50b-4470">Method verticalSpacing</span></span>

<span data-ttu-id="de50b-4471">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4471">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4472">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4472">Parameters</span></span>

<span data-ttu-id="de50b-4473">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4473">value</span></span>  
<span data-ttu-id="de50b-4474">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4474">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-4475">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4475">mode</span></span>  
<span data-ttu-id="de50b-4476">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4476">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4477">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4477">Return Value</span></span>

<span data-ttu-id="de50b-4478">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="de50b-4478">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="de50b-4479">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4479">Method verticalSpacingMode</span></span>

<span data-ttu-id="de50b-4480">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4480">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4481">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4481">Parameters</span></span>

<span data-ttu-id="de50b-4482">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4482">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4483">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4483">Return Value</span></span>

<span data-ttu-id="de50b-4484">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-4484">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="de50b-4485">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="de50b-4485">Method verticalSpacingValue</span></span>

<span data-ttu-id="de50b-4486">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4486">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4487">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4487">Parameters</span></span>

<span data-ttu-id="de50b-4488">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4488">value</span></span>  
<span data-ttu-id="de50b-4489">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4489">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4490">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4490">Return Value</span></span>

<span data-ttu-id="de50b-4491">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="de50b-4491">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="de50b-4492">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="de50b-4492">Method visible</span></span>

<span data-ttu-id="de50b-4493">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4493">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4494">Parameters</span></span>

<span data-ttu-id="de50b-4495">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4495">value</span></span>  
<span data-ttu-id="de50b-4496">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4496">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4497">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4497">Return Value</span></span>

<span data-ttu-id="de50b-4498">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="de50b-4498">true if the control is visible; otherwise, false.</span></span>

### <a name="method-visiblecols"></a><span data-ttu-id="de50b-4499">メソッド visibleCols</span><span class="sxs-lookup"><span data-stu-id="de50b-4499">Method visibleCols</span></span>

    public int visibleCols([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4500">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4500">Parameters</span></span>

<span data-ttu-id="de50b-4501">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4501">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-4502">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4502">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4503">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4503">Return Value</span></span>

### <a name="method-visiblecolsmode"></a><span data-ttu-id="de50b-4504">メソッド visibleColsMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4504">Method visibleColsMode</span></span>

    public AutoMode visibleColsMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4505">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4505">Parameters</span></span>

<span data-ttu-id="de50b-4506">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4506">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4507">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4507">Return Value</span></span>

### <a name="method-visiblecolsvalue"></a><span data-ttu-id="de50b-4508">メソッド visibleColsValue</span><span class="sxs-lookup"><span data-stu-id="de50b-4508">Method visibleColsValue</span></span>

    public int visibleColsValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4509">Parameters</span></span>

<span data-ttu-id="de50b-4510">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4510">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4511">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4511">Return Value</span></span>

### <a name="method-visiblerows"></a><span data-ttu-id="de50b-4512">メソッド visibleRows</span><span class="sxs-lookup"><span data-stu-id="de50b-4512">Method visibleRows</span></span>

    public int visibleRows([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4513">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4513">Parameters</span></span>

<span data-ttu-id="de50b-4514">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4514">value</span></span>  

<!-- -->

<span data-ttu-id="de50b-4515">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4515">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4516">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4516">Return Value</span></span>

### <a name="method-visiblerowsmode"></a><span data-ttu-id="de50b-4517">メソッド visibleRowsMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4517">Method visibleRowsMode</span></span>

    public AutoMode visibleRowsMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4518">Parameters</span></span>

<span data-ttu-id="de50b-4519">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4519">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4520">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4520">Return Value</span></span>

### <a name="method-visiblerowsvalue"></a><span data-ttu-id="de50b-4521">メソッド visibleRowsValue</span><span class="sxs-lookup"><span data-stu-id="de50b-4521">Method visibleRowsValue</span></span>

    public int visibleRowsValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4522">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4522">Parameters</span></span>

<span data-ttu-id="de50b-4523">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4523">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="de50b-4524">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4524">Return Value</span></span>

### <a name="method-width"></a><span data-ttu-id="de50b-4525">メソッド width</span><span class="sxs-lookup"><span data-stu-id="de50b-4525">Method width</span></span>

<span data-ttu-id="de50b-4526">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4526">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="de50b-4527">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4527">Parameters</span></span>

<span data-ttu-id="de50b-4528">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4528">value</span></span>  
<span data-ttu-id="de50b-4529">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4529">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="de50b-4530">モード</span><span class="sxs-lookup"><span data-stu-id="de50b-4530">mode</span></span>  
<span data-ttu-id="de50b-4531">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4531">An Integer that indicates how the width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4532">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4532">Return Value</span></span>

<span data-ttu-id="de50b-4533">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-4533">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4534">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4534">Remarks</span></span>

<span data-ttu-id="de50b-4535">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4535">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="de50b-4536">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-4536">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="de50b-4537">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-4537">Mode.</span></span>           | <span data-ttu-id="de50b-4538">幅計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-4538">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-4539">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-4539">-1 Exact.</span></span>       | <span data-ttu-id="de50b-4540">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4540">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-4541">0 自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-4541">0 Auto.</span></span>         | <span data-ttu-id="de50b-4542">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4542">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-4543">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-4543">1 Column width.</span></span> | <span data-ttu-id="de50b-4544">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4544">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="de50b-4545">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4545">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="de50b-4546">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4546">Method widthMode</span></span>

<span data-ttu-id="de50b-4547">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4547">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4548">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4548">Parameters</span></span>

<span data-ttu-id="de50b-4549">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4549">value</span></span>  
<span data-ttu-id="de50b-4550">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="de50b-4550">An integer value that indicates how control width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4551">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4551">Return Value</span></span>

<span data-ttu-id="de50b-4552">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4552">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4553">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4553">Remarks</span></span>

<span data-ttu-id="de50b-4554">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="de50b-4554">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="de50b-4555">モード。</span><span class="sxs-lookup"><span data-stu-id="de50b-4555">Mode.</span></span>         | <span data-ttu-id="de50b-4556">幅計算。</span><span class="sxs-lookup"><span data-stu-id="de50b-4556">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de50b-4557">正確。</span><span class="sxs-lookup"><span data-stu-id="de50b-4557">Exact.</span></span>        | <span data-ttu-id="de50b-4558">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4558">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="de50b-4559">自動。</span><span class="sxs-lookup"><span data-stu-id="de50b-4559">Auto.</span></span>         | <span data-ttu-id="de50b-4560">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4560">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="de50b-4561">列の幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-4561">Column width.</span></span> | <span data-ttu-id="de50b-4562">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4562">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="de50b-4563">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="de50b-4563">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="de50b-4564">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="de50b-4564">Method widthValue</span></span>

<span data-ttu-id="de50b-4565">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4565">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="de50b-4566">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4566">Parameters</span></span>

<span data-ttu-id="de50b-4567">値</span><span class="sxs-lookup"><span data-stu-id="de50b-4567">value</span></span>  
<span data-ttu-id="de50b-4568">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4568">An Integer that specifies the width in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="de50b-4569">戻り値</span><span class="sxs-lookup"><span data-stu-id="de50b-4569">Return Value</span></span>

<span data-ttu-id="de50b-4570">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="de50b-4570">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="de50b-4571">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4571">Remarks</span></span>

<span data-ttu-id="de50b-4572">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4572">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-cut"></a><span data-ttu-id="de50b-4573">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="de50b-4573">Method cut</span></span>

<span data-ttu-id="de50b-4574">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="de50b-4574">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-applyquickfilter"></a><span data-ttu-id="de50b-4575">メソッド applyQuickFilter</span><span class="sxs-lookup"><span data-stu-id="de50b-4575">Method applyQuickFilter</span></span>

    public void applyQuickFilter([int controlId], [str filterValue])

#### <a name="parameters"></a><span data-ttu-id="de50b-4576">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4576">Parameters</span></span>

<span data-ttu-id="de50b-4577">controlId</span><span class="sxs-lookup"><span data-stu-id="de50b-4577">controlId</span></span>  

<!-- -->

<span data-ttu-id="de50b-4578">filterValue</span><span class="sxs-lookup"><span data-stu-id="de50b-4578">filterValue</span></span>  

### <a name="method-autosizecolumns"></a><span data-ttu-id="de50b-4579">メソッド autoSizeColumns</span><span class="sxs-lookup"><span data-stu-id="de50b-4579">Method autoSizeColumns</span></span>

    public void autoSizeColumns([boolean autoSizeColumns])

#### <a name="parameters"></a><span data-ttu-id="de50b-4580">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4580">Parameters</span></span>

<span data-ttu-id="de50b-4581">autoSizeColumns</span><span class="sxs-lookup"><span data-stu-id="de50b-4581">autoSizeColumns</span></span>  

### <a name="method-drop"></a><span data-ttu-id="de50b-4582">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="de50b-4582">Method drop</span></span>

<span data-ttu-id="de50b-4583">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4583">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-4584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4584">Parameters</span></span>

<span data-ttu-id="de50b-4585">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-4585">dragSource</span></span>  
<span data-ttu-id="de50b-4586">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4586">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-4587">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4587">dragMode</span></span>  
<span data-ttu-id="de50b-4588">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4588">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-4589">x</span><span class="sxs-lookup"><span data-stu-id="de50b-4589">x</span></span>  
<span data-ttu-id="de50b-4590">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4590">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-4591">y</span><span class="sxs-lookup"><span data-stu-id="de50b-4591">y</span></span>  
<span data-ttu-id="de50b-4592">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4592">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-context"></a><span data-ttu-id="de50b-4593">メソッド context</span><span class="sxs-lookup"><span data-stu-id="de50b-4593">Method context</span></span>

<span data-ttu-id="de50b-4594">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4594">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-jumpref"></a><span data-ttu-id="de50b-4595">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="de50b-4595">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-onlookup"></a><span data-ttu-id="de50b-4596">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="de50b-4596">Method OnLookup</span></span>

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-4597">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4597">Parameters</span></span>

<span data-ttu-id="de50b-4598">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-4598">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-4599">e</span><span class="sxs-lookup"><span data-stu-id="de50b-4599">e</span></span>  

### <a name="method-onlostfocus"></a><span data-ttu-id="de50b-4600">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-4600">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-4601">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4601">Parameters</span></span>

<span data-ttu-id="de50b-4602">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-4602">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-4603">e</span><span class="sxs-lookup"><span data-stu-id="de50b-4603">e</span></span>  

### <a name="method-registeroverridemethod"></a><span data-ttu-id="de50b-4604">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="de50b-4604">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="de50b-4605">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4605">Parameters</span></span>

<span data-ttu-id="de50b-4606">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="de50b-4606">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="de50b-4607">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="de50b-4607">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="de50b-4608">overrideObject</span><span class="sxs-lookup"><span data-stu-id="de50b-4608">overrideObject</span></span>  

### <a name="method-copy"></a><span data-ttu-id="de50b-4609">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="de50b-4609">Method copy</span></span>

<span data-ttu-id="de50b-4610">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="de50b-4610">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-enter"></a><span data-ttu-id="de50b-4611">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="de50b-4611">Method enter</span></span>

    public void enter()

### <a name="method-mouseenter"></a><span data-ttu-id="de50b-4612">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="de50b-4612">Method mouseEnter</span></span>

<span data-ttu-id="de50b-4613">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4613">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="de50b-4614">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4614">Parameters</span></span>

<span data-ttu-id="de50b-4615">x</span><span class="sxs-lookup"><span data-stu-id="de50b-4615">x</span></span>  
<span data-ttu-id="de50b-4616">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4616">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4617">y</span><span class="sxs-lookup"><span data-stu-id="de50b-4617">y</span></span>  
<span data-ttu-id="de50b-4618">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4618">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4619">ボタン</span><span class="sxs-lookup"><span data-stu-id="de50b-4619">button</span></span>  
<span data-ttu-id="de50b-4620">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4620">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4621">Ctrl</span><span class="sxs-lookup"><span data-stu-id="de50b-4621">Ctrl</span></span>  
<span data-ttu-id="de50b-4622">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4622">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="de50b-4623">シフト</span><span class="sxs-lookup"><span data-stu-id="de50b-4623">Shift</span></span>  
<span data-ttu-id="de50b-4624">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4624">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-displaycontrol"></a><span data-ttu-id="de50b-4625">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="de50b-4625">Method displayControl</span></span>

<span data-ttu-id="de50b-4626">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4626">Displays the control.</span></span>

    public void displayControl()

### <a name="method-onleaving"></a><span data-ttu-id="de50b-4627">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="de50b-4627">Method OnLeaving</span></span>

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-4628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4628">Parameters</span></span>

<span data-ttu-id="de50b-4629">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-4629">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-4630">e</span><span class="sxs-lookup"><span data-stu-id="de50b-4630">e</span></span>  

### <a name="method-paste"></a><span data-ttu-id="de50b-4631">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="de50b-4631">Method paste</span></span>

<span data-ttu-id="de50b-4632">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4632">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-resetusersetting"></a><span data-ttu-id="de50b-4633">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="de50b-4633">Method resetUserSetting</span></span>

<span data-ttu-id="de50b-4634">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="de50b-4634">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-quickfilterprovider"></a><span data-ttu-id="de50b-4635">メソッド quickFilterProvider</span><span class="sxs-lookup"><span data-stu-id="de50b-4635">Method quickFilterProvider</span></span>

    public void quickFilterProvider([GridQuickFilterProvider quickFilterProvider])

#### <a name="parameters"></a><span data-ttu-id="de50b-4636">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4636">Parameters</span></span>

<span data-ttu-id="de50b-4637">quickFilterProvider</span><span class="sxs-lookup"><span data-stu-id="de50b-4637">quickFilterProvider</span></span>  

### <a name="method-dropex"></a><span data-ttu-id="de50b-4638">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="de50b-4638">Method dropEx</span></span>

<span data-ttu-id="de50b-4639">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4639">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="de50b-4640">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4640">Parameters</span></span>

<span data-ttu-id="de50b-4641">dragSource</span><span class="sxs-lookup"><span data-stu-id="de50b-4641">dragSource</span></span>  
<span data-ttu-id="de50b-4642">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4642">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-4643">dragMode</span><span class="sxs-lookup"><span data-stu-id="de50b-4643">dragMode</span></span>  
<span data-ttu-id="de50b-4644">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4644">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-4645">x</span><span class="sxs-lookup"><span data-stu-id="de50b-4645">x</span></span>  
<span data-ttu-id="de50b-4646">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4646">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="de50b-4647">y</span><span class="sxs-lookup"><span data-stu-id="de50b-4647">y</span></span>  
<span data-ttu-id="de50b-4648">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="de50b-4648">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-onenter"></a><span data-ttu-id="de50b-4649">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="de50b-4649">Method OnEnter</span></span>

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-4650">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4650">Parameters</span></span>

<span data-ttu-id="de50b-4651">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-4651">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-4652">e</span><span class="sxs-lookup"><span data-stu-id="de50b-4652">e</span></span>  

### <a name="method-inputsearch"></a><span data-ttu-id="de50b-4653">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="de50b-4653">Method inputSearch</span></span>

<span data-ttu-id="de50b-4654">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4654">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="de50b-4655">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4655">Parameters</span></span>

<span data-ttu-id="de50b-4656">searchStr</span><span class="sxs-lookup"><span data-stu-id="de50b-4656">searchStr</span></span>  
<span data-ttu-id="de50b-4657">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="de50b-4657">The string value to use to filter data; optional.</span></span>

### <a name="method-filter"></a><span data-ttu-id="de50b-4658">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="de50b-4658">Method filter</span></span>

    public void filter([str filterStr])

#### <a name="parameters"></a><span data-ttu-id="de50b-4659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4659">Parameters</span></span>

<span data-ttu-id="de50b-4660">filterStr</span><span class="sxs-lookup"><span data-stu-id="de50b-4660">filterStr</span></span>  

### <a name="method-prefcolumnsize"></a><span data-ttu-id="de50b-4661">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="de50b-4661">Method prefColumnSize</span></span>

<span data-ttu-id="de50b-4662">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4662">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="de50b-4663">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4663">Parameters</span></span>

<span data-ttu-id="de50b-4664">width</span><span class="sxs-lookup"><span data-stu-id="de50b-4664">width</span></span>  
<span data-ttu-id="de50b-4665">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="de50b-4665">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="de50b-4666">height</span><span class="sxs-lookup"><span data-stu-id="de50b-4666">height</span></span>  
<span data-ttu-id="de50b-4667">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="de50b-4667">The preferred height of the control.</span></span>

### <a name="method-dragleave"></a><span data-ttu-id="de50b-4668">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="de50b-4668">Method dragLeave</span></span>

<span data-ttu-id="de50b-4669">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4669">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-ongotfocus"></a><span data-ttu-id="de50b-4670">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-4670">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="de50b-4671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de50b-4671">Parameters</span></span>

<span data-ttu-id="de50b-4672">sender</span><span class="sxs-lookup"><span data-stu-id="de50b-4672">sender</span></span>  

<!-- -->

<span data-ttu-id="de50b-4673">e</span><span class="sxs-lookup"><span data-stu-id="de50b-4673">e</span></span>  

### <a name="method-lostfocus"></a><span data-ttu-id="de50b-4674">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-4674">Method lostFocus</span></span>

<span data-ttu-id="de50b-4675">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4675">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-enddrag"></a><span data-ttu-id="de50b-4676">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="de50b-4676">Method endDrag</span></span>

<span data-ttu-id="de50b-4677">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="de50b-4677">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="de50b-4678">備考</span><span class="sxs-lookup"><span data-stu-id="de50b-4678">Remarks</span></span>

<span data-ttu-id="de50b-4679">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="de50b-4679">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="de50b-4680">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4680">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-arrange"></a><span data-ttu-id="de50b-4681">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="de50b-4681">Method arrange</span></span>

    public void arrange()

### <a name="method-gotfocus"></a><span data-ttu-id="de50b-4682">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-4682">Method gotFocus</span></span>

<span data-ttu-id="de50b-4683">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4683">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-mouseleave"></a><span data-ttu-id="de50b-4684">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="de50b-4684">Method mouseLeave</span></span>

<span data-ttu-id="de50b-4685">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4685">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-setfocus"></a><span data-ttu-id="de50b-4686">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="de50b-4686">Method setFocus</span></span>

<span data-ttu-id="de50b-4687">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="de50b-4687">Sets the focus on the control.</span></span>

    public void setFocus()



