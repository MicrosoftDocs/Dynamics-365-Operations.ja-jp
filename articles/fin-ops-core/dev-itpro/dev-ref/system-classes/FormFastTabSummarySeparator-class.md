---
title: FormFastTabSummarySeparator クラス
description: このトピックでは、FormFastTabSummarySeparator クラスについて説明します。
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
ms.openlocfilehash: 90801a2adf0ea9f544434125253f9e335a9e1300
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502941"
---
# <a name="class-formfasttabsummaryseparator"></a><span data-ttu-id="66471-103">クラス FormFastTabSummarySeparator</span><span class="sxs-lookup"><span data-stu-id="66471-103">Class FormFastTabSummarySeparator</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormFastTabSummarySeparator extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="66471-104">備考</span><span class="sxs-lookup"><span data-stu-id="66471-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="66471-105">例</span><span class="sxs-lookup"><span data-stu-id="66471-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="66471-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="66471-106">Methods</span></span>

| <span data-ttu-id="66471-107">方法</span><span class="sxs-lookup"><span data-stu-id="66471-107">Method</span></span>                                                                                                      | <span data-ttu-id="66471-108">説明</span><span class="sxs-lookup"><span data-stu-id="66471-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66471-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="66471-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="66471-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="66471-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="66471-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="66471-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="66471-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="66471-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="66471-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="66471-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="66471-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-118">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="66471-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-119">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="66471-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-120">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="66471-121">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="66471-121">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="66471-122">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-122">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="66471-123">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-123">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="66471-124">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-124">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="66471-125">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="66471-125">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="66471-126">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-126">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="66471-127">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-127">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="66471-128">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-128">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="66471-129">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-129">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="66471-130">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-130">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="66471-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="66471-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="66471-132">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-132">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="66471-133">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="66471-133">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="66471-134">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-134">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="66471-135">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="66471-135">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="66471-136">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-136">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="66471-137">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="66471-137">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="66471-138">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-138">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="66471-139">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-139">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="66471-140">コントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-140">Gets or sets the value that indicates whether the control is displayed.</span></span> |
| <span data-ttu-id="66471-141">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-141">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="66471-142">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-142">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="66471-143">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="66471-143">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="66471-144">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-144">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="66471-145">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="66471-145">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="66471-146">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-146">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="66471-147">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="66471-147">public str dragText()</span></span>                                                                                       | <span data-ttu-id="66471-148">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-148">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="66471-149">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-149">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="66471-150">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-150">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="66471-151">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="66471-151">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="66471-152">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-152">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="66471-153">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-153">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="66471-154">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-154">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="66471-155">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="66471-155">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="66471-156">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-156">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="66471-157">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="66471-157">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="66471-158">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-158">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="66471-159">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="66471-159">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="66471-160">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-160">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="66471-161">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-161">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="66471-162">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-162">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="66471-163">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-163">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="66471-164">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-164">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="66471-165">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="66471-165">public str helpField()</span></span>                                                                                      | <span data-ttu-id="66471-166">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-166">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="66471-167">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="66471-167">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="66471-168">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-168">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="66471-169">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="66471-169">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="66471-170">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-170">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="66471-171">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="66471-171">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="66471-172">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-172">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="66471-173">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="66471-173">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="66471-174">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="66471-174">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="66471-175">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-175">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="66471-176">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="66471-176">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="66471-177">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-177">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="66471-178">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="66471-178">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="66471-179">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-179">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="66471-180">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-180">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="66471-181">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="66471-181">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="66471-182">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-182">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="66471-183">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-183">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="66471-184">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-184">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="66471-185">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-185">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="66471-186">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-186">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="66471-187">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-187">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="66471-188">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="66471-188">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="66471-189">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="66471-189">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="66471-190">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-190">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="66471-191">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="66471-191">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="66471-192">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-192">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="66471-193">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="66471-193">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="66471-194">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-194">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="66471-195">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="66471-195">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="66471-196">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-196">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="66471-197">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="66471-197">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="66471-198">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-198">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="66471-199">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-199">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="66471-200">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="66471-200">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="66471-201">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="66471-201">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="66471-202">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-202">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="66471-203">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="66471-203">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="66471-204">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-204">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="66471-205">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="66471-205">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="66471-206">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="66471-206">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="66471-207">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-207">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="66471-208">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-208">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="66471-209">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="66471-209">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="66471-210">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-210">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="66471-211">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="66471-211">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="66471-212">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-212">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="66471-213">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-213">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="66471-214">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-214">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="66471-215">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-215">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="66471-216">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-216">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="66471-217">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-217">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="66471-218">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-218">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="66471-219">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="66471-219">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="66471-220">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-220">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="66471-221">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-221">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="66471-222">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-222">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="66471-223">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-223">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="66471-224">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-224">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="66471-225">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-225">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="66471-226">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-226">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="66471-227">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-227">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="66471-228">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-228">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="66471-229">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-229">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="66471-230">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-230">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="66471-231">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-231">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="66471-232">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-232">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="66471-233">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-233">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="66471-234">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-234">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="66471-235">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-235">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="66471-236">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="66471-236">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="66471-237">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-237">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="66471-238">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-238">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="66471-239">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-239">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="66471-240">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-240">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="66471-241">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-241">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="66471-242">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-242">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="66471-243">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-243">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="66471-244">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="66471-244">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="66471-245">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-245">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="66471-246">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="66471-246">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="66471-247">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-247">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="66471-248">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-248">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="66471-249">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-249">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="66471-250">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="66471-250">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="66471-251">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-251">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="66471-252">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="66471-252">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="66471-253">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-253">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="66471-254">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-254">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="66471-255">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-255">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="66471-256">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="66471-256">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="66471-257">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-257">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="66471-258">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="66471-258">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="66471-259">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-259">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="66471-260">public void copy()</span><span class="sxs-lookup"><span data-stu-id="66471-260">public void copy()</span></span>                                                                                          | <span data-ttu-id="66471-261">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="66471-261">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="66471-262">public void cut()</span><span class="sxs-lookup"><span data-stu-id="66471-262">public void cut()</span></span>                                                                                           | <span data-ttu-id="66471-263">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="66471-263">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="66471-264">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="66471-264">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="66471-265">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-265">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="66471-266">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="66471-266">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="66471-267">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-267">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="66471-268">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="66471-268">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="66471-269">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-269">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="66471-270">public void context()</span><span class="sxs-lookup"><span data-stu-id="66471-270">public void context()</span></span>                                                                                       | <span data-ttu-id="66471-271">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="66471-271">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="66471-272">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="66471-272">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="66471-273">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-273">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="66471-274">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="66471-274">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="66471-275">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="66471-275">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="66471-276">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="66471-276">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="66471-277">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-277">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="66471-278">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="66471-278">public void displayControl()</span></span>                                                                                | <span data-ttu-id="66471-279">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="66471-279">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="66471-280">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="66471-280">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="66471-281">public void paste()</span><span class="sxs-lookup"><span data-stu-id="66471-281">public void paste()</span></span>                                                                                         | <span data-ttu-id="66471-282">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="66471-282">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="66471-283">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="66471-283">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="66471-284">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="66471-284">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="66471-285">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="66471-285">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="66471-286">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-286">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="66471-287">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="66471-287">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="66471-288">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-288">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="66471-289">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="66471-289">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="66471-290">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="66471-290">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="66471-291">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="66471-291">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="66471-292">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-292">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |

## <a name="method-aligncontrol"></a><span data-ttu-id="66471-293">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="66471-293">Method alignControl</span></span>

<span data-ttu-id="66471-294">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-294">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="66471-295">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="66471-295">Parameters - alignControl</span></span>

<span data-ttu-id="66471-296">値</span><span class="sxs-lookup"><span data-stu-id="66471-296">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="66471-297">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="66471-297">Return Value - alignControl</span></span>

<span data-ttu-id="66471-298">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="66471-298">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="66471-299">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="66471-299">Remarks - alignControl</span></span>

<span data-ttu-id="66471-300">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="66471-300">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="66471-301">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="66471-301">Method allowEdit</span></span>

<span data-ttu-id="66471-302">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-302">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="66471-303">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="66471-303">Parameters - allowEdit</span></span>

<span data-ttu-id="66471-304">値</span><span class="sxs-lookup"><span data-stu-id="66471-304">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="66471-305">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="66471-305">Return Value - allowEdit</span></span>

<span data-ttu-id="66471-306">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-306">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="66471-307">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="66471-307">Remarks - allowEdit</span></span>

<span data-ttu-id="66471-308">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="66471-308">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="66471-309">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="66471-309">Method allowSysSetup</span></span>

<span data-ttu-id="66471-310">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-310">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="66471-311">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="66471-311">Return Value - allowSysSetup</span></span>

<span data-ttu-id="66471-312">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-312">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="66471-313">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="66471-313">Method autoDeclaration</span></span>

<span data-ttu-id="66471-314">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-314">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="66471-315">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="66471-315">Parameters - autoDeclaration</span></span>

<span data-ttu-id="66471-316">値</span><span class="sxs-lookup"><span data-stu-id="66471-316">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="66471-317">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="66471-317">Return Value - autoDeclaration</span></span>

<span data-ttu-id="66471-318">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-318">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="66471-319">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="66471-319">Remarks - autoDeclaration</span></span>

<span data-ttu-id="66471-320">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="66471-320">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="66471-321">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="66471-321">Method backgroundColor</span></span>

<span data-ttu-id="66471-322">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-322">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="66471-323">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="66471-323">Parameters - backgroundColor</span></span>

<span data-ttu-id="66471-324">値</span><span class="sxs-lookup"><span data-stu-id="66471-324">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="66471-325">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="66471-325">Return Value - backgroundColor</span></span>

<span data-ttu-id="66471-326">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="66471-326">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="66471-327">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="66471-327">Remarks - backgroundColor</span></span>

<span data-ttu-id="66471-328">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="66471-328">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="66471-329">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="66471-329">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="66471-330">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="66471-330">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="66471-331">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="66471-331">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="66471-332">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="66471-332">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="66471-333">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="66471-333">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="66471-334">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="66471-334">Method backStyle</span></span>

<span data-ttu-id="66471-335">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-335">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="66471-336">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="66471-336">Parameters - backStyle</span></span>

<span data-ttu-id="66471-337">値</span><span class="sxs-lookup"><span data-stu-id="66471-337">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="66471-338">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="66471-338">Return Value - backStyle</span></span>

<span data-ttu-id="66471-339">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="66471-339">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="66471-340">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="66471-340">Method beginDrag</span></span>

<span data-ttu-id="66471-341">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-341">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="66471-342">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="66471-342">Parameters - beginDrag</span></span>

<span data-ttu-id="66471-343">x</span><span class="sxs-lookup"><span data-stu-id="66471-343">x</span></span>  
<span data-ttu-id="66471-344">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-344">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="66471-345">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="66471-345">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="66471-346">y</span><span class="sxs-lookup"><span data-stu-id="66471-346">y</span></span>  
<span data-ttu-id="66471-347">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-347">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="66471-348">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="66471-348">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="66471-349">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="66471-349">Return Value - beginDrag</span></span>

<span data-ttu-id="66471-350">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="66471-350">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="66471-351">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="66471-351">Remarks - beginDrag</span></span>

<span data-ttu-id="66471-352">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="66471-352">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="66471-353">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="66471-353">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="66471-354">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="66471-354">Method bold</span></span>

<span data-ttu-id="66471-355">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-355">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="66471-356">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="66471-356">Parameters - bold</span></span>

<span data-ttu-id="66471-357">値</span><span class="sxs-lookup"><span data-stu-id="66471-357">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="66471-358">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="66471-358">Return Value - bold</span></span>

<span data-ttu-id="66471-359">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-359">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="66471-360">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="66471-360">Remarks - bold</span></span>

<span data-ttu-id="66471-361">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="66471-361">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="66471-362">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="66471-362">0 Use the default font weight.</span></span>
-   <span data-ttu-id="66471-363">1 シン。</span><span class="sxs-lookup"><span data-stu-id="66471-363">1 Thin.</span></span>
-   <span data-ttu-id="66471-364">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="66471-364">2 Extra-light.</span></span>
-   <span data-ttu-id="66471-365">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="66471-365">3 Light.</span></span>
-   <span data-ttu-id="66471-366">4 標準。</span><span class="sxs-lookup"><span data-stu-id="66471-366">4 Normal.</span></span>
-   <span data-ttu-id="66471-367">5 中。</span><span class="sxs-lookup"><span data-stu-id="66471-367">5 Medium.</span></span>
-   <span data-ttu-id="66471-368">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="66471-368">6 Semibold.</span></span>
-   <span data-ttu-id="66471-369">7 太字。</span><span class="sxs-lookup"><span data-stu-id="66471-369">7 Bold.</span></span>
-   <span data-ttu-id="66471-370">8 極太。</span><span class="sxs-lookup"><span data-stu-id="66471-370">8 Extra-bold.</span></span>
-   <span data-ttu-id="66471-371">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="66471-371">9 Heavy.</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="66471-372">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="66471-372">Method calcControlSize</span></span>

<span data-ttu-id="66471-373">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-373">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="66471-374">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="66471-374">Parameters - calcControlSize</span></span>

<span data-ttu-id="66471-375">chars</span><span class="sxs-lookup"><span data-stu-id="66471-375">chars</span></span>  
<span data-ttu-id="66471-376">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="66471-376">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="66471-377">明細行</span><span class="sxs-lookup"><span data-stu-id="66471-377">lines</span></span>  
<span data-ttu-id="66471-378">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="66471-378">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="66471-379">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="66471-379">Return Value - calcControlSize</span></span>

<span data-ttu-id="66471-380">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="66471-380">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="66471-381">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="66471-381">Method characterSet</span></span>

<span data-ttu-id="66471-382">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-382">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="66471-383">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="66471-383">Parameters - characterSet</span></span>

<span data-ttu-id="66471-384">値</span><span class="sxs-lookup"><span data-stu-id="66471-384">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="66471-385">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="66471-385">Return Value - characterSet</span></span>

<span data-ttu-id="66471-386">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-386">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="66471-387">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="66471-387">Remarks - characterSet</span></span>

<span data-ttu-id="66471-388">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-388">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="66471-389">値です。</span><span class="sxs-lookup"><span data-stu-id="66471-389">Value.</span></span> | <span data-ttu-id="66471-390">説明。</span><span class="sxs-lookup"><span data-stu-id="66471-390">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="66471-391">0</span><span class="sxs-lookup"><span data-stu-id="66471-391">0</span></span>      | <span data-ttu-id="66471-392">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-392">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="66471-393">1</span><span class="sxs-lookup"><span data-stu-id="66471-393">1</span></span>      | <span data-ttu-id="66471-394">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-394">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="66471-395">2</span><span class="sxs-lookup"><span data-stu-id="66471-395">2</span></span>      | <span data-ttu-id="66471-396">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-396">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="66471-397">77</span><span class="sxs-lookup"><span data-stu-id="66471-397">77</span></span>     | <span data-ttu-id="66471-398">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-398">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="66471-399">128</span><span class="sxs-lookup"><span data-stu-id="66471-399">128</span></span>    | <span data-ttu-id="66471-400">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-400">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="66471-401">129</span><span class="sxs-lookup"><span data-stu-id="66471-401">129</span></span>    | <span data-ttu-id="66471-402">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-402">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="66471-403">134</span><span class="sxs-lookup"><span data-stu-id="66471-403">134</span></span>    | <span data-ttu-id="66471-404">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-404">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="66471-405">136</span><span class="sxs-lookup"><span data-stu-id="66471-405">136</span></span>    | <span data-ttu-id="66471-406">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-406">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="66471-407">161</span><span class="sxs-lookup"><span data-stu-id="66471-407">161</span></span>    | <span data-ttu-id="66471-408">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-408">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="66471-409">162</span><span class="sxs-lookup"><span data-stu-id="66471-409">162</span></span>    | <span data-ttu-id="66471-410">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-410">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="66471-411">163</span><span class="sxs-lookup"><span data-stu-id="66471-411">163</span></span>    | <span data-ttu-id="66471-412">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-412">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="66471-413">186</span><span class="sxs-lookup"><span data-stu-id="66471-413">186</span></span>    | <span data-ttu-id="66471-414">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-414">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="66471-415">204</span><span class="sxs-lookup"><span data-stu-id="66471-415">204</span></span>    | <span data-ttu-id="66471-416">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-416">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="66471-417">238</span><span class="sxs-lookup"><span data-stu-id="66471-417">238</span></span>    | <span data-ttu-id="66471-418">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-418">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="66471-419">255</span><span class="sxs-lookup"><span data-stu-id="66471-419">255</span></span>    | <span data-ttu-id="66471-420">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-420">OEM\_CHARSET</span></span>         |

<span data-ttu-id="66471-421">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="66471-421">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="66471-422">値です。</span><span class="sxs-lookup"><span data-stu-id="66471-422">Value.</span></span> | <span data-ttu-id="66471-423">説明。</span><span class="sxs-lookup"><span data-stu-id="66471-423">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="66471-424">130</span><span class="sxs-lookup"><span data-stu-id="66471-424">130</span></span>    | <span data-ttu-id="66471-425">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-425">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="66471-426">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="66471-426">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="66471-427">値です。</span><span class="sxs-lookup"><span data-stu-id="66471-427">Value.</span></span> | <span data-ttu-id="66471-428">説明。</span><span class="sxs-lookup"><span data-stu-id="66471-428">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="66471-429">177</span><span class="sxs-lookup"><span data-stu-id="66471-429">177</span></span>    | <span data-ttu-id="66471-430">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-430">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="66471-431">178</span><span class="sxs-lookup"><span data-stu-id="66471-431">178</span></span>    | <span data-ttu-id="66471-432">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-432">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="66471-433">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="66471-433">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="66471-434">値です。</span><span class="sxs-lookup"><span data-stu-id="66471-434">Value.</span></span> | <span data-ttu-id="66471-435">説明。</span><span class="sxs-lookup"><span data-stu-id="66471-435">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="66471-436">222</span><span class="sxs-lookup"><span data-stu-id="66471-436">222</span></span>    | <span data-ttu-id="66471-437">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="66471-437">THAI\_CHARSET</span></span> |

<span data-ttu-id="66471-438">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="66471-438">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="66471-439">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="66471-439">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="66471-440">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66471-440">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="66471-441">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="66471-441">Method colorScheme</span></span>

<span data-ttu-id="66471-442">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-442">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="66471-443">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="66471-443">Parameters - colorScheme</span></span>

<span data-ttu-id="66471-444">値</span><span class="sxs-lookup"><span data-stu-id="66471-444">value</span></span>  
<span data-ttu-id="66471-445">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-445">The value to set; optional.</span></span>

### <a name="return-value---colorscheme"></a><span data-ttu-id="66471-446">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="66471-446">Return Value - colorScheme</span></span>

<span data-ttu-id="66471-447">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="66471-447">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="66471-448">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="66471-448">Remarks - colorScheme</span></span>

<span data-ttu-id="66471-449">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="66471-449">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="66471-450">値です。</span><span class="sxs-lookup"><span data-stu-id="66471-450">Value.</span></span> | <span data-ttu-id="66471-451">スタイル。</span><span class="sxs-lookup"><span data-stu-id="66471-451">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="66471-452">0</span><span class="sxs-lookup"><span data-stu-id="66471-452">0</span></span>      | <span data-ttu-id="66471-453">既定。</span><span class="sxs-lookup"><span data-stu-id="66471-453">Default.</span></span>               |
| <span data-ttu-id="66471-454">1</span><span class="sxs-lookup"><span data-stu-id="66471-454">1</span></span>      | <span data-ttu-id="66471-455">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="66471-455">The Windows palette.</span></span>   |
| <span data-ttu-id="66471-456">2</span><span class="sxs-lookup"><span data-stu-id="66471-456">2</span></span>      | <span data-ttu-id="66471-457">真の配色。</span><span class="sxs-lookup"><span data-stu-id="66471-457">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="66471-458">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="66471-458">Method configurationKey</span></span>

<span data-ttu-id="66471-459">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-459">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="66471-460">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="66471-460">Parameters - configurationKey</span></span>

<span data-ttu-id="66471-461">値</span><span class="sxs-lookup"><span data-stu-id="66471-461">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="66471-462">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="66471-462">Return Value - configurationKey</span></span>

<span data-ttu-id="66471-463">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="66471-463">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="66471-464">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="66471-464">Remarks - configurationKey</span></span>

<span data-ttu-id="66471-465">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="66471-465">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="66471-466">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="66471-466">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="66471-467">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="66471-467">Method configurationKeyEx</span></span>

<span data-ttu-id="66471-468">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-468">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="66471-469">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="66471-469">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="66471-470">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="66471-470">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="66471-471">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="66471-471">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="66471-472">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="66471-472">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="66471-473">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="66471-473">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="66471-474">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="66471-474">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="66471-475">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="66471-475">Method countryRegionCodes</span></span>

<span data-ttu-id="66471-476">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-476">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="66471-477">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="66471-477">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="66471-478">値</span><span class="sxs-lookup"><span data-stu-id="66471-478">value</span></span>  
<span data-ttu-id="66471-479">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-479">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="66471-480">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="66471-480">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="66471-481">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="66471-481">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="66471-482">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="66471-482">Method dataRelationPath</span></span>

<span data-ttu-id="66471-483">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-483">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="66471-484">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="66471-484">Parameters - dataRelationPath</span></span>

<span data-ttu-id="66471-485">値</span><span class="sxs-lookup"><span data-stu-id="66471-485">value</span></span>  
<span data-ttu-id="66471-486">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-486">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="66471-487">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="66471-487">Return Value - dataRelationPath</span></span>

<span data-ttu-id="66471-488">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="66471-488">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="66471-489">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="66471-489">Remarks - dataRelationPath</span></span>

<span data-ttu-id="66471-490">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="66471-490">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="66471-491">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="66471-491">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="66471-492">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="66471-492">Method displayTarget</span></span>

<span data-ttu-id="66471-493">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-493">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="66471-494">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="66471-494">Parameters - displayTarget</span></span>

<span data-ttu-id="66471-495">値</span><span class="sxs-lookup"><span data-stu-id="66471-495">value</span></span>  
<span data-ttu-id="66471-496">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-496">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="66471-497">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="66471-497">Return Value - displayTarget</span></span>

<span data-ttu-id="66471-498">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="66471-498">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="66471-499">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="66471-499">Method dragDrop</span></span>

<span data-ttu-id="66471-500">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-500">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="66471-501">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="66471-501">Parameters - dragDrop</span></span>

<span data-ttu-id="66471-502">値</span><span class="sxs-lookup"><span data-stu-id="66471-502">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="66471-503">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="66471-503">Return Value - dragDrop</span></span>

<span data-ttu-id="66471-504">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="66471-504">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="66471-505">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="66471-505">Method dragOver</span></span>

<span data-ttu-id="66471-506">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-506">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="66471-507">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="66471-507">Parameters - dragOver</span></span>

<span data-ttu-id="66471-508">dragSource</span><span class="sxs-lookup"><span data-stu-id="66471-508">dragSource</span></span>  
<span data-ttu-id="66471-509">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-509">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-510">dragMode</span><span class="sxs-lookup"><span data-stu-id="66471-510">dragMode</span></span>  
<span data-ttu-id="66471-511">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-511">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-512">x</span><span class="sxs-lookup"><span data-stu-id="66471-512">x</span></span>  
<span data-ttu-id="66471-513">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-513">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-514">y</span><span class="sxs-lookup"><span data-stu-id="66471-514">y</span></span>  
<span data-ttu-id="66471-515">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-515">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="66471-516">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="66471-516">Return Value - dragOver</span></span>

<span data-ttu-id="66471-517">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="66471-517">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="66471-518">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="66471-518">Method dragOverEx</span></span>

<span data-ttu-id="66471-519">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-519">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="66471-520">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="66471-520">Parameters - dragOverEx</span></span>

<span data-ttu-id="66471-521">dragSource</span><span class="sxs-lookup"><span data-stu-id="66471-521">dragSource</span></span>  
<span data-ttu-id="66471-522">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-522">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-523">dragMode</span><span class="sxs-lookup"><span data-stu-id="66471-523">dragMode</span></span>  
<span data-ttu-id="66471-524">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-524">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-525">x</span><span class="sxs-lookup"><span data-stu-id="66471-525">x</span></span>  
<span data-ttu-id="66471-526">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-526">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-527">y</span><span class="sxs-lookup"><span data-stu-id="66471-527">y</span></span>  
<span data-ttu-id="66471-528">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-528">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="66471-529">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="66471-529">Return Value - dragOverEx</span></span>

<span data-ttu-id="66471-530">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="66471-530">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="66471-531">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="66471-531">Method dragText</span></span>

<span data-ttu-id="66471-532">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-532">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="66471-533">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="66471-533">Return Value - dragText</span></span>

<span data-ttu-id="66471-534">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="66471-534">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="66471-535">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="66471-535">Method enabled</span></span>

<span data-ttu-id="66471-536">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="66471-536">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="66471-537">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="66471-537">Parameters - enabled</span></span>

<span data-ttu-id="66471-538">値</span><span class="sxs-lookup"><span data-stu-id="66471-538">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="66471-539">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="66471-539">Return Value - enabled</span></span>

<span data-ttu-id="66471-540">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-540">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="66471-541">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="66471-541">Remarks - enabled</span></span>

<span data-ttu-id="66471-542">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="66471-542">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="66471-543">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="66471-543">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="66471-544">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="66471-544">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="66471-545">メソッド font</span><span class="sxs-lookup"><span data-stu-id="66471-545">Method font</span></span>

<span data-ttu-id="66471-546">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-546">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="66471-547">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="66471-547">Parameters - font</span></span>

<span data-ttu-id="66471-548">値</span><span class="sxs-lookup"><span data-stu-id="66471-548">value</span></span>  
<span data-ttu-id="66471-549">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-549">The value to set; optional.</span></span>

### <a name="return-value---font"></a><span data-ttu-id="66471-550">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="66471-550">Return Value - font</span></span>

<span data-ttu-id="66471-551">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="66471-551">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="66471-552">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="66471-552">Method fontSize</span></span>

<span data-ttu-id="66471-553">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-553">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="66471-554">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="66471-554">Parameters - fontSize</span></span>

<span data-ttu-id="66471-555">値</span><span class="sxs-lookup"><span data-stu-id="66471-555">value</span></span>  
<span data-ttu-id="66471-556">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-556">The value to set; optional.</span></span>

### <a name="return-value---fontsize"></a><span data-ttu-id="66471-557">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="66471-557">Return Value - fontSize</span></span>

<span data-ttu-id="66471-558">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="66471-558">The height of the font in points.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="66471-559">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="66471-559">Method hasChanged</span></span>

<span data-ttu-id="66471-560">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-560">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="66471-561">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="66471-561">Parameters - hasChanged</span></span>

<span data-ttu-id="66471-562">val</span><span class="sxs-lookup"><span data-stu-id="66471-562">val</span></span>  
<span data-ttu-id="66471-563">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-563">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="66471-564">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="66471-564">Return Value - hasChanged</span></span>

<span data-ttu-id="66471-565">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-565">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="66471-566">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="66471-566">Method hasUserSetting</span></span>

<span data-ttu-id="66471-567">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-567">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="66471-568">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="66471-568">Return Value - hasUserSetting</span></span>

<span data-ttu-id="66471-569">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-569">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="66471-570">メソッド height</span><span class="sxs-lookup"><span data-stu-id="66471-570">Method height</span></span>

<span data-ttu-id="66471-571">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-571">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="66471-572">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="66471-572">Parameters - height</span></span>

<span data-ttu-id="66471-573">値</span><span class="sxs-lookup"><span data-stu-id="66471-573">value</span></span>  

<!-- -->

<span data-ttu-id="66471-574">モード</span><span class="sxs-lookup"><span data-stu-id="66471-574">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="66471-575">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="66471-575">Return Value - height</span></span>

<span data-ttu-id="66471-576">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="66471-576">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="66471-577">備考 - height</span><span class="sxs-lookup"><span data-stu-id="66471-577">Remarks - height</span></span>

<span data-ttu-id="66471-578">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="66471-578">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="66471-579">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="66471-579">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="66471-580">モード。</span><span class="sxs-lookup"><span data-stu-id="66471-580">Mode.</span></span>            | <span data-ttu-id="66471-581">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="66471-581">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="66471-582">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="66471-582">-1 Exact.</span></span>        | <span data-ttu-id="66471-583">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="66471-583">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="66471-584">0 自動。</span><span class="sxs-lookup"><span data-stu-id="66471-584">0 Auto.</span></span>          | <span data-ttu-id="66471-585">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="66471-585">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="66471-586">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="66471-586">1 Column height.</span></span> | <span data-ttu-id="66471-587">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="66471-587">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="66471-588">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="66471-588">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="66471-589">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="66471-589">Method heightMode</span></span>

<span data-ttu-id="66471-590">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-590">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="66471-591">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="66471-591">Parameters - heightMode</span></span>

<span data-ttu-id="66471-592">値</span><span class="sxs-lookup"><span data-stu-id="66471-592">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="66471-593">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="66471-593">Return Value - heightMode</span></span>

<span data-ttu-id="66471-594">計算モード。</span><span class="sxs-lookup"><span data-stu-id="66471-594">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="66471-595">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="66471-595">Remarks - heightMode</span></span>

<span data-ttu-id="66471-596">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="66471-596">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="66471-597">モード。</span><span class="sxs-lookup"><span data-stu-id="66471-597">Mode.</span></span>          | <span data-ttu-id="66471-598">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="66471-598">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="66471-599">正確。</span><span class="sxs-lookup"><span data-stu-id="66471-599">Exact.</span></span>         | <span data-ttu-id="66471-600">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="66471-600">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="66471-601">自動。</span><span class="sxs-lookup"><span data-stu-id="66471-601">Auto.</span></span>          | <span data-ttu-id="66471-602">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="66471-602">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="66471-603">列の高さ</span><span class="sxs-lookup"><span data-stu-id="66471-603">Column height.</span></span> | <span data-ttu-id="66471-604">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="66471-604">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="66471-605">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="66471-605">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="66471-606">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="66471-606">Method heightValue</span></span>

<span data-ttu-id="66471-607">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-607">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="66471-608">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="66471-608">Parameters - heightValue</span></span>

<span data-ttu-id="66471-609">値</span><span class="sxs-lookup"><span data-stu-id="66471-609">value</span></span>  
<span data-ttu-id="66471-610">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-610">The value to set; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="66471-611">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="66471-611">Return Value - heightValue</span></span>

<span data-ttu-id="66471-612">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="66471-612">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="66471-613">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="66471-613">Remarks - heightValue</span></span>

<span data-ttu-id="66471-614">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="66471-614">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="66471-615">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="66471-615">Method helpField</span></span>

<span data-ttu-id="66471-616">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-616">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="66471-617">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="66471-617">Return Value - helpField</span></span>

<span data-ttu-id="66471-618">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="66471-618">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="66471-619">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="66471-619">Remarks - helpField</span></span>

<span data-ttu-id="66471-620">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="66471-620">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="66471-621">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="66471-621">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="66471-622">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="66471-622">Method helpText</span></span>

<span data-ttu-id="66471-623">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-623">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="66471-624">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="66471-624">Parameters - helpText</span></span>

<span data-ttu-id="66471-625">値</span><span class="sxs-lookup"><span data-stu-id="66471-625">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="66471-626">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="66471-626">Return Value - helpText</span></span>

<span data-ttu-id="66471-627">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="66471-627">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="66471-628">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="66471-628">Remarks - helpText</span></span>

<span data-ttu-id="66471-629">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-629">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="66471-630">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="66471-630">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="66471-631">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="66471-631">Method hierarchyParent</span></span>

<span data-ttu-id="66471-632">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-632">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="66471-633">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="66471-633">Parameters - hierarchyParent</span></span>

<span data-ttu-id="66471-634">値</span><span class="sxs-lookup"><span data-stu-id="66471-634">value</span></span>  
<span data-ttu-id="66471-635">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="66471-635">The value to assign the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="66471-636">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="66471-636">Return Value - hierarchyParent</span></span>

<span data-ttu-id="66471-637">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="66471-637">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="66471-638">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="66471-638">Method hWnd</span></span>

<span data-ttu-id="66471-639">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-639">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="66471-640">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="66471-640">Return Value - hWnd</span></span>

<span data-ttu-id="66471-641">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="66471-641">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="66471-642">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="66471-642">Remarks - hWnd</span></span>

<span data-ttu-id="66471-643">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="66471-643">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="66471-644">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="66471-644">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="66471-645">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="66471-645">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="66471-646">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="66471-646">Method isDisplayed</span></span>

<span data-ttu-id="66471-647">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-647">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="66471-648">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="66471-648">Return Value - isDisplayed</span></span>

<span data-ttu-id="66471-649">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="66471-649">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="66471-650">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="66471-650">Remarks - isDisplayed</span></span>

<span data-ttu-id="66471-651">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="66471-651">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="66471-652">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="66471-652">Method isRestricted</span></span>

<span data-ttu-id="66471-653">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-653">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="66471-654">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="66471-654">Return Value - isRestricted</span></span>

<span data-ttu-id="66471-655">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="66471-655">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="66471-656">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="66471-656">Method isUserSetupEnabled</span></span>

<span data-ttu-id="66471-657">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-657">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="66471-658">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="66471-658">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="66471-659">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="66471-659">neededSetupRights</span></span>  
<span data-ttu-id="66471-660">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="66471-660">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="66471-661">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="66471-661">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="66471-662">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-662">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="66471-663">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="66471-663">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="66471-664">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="66471-664">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66471-665">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="66471-665">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="66471-666">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="66471-666">No changes can be made to the control.</span></span> <span data-ttu-id="66471-667">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="66471-667">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="66471-668">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="66471-668">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="66471-669">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="66471-669">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="66471-670">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="66471-670">The user cannot move the control.</span></span>   |
| <span data-ttu-id="66471-671">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="66471-671">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="66471-672">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="66471-672">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="66471-673">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="66471-673">The user can also move the control.</span></span> |

<span data-ttu-id="66471-674">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="66471-674">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="66471-675">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="66471-675">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="66471-676">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="66471-676">Parameters - italic</span></span>

<span data-ttu-id="66471-677">値</span><span class="sxs-lookup"><span data-stu-id="66471-677">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="66471-678">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="66471-678">Return Value - italic</span></span>

## <a name="method-left"></a><span data-ttu-id="66471-679">メソッド left</span><span class="sxs-lookup"><span data-stu-id="66471-679">Method left</span></span>

<span data-ttu-id="66471-680">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-680">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="66471-681">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="66471-681">Parameters - left</span></span>

<span data-ttu-id="66471-682">値</span><span class="sxs-lookup"><span data-stu-id="66471-682">value</span></span>  
<span data-ttu-id="66471-683">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-683">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="66471-684">モード</span><span class="sxs-lookup"><span data-stu-id="66471-684">mode</span></span>  
<span data-ttu-id="66471-685">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-685">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="66471-686">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="66471-686">Return Value - left</span></span>

<span data-ttu-id="66471-687">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="66471-687">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="66471-688">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="66471-688">Method leftMode</span></span>

<span data-ttu-id="66471-689">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-689">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="66471-690">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="66471-690">Parameters - leftMode</span></span>

<span data-ttu-id="66471-691">値</span><span class="sxs-lookup"><span data-stu-id="66471-691">value</span></span>  
<span data-ttu-id="66471-692">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-692">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="66471-693">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="66471-693">Return Value - leftMode</span></span>

<span data-ttu-id="66471-694">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="66471-694">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="66471-695">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="66471-695">Method leftValue</span></span>

<span data-ttu-id="66471-696">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-696">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="66471-697">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="66471-697">Parameters - leftValue</span></span>

<span data-ttu-id="66471-698">値</span><span class="sxs-lookup"><span data-stu-id="66471-698">value</span></span>  
<span data-ttu-id="66471-699">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-699">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="66471-700">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="66471-700">Return Value - leftValue</span></span>

<span data-ttu-id="66471-701">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="66471-701">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="66471-702">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="66471-702">Method markAsUserAdd</span></span>

<span data-ttu-id="66471-703">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="66471-703">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="66471-704">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="66471-704">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="66471-705">値</span><span class="sxs-lookup"><span data-stu-id="66471-705">value</span></span>  
<span data-ttu-id="66471-706">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-706">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="66471-707">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="66471-707">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="66471-708">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-708">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="66471-709">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="66471-709">Method mouseDblClick</span></span>

<span data-ttu-id="66471-710">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-710">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="66471-711">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="66471-711">Parameters - mouseDblClick</span></span>

<span data-ttu-id="66471-712">x</span><span class="sxs-lookup"><span data-stu-id="66471-712">x</span></span>  
<span data-ttu-id="66471-713">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-713">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-714">y</span><span class="sxs-lookup"><span data-stu-id="66471-714">y</span></span>  
<span data-ttu-id="66471-715">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-715">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-716">ボタン</span><span class="sxs-lookup"><span data-stu-id="66471-716">button</span></span>  
<span data-ttu-id="66471-717">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-717">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-718">Ctrl</span><span class="sxs-lookup"><span data-stu-id="66471-718">Ctrl</span></span>  
<span data-ttu-id="66471-719">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-719">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-720">シフト</span><span class="sxs-lookup"><span data-stu-id="66471-720">Shift</span></span>  
<span data-ttu-id="66471-721">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-721">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="66471-722">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="66471-722">Return Value - mouseDblClick</span></span>

<span data-ttu-id="66471-723">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="66471-723">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="66471-724">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="66471-724">Remarks - mouseDblClick</span></span>

<span data-ttu-id="66471-725">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="66471-725">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="66471-726">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="66471-726">Method mouseDown</span></span>

<span data-ttu-id="66471-727">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-727">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="66471-728">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="66471-728">Parameters - mouseDown</span></span>

<span data-ttu-id="66471-729">x</span><span class="sxs-lookup"><span data-stu-id="66471-729">x</span></span>  
<span data-ttu-id="66471-730">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-730">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-731">y</span><span class="sxs-lookup"><span data-stu-id="66471-731">y</span></span>  
<span data-ttu-id="66471-732">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-732">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-733">ボタン</span><span class="sxs-lookup"><span data-stu-id="66471-733">button</span></span>  
<span data-ttu-id="66471-734">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-734">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-735">Ctrl</span><span class="sxs-lookup"><span data-stu-id="66471-735">Ctrl</span></span>  
<span data-ttu-id="66471-736">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-736">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-737">シフト</span><span class="sxs-lookup"><span data-stu-id="66471-737">Shift</span></span>  
<span data-ttu-id="66471-738">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-738">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="66471-739">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="66471-739">Return Value - mouseDown</span></span>

<span data-ttu-id="66471-740">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="66471-740">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="66471-741">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="66471-741">Remarks - mouseDown</span></span>

<span data-ttu-id="66471-742">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="66471-742">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="66471-743">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-743">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="66471-744">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="66471-744">Method mouseMove</span></span>

<span data-ttu-id="66471-745">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-745">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="66471-746">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="66471-746">Parameters - mouseMove</span></span>

<span data-ttu-id="66471-747">x</span><span class="sxs-lookup"><span data-stu-id="66471-747">x</span></span>  
<span data-ttu-id="66471-748">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-748">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-749">y</span><span class="sxs-lookup"><span data-stu-id="66471-749">y</span></span>  
<span data-ttu-id="66471-750">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-750">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-751">ボタン</span><span class="sxs-lookup"><span data-stu-id="66471-751">button</span></span>  
<span data-ttu-id="66471-752">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-752">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-753">Ctrl</span><span class="sxs-lookup"><span data-stu-id="66471-753">Ctrl</span></span>  
<span data-ttu-id="66471-754">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-754">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-755">シフト</span><span class="sxs-lookup"><span data-stu-id="66471-755">Shift</span></span>  
<span data-ttu-id="66471-756">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-756">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="66471-757">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="66471-757">Return Value - mouseMove</span></span>

<span data-ttu-id="66471-758">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="66471-758">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="66471-759">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="66471-759">Remarks - mouseMove</span></span>

<span data-ttu-id="66471-760">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="66471-760">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="66471-761">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="66471-761">Method mouseUp</span></span>

<span data-ttu-id="66471-762">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-762">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="66471-763">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="66471-763">Parameters - mouseUp</span></span>

<span data-ttu-id="66471-764">x</span><span class="sxs-lookup"><span data-stu-id="66471-764">x</span></span>  
<span data-ttu-id="66471-765">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-765">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-766">y</span><span class="sxs-lookup"><span data-stu-id="66471-766">y</span></span>  
<span data-ttu-id="66471-767">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-767">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-768">ボタン</span><span class="sxs-lookup"><span data-stu-id="66471-768">button</span></span>  
<span data-ttu-id="66471-769">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-769">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-770">Ctrl</span><span class="sxs-lookup"><span data-stu-id="66471-770">Ctrl</span></span>  
<span data-ttu-id="66471-771">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-771">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-772">シフト</span><span class="sxs-lookup"><span data-stu-id="66471-772">Shift</span></span>  
<span data-ttu-id="66471-773">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-773">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="66471-774">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="66471-774">Return Value - mouseUp</span></span>

<span data-ttu-id="66471-775">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="66471-775">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="66471-776">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="66471-776">Remarks - mouseUp</span></span>

<span data-ttu-id="66471-777">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="66471-777">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="66471-778">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-778">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="66471-779">メソッド名</span><span class="sxs-lookup"><span data-stu-id="66471-779">Method name</span></span>

<span data-ttu-id="66471-780">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-780">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="66471-781">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="66471-781">Parameters - name</span></span>

<span data-ttu-id="66471-782">値</span><span class="sxs-lookup"><span data-stu-id="66471-782">value</span></span>  
<span data-ttu-id="66471-783">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="66471-783">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="66471-784">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="66471-784">Return Value - name</span></span>

<span data-ttu-id="66471-785">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="66471-785">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="66471-786">備考 - name</span><span class="sxs-lookup"><span data-stu-id="66471-786">Remarks - name</span></span>

<span data-ttu-id="66471-787">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="66471-787">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="66471-788">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="66471-788">It must begin with a letter.</span></span>
-   <span data-ttu-id="66471-789">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="66471-789">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="66471-790">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="66471-790">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="66471-791">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="66471-791">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="66471-792">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="66471-792">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="66471-793">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="66471-793">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="66471-794">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="66471-794">Parameters - neededPermission</span></span>

<span data-ttu-id="66471-795">値</span><span class="sxs-lookup"><span data-stu-id="66471-795">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="66471-796">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="66471-796">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="66471-797">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="66471-797">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="66471-798">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="66471-798">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="66471-799">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="66471-799">Method parentControl</span></span>

<span data-ttu-id="66471-800">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-800">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="66471-801">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="66471-801">Return Value - parentControl</span></span>

<span data-ttu-id="66471-802">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="66471-802">The parent control for the control.</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="66471-803">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="66471-803">Method securityKey</span></span>

<span data-ttu-id="66471-804">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-804">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="66471-805">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="66471-805">Parameters - securityKey</span></span>

<span data-ttu-id="66471-806">値</span><span class="sxs-lookup"><span data-stu-id="66471-806">value</span></span>  
<span data-ttu-id="66471-807">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-807">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="66471-808">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="66471-808">Return Value - securityKey</span></span>

<span data-ttu-id="66471-809">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="66471-809">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="66471-810">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="66471-810">Method showContextMenu</span></span>

<span data-ttu-id="66471-811">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="66471-811">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="66471-812">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="66471-812">Parameters - showContextMenu</span></span>

<span data-ttu-id="66471-813">menuHandle</span><span class="sxs-lookup"><span data-stu-id="66471-813">menuHandle</span></span>  
<span data-ttu-id="66471-814">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="66471-814">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="66471-815">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="66471-815">Return Value - showContextMenu</span></span>

<span data-ttu-id="66471-816">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-816">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="66471-817">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="66471-817">Method skip</span></span>

<span data-ttu-id="66471-818">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-818">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="66471-819">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="66471-819">Parameters - skip</span></span>

<span data-ttu-id="66471-820">値</span><span class="sxs-lookup"><span data-stu-id="66471-820">value</span></span>  
<span data-ttu-id="66471-821">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-821">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="66471-822">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="66471-822">Return Value - skip</span></span>

<span data-ttu-id="66471-823">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="66471-823">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="66471-824">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="66471-824">Remarks - skip</span></span>

<span data-ttu-id="66471-825">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="66471-825">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="66471-826">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="66471-826">Method toolTip</span></span>

<span data-ttu-id="66471-827">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="66471-827">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="66471-828">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="66471-828">Return Value - toolTip</span></span>

<span data-ttu-id="66471-829">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="66471-829">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="66471-830">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="66471-830">Remarks - toolTip</span></span>

<span data-ttu-id="66471-831">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="66471-831">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="66471-832">メソッド top</span><span class="sxs-lookup"><span data-stu-id="66471-832">Method top</span></span>

<span data-ttu-id="66471-833">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-833">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="66471-834">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="66471-834">Parameters - top</span></span>

<span data-ttu-id="66471-835">値</span><span class="sxs-lookup"><span data-stu-id="66471-835">value</span></span>  
<span data-ttu-id="66471-836">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-836">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="66471-837">モード</span><span class="sxs-lookup"><span data-stu-id="66471-837">mode</span></span>  
<span data-ttu-id="66471-838">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-838">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="66471-839">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="66471-839">Return Value - top</span></span>

<span data-ttu-id="66471-840">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="66471-840">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="66471-841">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="66471-841">Method topMode</span></span>

<span data-ttu-id="66471-842">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-842">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="66471-843">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="66471-843">Parameters - topMode</span></span>

<span data-ttu-id="66471-844">値</span><span class="sxs-lookup"><span data-stu-id="66471-844">value</span></span>  
<span data-ttu-id="66471-845">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-845">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="66471-846">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="66471-846">Return Value - topMode</span></span>

<span data-ttu-id="66471-847">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="66471-847">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="66471-848">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="66471-848">Method topValue</span></span>

<span data-ttu-id="66471-849">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-849">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="66471-850">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="66471-850">Parameters - topValue</span></span>

<span data-ttu-id="66471-851">値</span><span class="sxs-lookup"><span data-stu-id="66471-851">value</span></span>  
<span data-ttu-id="66471-852">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-852">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="66471-853">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="66471-853">Return Value - topValue</span></span>

<span data-ttu-id="66471-854">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="66471-854">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="66471-855">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="66471-855">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="66471-856">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="66471-856">Parameters - type</span></span>

<span data-ttu-id="66471-857">値</span><span class="sxs-lookup"><span data-stu-id="66471-857">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="66471-858">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="66471-858">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="66471-859">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="66471-859">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="66471-860">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="66471-860">Parameters - underline</span></span>

<span data-ttu-id="66471-861">値</span><span class="sxs-lookup"><span data-stu-id="66471-861">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="66471-862">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="66471-862">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="66471-863">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="66471-863">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="66471-864">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="66471-864">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="66471-865">データ</span><span class="sxs-lookup"><span data-stu-id="66471-865">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="66471-866">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="66471-866">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="66471-867">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="66471-867">Method userData</span></span>

<span data-ttu-id="66471-868">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-868">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="66471-869">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="66471-869">Parameters - userData</span></span>

<span data-ttu-id="66471-870">値</span><span class="sxs-lookup"><span data-stu-id="66471-870">value</span></span>  
<span data-ttu-id="66471-871">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-871">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="66471-872">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="66471-872">Return Value - userData</span></span>

<span data-ttu-id="66471-873">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="66471-873">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="66471-874">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="66471-874">Method userDataItem</span></span>

<span data-ttu-id="66471-875">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-875">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="66471-876">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="66471-876">Parameters - userDataItem</span></span>

<span data-ttu-id="66471-877">値</span><span class="sxs-lookup"><span data-stu-id="66471-877">value</span></span>  
<span data-ttu-id="66471-878">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-878">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="66471-879">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="66471-879">Return Value - userDataItem</span></span>

<span data-ttu-id="66471-880">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="66471-880">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="66471-881">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="66471-881">Method userDataItems</span></span>

<span data-ttu-id="66471-882">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-882">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="66471-883">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="66471-883">Parameters - userDataItems</span></span>

<span data-ttu-id="66471-884">値</span><span class="sxs-lookup"><span data-stu-id="66471-884">value</span></span>  
<span data-ttu-id="66471-885">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-885">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="66471-886">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="66471-886">Return Value - userDataItems</span></span>

<span data-ttu-id="66471-887">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="66471-887">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="66471-888">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="66471-888">Method userDisable</span></span>

<span data-ttu-id="66471-889">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-889">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="66471-890">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="66471-890">Parameters - userDisable</span></span>

<span data-ttu-id="66471-891">値</span><span class="sxs-lookup"><span data-stu-id="66471-891">value</span></span>  
<span data-ttu-id="66471-892">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-892">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="66471-893">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="66471-893">Return Value - userDisable</span></span>

<span data-ttu-id="66471-894">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="66471-894">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="66471-895">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="66471-895">Method userHeight</span></span>

<span data-ttu-id="66471-896">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-896">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="66471-897">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="66471-897">Parameters - userHeight</span></span>

<span data-ttu-id="66471-898">値</span><span class="sxs-lookup"><span data-stu-id="66471-898">value</span></span>  
<span data-ttu-id="66471-899">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-899">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="66471-900">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="66471-900">Return Value - userHeight</span></span>

<span data-ttu-id="66471-901">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="66471-901">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="66471-902">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="66471-902">Method userHide</span></span>

<span data-ttu-id="66471-903">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-903">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="66471-904">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="66471-904">Parameters - userHide</span></span>

<span data-ttu-id="66471-905">値</span><span class="sxs-lookup"><span data-stu-id="66471-905">value</span></span>  
<span data-ttu-id="66471-906">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-906">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="66471-907">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="66471-907">Return Value - userHide</span></span>

<span data-ttu-id="66471-908">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="66471-908">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="66471-909">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="66471-909">Remarks - userHide</span></span>

<span data-ttu-id="66471-910">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="66471-910">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="66471-911">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="66471-911">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="66471-912">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="66471-912">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="66471-913">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="66471-913">Method userOrgContainer</span></span>

<span data-ttu-id="66471-914">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-914">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="66471-915">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="66471-915">Parameters - userOrgContainer</span></span>

<span data-ttu-id="66471-916">値</span><span class="sxs-lookup"><span data-stu-id="66471-916">value</span></span>  
<span data-ttu-id="66471-917">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-917">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="66471-918">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="66471-918">Return Value - userOrgContainer</span></span>

<span data-ttu-id="66471-919">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="66471-919">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="66471-920">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="66471-920">Method userOrgSibling</span></span>

<span data-ttu-id="66471-921">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-921">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="66471-922">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="66471-922">Parameters - userOrgSibling</span></span>

<span data-ttu-id="66471-923">値</span><span class="sxs-lookup"><span data-stu-id="66471-923">value</span></span>  
<span data-ttu-id="66471-924">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-924">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="66471-925">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="66471-925">Return Value - userOrgSibling</span></span>

<span data-ttu-id="66471-926">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="66471-926">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="66471-927">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="66471-927">Method userPromptText</span></span>

<span data-ttu-id="66471-928">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-928">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="66471-929">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="66471-929">Parameters - userPromptText</span></span>

<span data-ttu-id="66471-930">値</span><span class="sxs-lookup"><span data-stu-id="66471-930">value</span></span>  
<span data-ttu-id="66471-931">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-931">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="66471-932">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="66471-932">Return Value - userPromptText</span></span>

<span data-ttu-id="66471-933">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="66471-933">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="66471-934">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="66471-934">Method userSecurityLevel</span></span>

<span data-ttu-id="66471-935">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-935">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="66471-936">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="66471-936">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="66471-937">値</span><span class="sxs-lookup"><span data-stu-id="66471-937">value</span></span>  
<span data-ttu-id="66471-938">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-938">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="66471-939">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="66471-939">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="66471-940">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="66471-940">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="66471-941">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="66471-941">Method userSkip</span></span>

<span data-ttu-id="66471-942">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-942">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="66471-943">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="66471-943">Parameters - userSkip</span></span>

<span data-ttu-id="66471-944">値</span><span class="sxs-lookup"><span data-stu-id="66471-944">value</span></span>  
<span data-ttu-id="66471-945">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-945">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="66471-946">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="66471-946">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="66471-947">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="66471-947">Return Value - userSkip</span></span>

<span data-ttu-id="66471-948">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="66471-948">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="66471-949">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="66471-949">Method userWidth</span></span>

<span data-ttu-id="66471-950">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-950">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="66471-951">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="66471-951">Parameters - userWidth</span></span>

<span data-ttu-id="66471-952">値</span><span class="sxs-lookup"><span data-stu-id="66471-952">value</span></span>  
<span data-ttu-id="66471-953">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-953">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="66471-954">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="66471-954">Return Value - userWidth</span></span>

<span data-ttu-id="66471-955">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="66471-955">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="66471-956">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="66471-956">Remarks - userWidth</span></span>

<span data-ttu-id="66471-957">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="66471-957">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="66471-958">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="66471-958">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="66471-959">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="66471-959">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="66471-960">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="66471-960">Method verticalSpacing</span></span>

<span data-ttu-id="66471-961">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-961">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="66471-962">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="66471-962">Parameters - verticalSpacing</span></span>

<span data-ttu-id="66471-963">値</span><span class="sxs-lookup"><span data-stu-id="66471-963">value</span></span>  
<span data-ttu-id="66471-964">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-964">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="66471-965">モード</span><span class="sxs-lookup"><span data-stu-id="66471-965">mode</span></span>  
<span data-ttu-id="66471-966">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-966">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="66471-967">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="66471-967">Return Value - verticalSpacing</span></span>

<span data-ttu-id="66471-968">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="66471-968">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="66471-969">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="66471-969">Method verticalSpacingMode</span></span>

<span data-ttu-id="66471-970">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-970">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="66471-971">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="66471-971">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="66471-972">モード</span><span class="sxs-lookup"><span data-stu-id="66471-972">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="66471-973">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="66471-973">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="66471-974">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="66471-974">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="66471-975">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="66471-975">Method verticalSpacingValue</span></span>

<span data-ttu-id="66471-976">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-976">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="66471-977">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="66471-977">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="66471-978">値</span><span class="sxs-lookup"><span data-stu-id="66471-978">value</span></span>  
<span data-ttu-id="66471-979">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="66471-979">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="66471-980">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="66471-980">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="66471-981">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="66471-981">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="66471-982">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="66471-982">Method visible</span></span>

<span data-ttu-id="66471-983">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="66471-983">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="66471-984">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="66471-984">Parameters - visible</span></span>

<span data-ttu-id="66471-985">値</span><span class="sxs-lookup"><span data-stu-id="66471-985">value</span></span>  
<span data-ttu-id="66471-986">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-986">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="66471-987">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="66471-987">Return Value - visible</span></span>

<span data-ttu-id="66471-988">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="66471-988">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="66471-989">メソッド width</span><span class="sxs-lookup"><span data-stu-id="66471-989">Method width</span></span>

<span data-ttu-id="66471-990">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-990">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="66471-991">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="66471-991">Parameters - width</span></span>

<span data-ttu-id="66471-992">値</span><span class="sxs-lookup"><span data-stu-id="66471-992">value</span></span>  

<!-- -->

<span data-ttu-id="66471-993">モード</span><span class="sxs-lookup"><span data-stu-id="66471-993">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="66471-994">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="66471-994">Return Value - width</span></span>

<span data-ttu-id="66471-995">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="66471-995">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="66471-996">備考 - width</span><span class="sxs-lookup"><span data-stu-id="66471-996">Remarks - width</span></span>

<span data-ttu-id="66471-997">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="66471-997">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="66471-998">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="66471-998">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="66471-999">モード。</span><span class="sxs-lookup"><span data-stu-id="66471-999">Mode.</span></span>           | <span data-ttu-id="66471-1000">幅計算。</span><span class="sxs-lookup"><span data-stu-id="66471-1000">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66471-1001">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="66471-1001">-1 Exact.</span></span>       | <span data-ttu-id="66471-1002">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="66471-1002">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="66471-1003">0 自動。</span><span class="sxs-lookup"><span data-stu-id="66471-1003">0 Auto.</span></span>         | <span data-ttu-id="66471-1004">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="66471-1004">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="66471-1005">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="66471-1005">1 Column width.</span></span> | <span data-ttu-id="66471-1006">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="66471-1006">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="66471-1007">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="66471-1007">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="66471-1008">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="66471-1008">Method widthMode</span></span>

<span data-ttu-id="66471-1009">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-1009">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="66471-1010">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="66471-1010">Parameters - widthMode</span></span>

<span data-ttu-id="66471-1011">値</span><span class="sxs-lookup"><span data-stu-id="66471-1011">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="66471-1012">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="66471-1012">Return Value - widthMode</span></span>

<span data-ttu-id="66471-1013">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1013">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="66471-1014">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="66471-1014">Remarks - widthMode</span></span>

<span data-ttu-id="66471-1015">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="66471-1015">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="66471-1016">モード。</span><span class="sxs-lookup"><span data-stu-id="66471-1016">Mode.</span></span>         | <span data-ttu-id="66471-1017">幅計算。</span><span class="sxs-lookup"><span data-stu-id="66471-1017">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66471-1018">正確。</span><span class="sxs-lookup"><span data-stu-id="66471-1018">Exact.</span></span>        | <span data-ttu-id="66471-1019">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="66471-1019">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="66471-1020">自動。</span><span class="sxs-lookup"><span data-stu-id="66471-1020">Auto.</span></span>         | <span data-ttu-id="66471-1021">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="66471-1021">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="66471-1022">列の幅。</span><span class="sxs-lookup"><span data-stu-id="66471-1022">Column width.</span></span> | <span data-ttu-id="66471-1023">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="66471-1023">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="66471-1024">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="66471-1024">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="66471-1025">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="66471-1025">Method widthValue</span></span>

<span data-ttu-id="66471-1026">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-1026">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="66471-1027">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="66471-1027">Parameters - widthValue</span></span>

<span data-ttu-id="66471-1028">値</span><span class="sxs-lookup"><span data-stu-id="66471-1028">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="66471-1029">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="66471-1029">Return Value - widthValue</span></span>

<span data-ttu-id="66471-1030">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="66471-1030">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="66471-1031">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="66471-1031">Remarks - widthValue</span></span>

<span data-ttu-id="66471-1032">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="66471-1032">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-drop"></a><span data-ttu-id="66471-1033">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="66471-1033">Method drop</span></span>

<span data-ttu-id="66471-1034">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-1034">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="66471-1035">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="66471-1035">Parameters - drop</span></span>

<span data-ttu-id="66471-1036">dragSource</span><span class="sxs-lookup"><span data-stu-id="66471-1036">dragSource</span></span>  
<span data-ttu-id="66471-1037">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1037">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-1038">dragMode</span><span class="sxs-lookup"><span data-stu-id="66471-1038">dragMode</span></span>  
<span data-ttu-id="66471-1039">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1039">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-1040">x</span><span class="sxs-lookup"><span data-stu-id="66471-1040">x</span></span>  
<span data-ttu-id="66471-1041">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1041">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-1042">y</span><span class="sxs-lookup"><span data-stu-id="66471-1042">y</span></span>  
<span data-ttu-id="66471-1043">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1043">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-copy"></a><span data-ttu-id="66471-1044">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="66471-1044">Method copy</span></span>

<span data-ttu-id="66471-1045">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="66471-1045">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-cut"></a><span data-ttu-id="66471-1046">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="66471-1046">Method cut</span></span>

<span data-ttu-id="66471-1047">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="66471-1047">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-setfocus"></a><span data-ttu-id="66471-1048">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="66471-1048">Method setFocus</span></span>

<span data-ttu-id="66471-1049">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="66471-1049">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-mouseleave"></a><span data-ttu-id="66471-1050">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="66471-1050">Method mouseLeave</span></span>

<span data-ttu-id="66471-1051">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-1051">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-enddrag"></a><span data-ttu-id="66471-1052">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="66471-1052">Method endDrag</span></span>

<span data-ttu-id="66471-1053">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-1053">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="66471-1054">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="66471-1054">Remarks - endDrag</span></span>

<span data-ttu-id="66471-1055">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="66471-1055">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="66471-1056">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="66471-1056">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-context"></a><span data-ttu-id="66471-1057">メソッド context</span><span class="sxs-lookup"><span data-stu-id="66471-1057">Method context</span></span>

<span data-ttu-id="66471-1058">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="66471-1058">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-gotfocus"></a><span data-ttu-id="66471-1059">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="66471-1059">Method gotFocus</span></span>

<span data-ttu-id="66471-1060">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-1060">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="66471-1061">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="66471-1061">Method prefColumnSize</span></span>

<span data-ttu-id="66471-1062">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="66471-1062">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="66471-1063">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="66471-1063">Parameters - prefColumnSize</span></span>

<span data-ttu-id="66471-1064">width</span><span class="sxs-lookup"><span data-stu-id="66471-1064">width</span></span>  
<span data-ttu-id="66471-1065">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="66471-1065">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="66471-1066">height</span><span class="sxs-lookup"><span data-stu-id="66471-1066">height</span></span>  
<span data-ttu-id="66471-1067">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="66471-1067">The preferred height of the control.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="66471-1068">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="66471-1068">Method lostFocus</span></span>

<span data-ttu-id="66471-1069">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="66471-1069">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="66471-1070">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="66471-1070">Method displayControl</span></span>

<span data-ttu-id="66471-1071">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="66471-1071">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="66471-1072">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="66471-1072">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="66471-1073">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="66471-1073">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="66471-1074">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="66471-1074">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="66471-1075">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="66471-1075">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="66471-1076">overrideObject</span><span class="sxs-lookup"><span data-stu-id="66471-1076">overrideObject</span></span>  

## <a name="method-paste"></a><span data-ttu-id="66471-1077">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="66471-1077">Method paste</span></span>

<span data-ttu-id="66471-1078">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="66471-1078">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="66471-1079">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="66471-1079">Method resetUserSetting</span></span>

<span data-ttu-id="66471-1080">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="66471-1080">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-dropex"></a><span data-ttu-id="66471-1081">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="66471-1081">Method dropEx</span></span>

<span data-ttu-id="66471-1082">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-1082">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="66471-1083">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="66471-1083">Parameters - dropEx</span></span>

<span data-ttu-id="66471-1084">dragSource</span><span class="sxs-lookup"><span data-stu-id="66471-1084">dragSource</span></span>  
<span data-ttu-id="66471-1085">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1085">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-1086">dragMode</span><span class="sxs-lookup"><span data-stu-id="66471-1086">dragMode</span></span>  
<span data-ttu-id="66471-1087">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1087">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-1088">x</span><span class="sxs-lookup"><span data-stu-id="66471-1088">x</span></span>  
<span data-ttu-id="66471-1089">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1089">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="66471-1090">y</span><span class="sxs-lookup"><span data-stu-id="66471-1090">y</span></span>  
<span data-ttu-id="66471-1091">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="66471-1091">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="66471-1092">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="66471-1092">Method mouseEnter</span></span>

<span data-ttu-id="66471-1093">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66471-1093">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="66471-1094">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="66471-1094">Parameters - mouseEnter</span></span>

<span data-ttu-id="66471-1095">x</span><span class="sxs-lookup"><span data-stu-id="66471-1095">x</span></span>  
<span data-ttu-id="66471-1096">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-1096">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-1097">y</span><span class="sxs-lookup"><span data-stu-id="66471-1097">y</span></span>  
<span data-ttu-id="66471-1098">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-1098">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-1099">ボタン</span><span class="sxs-lookup"><span data-stu-id="66471-1099">button</span></span>  
<span data-ttu-id="66471-1100">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-1100">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-1101">Ctrl</span><span class="sxs-lookup"><span data-stu-id="66471-1101">Ctrl</span></span>  
<span data-ttu-id="66471-1102">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-1102">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="66471-1103">シフト</span><span class="sxs-lookup"><span data-stu-id="66471-1103">Shift</span></span>  
<span data-ttu-id="66471-1104">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="66471-1104">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-inputsearch"></a><span data-ttu-id="66471-1105">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="66471-1105">Method inputSearch</span></span>

<span data-ttu-id="66471-1106">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="66471-1106">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="66471-1107">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="66471-1107">Parameters - inputSearch</span></span>

<span data-ttu-id="66471-1108">searchStr</span><span class="sxs-lookup"><span data-stu-id="66471-1108">searchStr</span></span>  
<span data-ttu-id="66471-1109">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="66471-1109">The string value to use to filter data; optional.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="66471-1110">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="66471-1110">Method dragLeave</span></span>

<span data-ttu-id="66471-1111">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="66471-1111">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

