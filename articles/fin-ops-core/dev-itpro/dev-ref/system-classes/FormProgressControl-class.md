---
title: FormProgressControl クラス
description: このトピックでは、FormProgressControl クラスについて説明します。
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
ms.openlocfilehash: 3bb19328352ff0840834ab14c922b295442d690c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502915"
---
# <a name="class-formprogresscontrol"></a><span data-ttu-id="11901-103">クラス FormProgressControl</span><span class="sxs-lookup"><span data-stu-id="11901-103">Class FormProgressControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormProgressControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="11901-104">備考</span><span class="sxs-lookup"><span data-stu-id="11901-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="11901-105">例</span><span class="sxs-lookup"><span data-stu-id="11901-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="11901-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="11901-106">Methods</span></span>

| <span data-ttu-id="11901-107">方法</span><span class="sxs-lookup"><span data-stu-id="11901-107">Method</span></span>                                                                                                      | <span data-ttu-id="11901-108">説明</span><span class="sxs-lookup"><span data-stu-id="11901-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11901-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="11901-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="11901-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="11901-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="11901-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="11901-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="11901-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="11901-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="11901-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="11901-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="11901-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="11901-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="11901-117">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="11901-117">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="11901-118">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-118">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="11901-119">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="11901-119">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="11901-120">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-120">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="11901-121">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="11901-121">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="11901-122">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-122">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="11901-123">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="11901-123">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="11901-124">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-124">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="11901-125">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="11901-125">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="11901-126">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-126">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="11901-127">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="11901-127">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="11901-128">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-128">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="11901-129">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-129">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="11901-130">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-130">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="11901-131">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-131">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="11901-132">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-132">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="11901-133">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-133">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="11901-134">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="11901-134">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="11901-135">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-135">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="11901-136">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="11901-136">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="11901-137">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-137">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="11901-138">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="11901-138">public str dragText()</span></span>                                                                                       | <span data-ttu-id="11901-139">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-139">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="11901-140">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="11901-140">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="11901-141">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-141">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="11901-142">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="11901-142">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="11901-143">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-143">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="11901-144">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="11901-144">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="11901-145">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="11901-145">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="11901-146">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="11901-146">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="11901-147">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-147">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="11901-148">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-148">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="11901-149">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-149">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="11901-150">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-150">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="11901-151">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-151">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="11901-152">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="11901-152">public str helpField()</span></span>                                                                                      | <span data-ttu-id="11901-153">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-153">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="11901-154">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="11901-154">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="11901-155">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-155">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="11901-156">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="11901-156">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="11901-157">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-157">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="11901-158">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="11901-158">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="11901-159">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-159">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="11901-160">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="11901-160">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="11901-161">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="11901-161">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="11901-162">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-162">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="11901-163">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="11901-163">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="11901-164">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-164">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="11901-165">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="11901-165">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="11901-166">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="11901-166">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="11901-167">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="11901-167">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="11901-168">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="11901-168">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="11901-169">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-169">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="11901-170">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-170">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="11901-171">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-171">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="11901-172">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-172">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="11901-173">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-173">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="11901-174">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="11901-174">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="11901-175">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="11901-175">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="11901-176">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="11901-176">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="11901-177">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-177">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="11901-178">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="11901-178">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="11901-179">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-179">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="11901-180">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="11901-180">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="11901-181">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-181">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="11901-182">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="11901-182">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="11901-183">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-183">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="11901-184">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="11901-184">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="11901-185">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-185">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="11901-186">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-186">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="11901-187">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="11901-187">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="11901-188">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="11901-188">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="11901-189">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-189">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="11901-190">public int pos(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-190">public int pos(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="11901-191">public int progressType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-191">public int progressType(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="11901-192">public int rangeHi(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-192">public int rangeHi(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="11901-193">public int rangeLo(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-193">public int rangeLo(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="11901-194">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="11901-194">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="11901-195">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-195">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="11901-196">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="11901-196">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="11901-197">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="11901-197">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="11901-198">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="11901-198">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="11901-199">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-199">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="11901-200">public int step(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-200">public int step(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="11901-201">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-201">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="11901-202">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="11901-202">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="11901-203">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-203">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="11901-204">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="11901-204">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="11901-205">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-205">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="11901-206">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-206">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="11901-207">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-207">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="11901-208">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-208">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="11901-209">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-209">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="11901-210">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-210">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="11901-211">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="11901-211">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="11901-212">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-212">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="11901-213">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-213">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="11901-214">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-214">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="11901-215">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-215">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="11901-216">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-216">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="11901-217">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-217">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="11901-218">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-218">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="11901-219">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-219">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="11901-220">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-220">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="11901-221">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-221">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="11901-222">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-222">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="11901-223">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-223">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="11901-224">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-224">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="11901-225">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-225">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="11901-226">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-226">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="11901-227">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-227">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="11901-228">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="11901-228">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="11901-229">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-229">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="11901-230">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-230">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="11901-231">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-231">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="11901-232">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-232">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="11901-233">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-233">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="11901-234">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-234">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="11901-235">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-235">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="11901-236">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="11901-236">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="11901-237">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-237">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="11901-238">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="11901-238">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="11901-239">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-239">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="11901-240">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-240">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="11901-241">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-241">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="11901-242">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="11901-242">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="11901-243">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-243">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="11901-244">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="11901-244">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="11901-245">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-245">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="11901-246">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-246">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="11901-247">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-247">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="11901-248">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="11901-248">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="11901-249">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-249">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="11901-250">public void context()</span><span class="sxs-lookup"><span data-stu-id="11901-250">public void context()</span></span>                                                                                       | <span data-ttu-id="11901-251">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="11901-251">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="11901-252">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="11901-252">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="11901-253">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-253">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="11901-254">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="11901-254">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="11901-255">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="11901-255">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="11901-256">public void paste()</span><span class="sxs-lookup"><span data-stu-id="11901-256">public void paste()</span></span>                                                                                         | <span data-ttu-id="11901-257">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="11901-257">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="11901-258">public void enter()</span><span class="sxs-lookup"><span data-stu-id="11901-258">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="11901-259">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="11901-259">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="11901-260">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-260">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="11901-261">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="11901-261">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="11901-262">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="11901-262">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="11901-263">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-263">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="11901-264">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="11901-264">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="11901-265">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="11901-265">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="11901-266">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="11901-266">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="11901-267">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="11901-267">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="11901-268">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="11901-268">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="11901-269">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-269">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="11901-270">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="11901-270">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="11901-271">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="11901-271">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="11901-272">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-272">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="11901-273">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="11901-273">public void displayControl()</span></span>                                                                                | <span data-ttu-id="11901-274">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="11901-274">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="11901-275">public void cut()</span><span class="sxs-lookup"><span data-stu-id="11901-275">public void cut()</span></span>                                                                                           | <span data-ttu-id="11901-276">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="11901-276">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="11901-277">public void stepIt()</span><span class="sxs-lookup"><span data-stu-id="11901-277">public void stepIt()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="11901-278">public void deltaPos(int inc)</span><span class="sxs-lookup"><span data-stu-id="11901-278">public void deltaPos(int inc)</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="11901-279">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="11901-279">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="11901-280">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="11901-280">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="11901-281">public void copy()</span><span class="sxs-lookup"><span data-stu-id="11901-281">public void copy()</span></span>                                                                                          | <span data-ttu-id="11901-282">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="11901-282">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="11901-283">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="11901-283">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="11901-284">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="11901-284">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="11901-285">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="11901-285">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="11901-286">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="11901-286">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="11901-287">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-287">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="11901-288">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="11901-288">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="11901-289">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="11901-289">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="11901-290">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="11901-290">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="11901-291">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="11901-291">Indicates that the control has received focus.</span></span>                                                                                                                          |

## <a name="method-aligncontrol"></a><span data-ttu-id="11901-292">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="11901-292">Method alignControl</span></span>

<span data-ttu-id="11901-293">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-293">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="11901-294">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="11901-294">Parameters - alignControl</span></span>

<span data-ttu-id="11901-295">値</span><span class="sxs-lookup"><span data-stu-id="11901-295">value</span></span>  
<span data-ttu-id="11901-296">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-296">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="11901-297">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="11901-297">Return Value - alignControl</span></span>

<span data-ttu-id="11901-298">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="11901-298">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="11901-299">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="11901-299">Remarks - alignControl</span></span>

<span data-ttu-id="11901-300">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="11901-300">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="11901-301">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="11901-301">Method allowEdit</span></span>

<span data-ttu-id="11901-302">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-302">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="11901-303">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="11901-303">Parameters - allowEdit</span></span>

<span data-ttu-id="11901-304">値</span><span class="sxs-lookup"><span data-stu-id="11901-304">value</span></span>  
<span data-ttu-id="11901-305">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="11901-305">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="11901-306">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="11901-306">Return Value - allowEdit</span></span>

<span data-ttu-id="11901-307">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="11901-307">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="11901-308">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="11901-308">Remarks - allowEdit</span></span>

<span data-ttu-id="11901-309">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="11901-309">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="11901-310">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="11901-310">Method allowSysSetup</span></span>

<span data-ttu-id="11901-311">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-311">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="11901-312">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="11901-312">Return Value - allowSysSetup</span></span>

<span data-ttu-id="11901-313">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="11901-313">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="11901-314">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="11901-314">Method autoDeclaration</span></span>

<span data-ttu-id="11901-315">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-315">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="11901-316">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="11901-316">Parameters - autoDeclaration</span></span>

<span data-ttu-id="11901-317">値</span><span class="sxs-lookup"><span data-stu-id="11901-317">value</span></span>  
<span data-ttu-id="11901-318">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-318">The new value for the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="11901-319">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="11901-319">Return Value - autoDeclaration</span></span>

<span data-ttu-id="11901-320">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="11901-320">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="11901-321">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="11901-321">Remarks - autoDeclaration</span></span>

<span data-ttu-id="11901-322">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="11901-322">Controls cannot have identical names.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="11901-323">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="11901-323">Method beginDrag</span></span>

<span data-ttu-id="11901-324">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-324">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="11901-325">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="11901-325">Parameters - beginDrag</span></span>

<span data-ttu-id="11901-326">x</span><span class="sxs-lookup"><span data-stu-id="11901-326">x</span></span>  
<span data-ttu-id="11901-327">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-327">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="11901-328">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="11901-328">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="11901-329">y</span><span class="sxs-lookup"><span data-stu-id="11901-329">y</span></span>  
<span data-ttu-id="11901-330">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-330">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="11901-331">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="11901-331">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="11901-332">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="11901-332">Return Value - beginDrag</span></span>

<span data-ttu-id="11901-333">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="11901-333">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="11901-334">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="11901-334">Remarks - beginDrag</span></span>

<span data-ttu-id="11901-335">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="11901-335">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="11901-336">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="11901-336">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="11901-337">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="11901-337">Method calcControlSize</span></span>

<span data-ttu-id="11901-338">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-338">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="11901-339">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="11901-339">Parameters - calcControlSize</span></span>

<span data-ttu-id="11901-340">chars</span><span class="sxs-lookup"><span data-stu-id="11901-340">chars</span></span>  
<span data-ttu-id="11901-341">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="11901-341">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="11901-342">明細行</span><span class="sxs-lookup"><span data-stu-id="11901-342">lines</span></span>  
<span data-ttu-id="11901-343">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="11901-343">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="11901-344">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="11901-344">Return Value - calcControlSize</span></span>

<span data-ttu-id="11901-345">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="11901-345">The container that holds the width and height.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="11901-346">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="11901-346">Method configurationKey</span></span>

<span data-ttu-id="11901-347">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-347">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="11901-348">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="11901-348">Parameters - configurationKey</span></span>

<span data-ttu-id="11901-349">値</span><span class="sxs-lookup"><span data-stu-id="11901-349">value</span></span>  
<span data-ttu-id="11901-350">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-350">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="11901-351">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="11901-351">Return Value - configurationKey</span></span>

<span data-ttu-id="11901-352">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="11901-352">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="11901-353">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="11901-353">Remarks - configurationKey</span></span>

<span data-ttu-id="11901-354">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="11901-354">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="11901-355">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="11901-355">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="11901-356">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="11901-356">Method configurationKeyEx</span></span>

<span data-ttu-id="11901-357">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-357">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="11901-358">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="11901-358">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="11901-359">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="11901-359">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="11901-360">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="11901-360">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="11901-361">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="11901-361">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="11901-362">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="11901-362">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="11901-363">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="11901-363">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="11901-364">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="11901-364">Method countryRegionCodes</span></span>

<span data-ttu-id="11901-365">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-365">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="11901-366">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="11901-366">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="11901-367">値</span><span class="sxs-lookup"><span data-stu-id="11901-367">value</span></span>  
<span data-ttu-id="11901-368">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-368">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="11901-369">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="11901-369">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="11901-370">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="11901-370">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="11901-371">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="11901-371">Method dataRelationPath</span></span>

<span data-ttu-id="11901-372">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-372">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="11901-373">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="11901-373">Parameters - dataRelationPath</span></span>

<span data-ttu-id="11901-374">値</span><span class="sxs-lookup"><span data-stu-id="11901-374">value</span></span>  
<span data-ttu-id="11901-375">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-375">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="11901-376">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="11901-376">Return Value - dataRelationPath</span></span>

<span data-ttu-id="11901-377">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="11901-377">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="11901-378">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="11901-378">Remarks - dataRelationPath</span></span>

<span data-ttu-id="11901-379">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="11901-379">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="11901-380">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="11901-380">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-direction"></a><span data-ttu-id="11901-381">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="11901-381">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="11901-382">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="11901-382">Parameters - direction</span></span>

<span data-ttu-id="11901-383">値</span><span class="sxs-lookup"><span data-stu-id="11901-383">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="11901-384">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="11901-384">Return Value - direction</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="11901-385">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="11901-385">Method displayTarget</span></span>

<span data-ttu-id="11901-386">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-386">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="11901-387">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="11901-387">Parameters - displayTarget</span></span>

<span data-ttu-id="11901-388">値</span><span class="sxs-lookup"><span data-stu-id="11901-388">value</span></span>  
<span data-ttu-id="11901-389">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-389">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="11901-390">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="11901-390">Return Value - displayTarget</span></span>

<span data-ttu-id="11901-391">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="11901-391">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="11901-392">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="11901-392">Method dragDrop</span></span>

<span data-ttu-id="11901-393">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-393">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="11901-394">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="11901-394">Parameters - dragDrop</span></span>

<span data-ttu-id="11901-395">値</span><span class="sxs-lookup"><span data-stu-id="11901-395">value</span></span>  
<span data-ttu-id="11901-396">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-396">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="11901-397">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="11901-397">Return Value - dragDrop</span></span>

<span data-ttu-id="11901-398">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="11901-398">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="11901-399">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="11901-399">Remarks - dragDrop</span></span>

<span data-ttu-id="11901-400">dragLeave、dragOver、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="11901-400">Use the dragLeave, the dragOver, and dragOverEx methods to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="11901-401">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="11901-401">Method dragOver</span></span>

<span data-ttu-id="11901-402">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-402">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="11901-403">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="11901-403">Parameters - dragOver</span></span>

<span data-ttu-id="11901-404">dragSource</span><span class="sxs-lookup"><span data-stu-id="11901-404">dragSource</span></span>  
<span data-ttu-id="11901-405">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-405">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-406">dragMode</span><span class="sxs-lookup"><span data-stu-id="11901-406">dragMode</span></span>  
<span data-ttu-id="11901-407">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-407">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-408">x</span><span class="sxs-lookup"><span data-stu-id="11901-408">x</span></span>  
<span data-ttu-id="11901-409">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-409">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-410">y</span><span class="sxs-lookup"><span data-stu-id="11901-410">y</span></span>  
<span data-ttu-id="11901-411">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-411">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="11901-412">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="11901-412">Return Value - dragOver</span></span>

<span data-ttu-id="11901-413">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="11901-413">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="11901-414">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="11901-414">Method dragOverEx</span></span>

<span data-ttu-id="11901-415">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-415">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="11901-416">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="11901-416">Parameters - dragOverEx</span></span>

<span data-ttu-id="11901-417">dragSource</span><span class="sxs-lookup"><span data-stu-id="11901-417">dragSource</span></span>  
<span data-ttu-id="11901-418">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-418">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-419">dragMode</span><span class="sxs-lookup"><span data-stu-id="11901-419">dragMode</span></span>  
<span data-ttu-id="11901-420">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-420">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-421">x</span><span class="sxs-lookup"><span data-stu-id="11901-421">x</span></span>  
<span data-ttu-id="11901-422">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-422">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-423">y</span><span class="sxs-lookup"><span data-stu-id="11901-423">y</span></span>  
<span data-ttu-id="11901-424">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-424">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="11901-425">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="11901-425">Return Value - dragOverEx</span></span>

<span data-ttu-id="11901-426">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="11901-426">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="11901-427">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="11901-427">Method dragText</span></span>

<span data-ttu-id="11901-428">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-428">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="11901-429">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="11901-429">Return Value - dragText</span></span>

<span data-ttu-id="11901-430">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="11901-430">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="11901-431">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="11901-431">Method enabled</span></span>

<span data-ttu-id="11901-432">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="11901-432">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="11901-433">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="11901-433">Parameters - enabled</span></span>

<span data-ttu-id="11901-434">値</span><span class="sxs-lookup"><span data-stu-id="11901-434">value</span></span>  
<span data-ttu-id="11901-435">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-435">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="11901-436">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="11901-436">Return Value - enabled</span></span>

<span data-ttu-id="11901-437">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="11901-437">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="11901-438">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="11901-438">Remarks - enabled</span></span>

<span data-ttu-id="11901-439">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="11901-439">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="11901-440">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="11901-440">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="11901-441">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="11901-441">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="11901-442">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="11901-442">Method hasChanged</span></span>

<span data-ttu-id="11901-443">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-443">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="11901-444">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="11901-444">Parameters - hasChanged</span></span>

<span data-ttu-id="11901-445">val</span><span class="sxs-lookup"><span data-stu-id="11901-445">val</span></span>  
<span data-ttu-id="11901-446">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-446">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="11901-447">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="11901-447">Return Value - hasChanged</span></span>

<span data-ttu-id="11901-448">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="11901-448">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="11901-449">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="11901-449">Method hasUserSetting</span></span>

<span data-ttu-id="11901-450">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="11901-450">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="11901-451">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="11901-451">Return Value - hasUserSetting</span></span>

<span data-ttu-id="11901-452">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="11901-452">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="11901-453">メソッド height</span><span class="sxs-lookup"><span data-stu-id="11901-453">Method height</span></span>

<span data-ttu-id="11901-454">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-454">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="11901-455">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="11901-455">Parameters - height</span></span>

<span data-ttu-id="11901-456">値</span><span class="sxs-lookup"><span data-stu-id="11901-456">value</span></span>  
<span data-ttu-id="11901-457">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-457">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="11901-458">モード</span><span class="sxs-lookup"><span data-stu-id="11901-458">mode</span></span>  
<span data-ttu-id="11901-459">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-459">An integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="11901-460">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="11901-460">Return Value - height</span></span>

<span data-ttu-id="11901-461">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="11901-461">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="11901-462">備考 - height</span><span class="sxs-lookup"><span data-stu-id="11901-462">Remarks - height</span></span>

<span data-ttu-id="11901-463">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="11901-463">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="11901-464">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="11901-464">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="11901-465">モード</span><span class="sxs-lookup"><span data-stu-id="11901-465">Mode</span></span>            | <span data-ttu-id="11901-466">高さの計算</span><span class="sxs-lookup"><span data-stu-id="11901-466">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="11901-467">-1 正確</span><span class="sxs-lookup"><span data-stu-id="11901-467">-1 Exact</span></span>        | <span data-ttu-id="11901-468">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="11901-468">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="11901-469">0 自動</span><span class="sxs-lookup"><span data-stu-id="11901-469">0 Auto</span></span>          | <span data-ttu-id="11901-470">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="11901-470">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="11901-471">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="11901-471">1 Column height</span></span> | <span data-ttu-id="11901-472">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="11901-472">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="11901-473">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="11901-473">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="11901-474">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="11901-474">Method heightMode</span></span>

<span data-ttu-id="11901-475">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-475">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="11901-476">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="11901-476">Parameters - heightMode</span></span>

<span data-ttu-id="11901-477">値</span><span class="sxs-lookup"><span data-stu-id="11901-477">value</span></span>  
<span data-ttu-id="11901-478">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-478">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="11901-479">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="11901-479">Return Value - heightMode</span></span>

<span data-ttu-id="11901-480">計算モード。</span><span class="sxs-lookup"><span data-stu-id="11901-480">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="11901-481">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="11901-481">Remarks - heightMode</span></span>

<span data-ttu-id="11901-482">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="11901-482">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="11901-483">モード</span><span class="sxs-lookup"><span data-stu-id="11901-483">Mode</span></span>          | <span data-ttu-id="11901-484">高さの計算</span><span class="sxs-lookup"><span data-stu-id="11901-484">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="11901-485">正確</span><span class="sxs-lookup"><span data-stu-id="11901-485">Exact</span></span>         | <span data-ttu-id="11901-486">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="11901-486">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="11901-487">自動</span><span class="sxs-lookup"><span data-stu-id="11901-487">Auto</span></span>          | <span data-ttu-id="11901-488">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="11901-488">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="11901-489">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="11901-489">Column height</span></span> | <span data-ttu-id="11901-490">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="11901-490">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="11901-491">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="11901-491">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="11901-492">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="11901-492">Method heightValue</span></span>

<span data-ttu-id="11901-493">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-493">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="11901-494">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="11901-494">Parameters - heightValue</span></span>

<span data-ttu-id="11901-495">値</span><span class="sxs-lookup"><span data-stu-id="11901-495">value</span></span>  
<span data-ttu-id="11901-496">高さをピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-496">An integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="11901-497">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="11901-497">Return Value - heightValue</span></span>

<span data-ttu-id="11901-498">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="11901-498">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="11901-499">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="11901-499">Remarks - heightValue</span></span>

<span data-ttu-id="11901-500">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="11901-500">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="11901-501">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="11901-501">Method helpField</span></span>

<span data-ttu-id="11901-502">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-502">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="11901-503">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="11901-503">Return Value - helpField</span></span>

<span data-ttu-id="11901-504">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="11901-504">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="11901-505">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="11901-505">Remarks - helpField</span></span>

<span data-ttu-id="11901-506">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="11901-506">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="11901-507">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="11901-507">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="11901-508">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="11901-508">Method helpText</span></span>

<span data-ttu-id="11901-509">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-509">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="11901-510">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="11901-510">Parameters - helpText</span></span>

<span data-ttu-id="11901-511">値</span><span class="sxs-lookup"><span data-stu-id="11901-511">value</span></span>  
<span data-ttu-id="11901-512">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="11901-512">The value to assign as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="11901-513">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="11901-513">Return Value - helpText</span></span>

<span data-ttu-id="11901-514">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="11901-514">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="11901-515">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="11901-515">Remarks - helpText</span></span>

<span data-ttu-id="11901-516">このメソッドは、プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-516">This method sets the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="11901-517">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="11901-517">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="11901-518">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="11901-518">Method hierarchyParent</span></span>

<span data-ttu-id="11901-519">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-519">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="11901-520">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="11901-520">Parameters - hierarchyParent</span></span>

<span data-ttu-id="11901-521">値</span><span class="sxs-lookup"><span data-stu-id="11901-521">value</span></span>  
<span data-ttu-id="11901-522">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="11901-522">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="11901-523">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="11901-523">Return Value - hierarchyParent</span></span>

<span data-ttu-id="11901-524">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="11901-524">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="11901-525">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="11901-525">Method hWnd</span></span>

<span data-ttu-id="11901-526">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-526">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="11901-527">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="11901-527">Return Value - hWnd</span></span>

<span data-ttu-id="11901-528">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="11901-528">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="11901-529">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="11901-529">Remarks - hWnd</span></span>

<span data-ttu-id="11901-530">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="11901-530">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="11901-531">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="11901-531">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="11901-532">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="11901-532">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="11901-533">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="11901-533">Method isDisplayed</span></span>

<span data-ttu-id="11901-534">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-534">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="11901-535">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="11901-535">Return Value - isDisplayed</span></span>

<span data-ttu-id="11901-536">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="11901-536">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="11901-537">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="11901-537">Remarks - isDisplayed</span></span>

<span data-ttu-id="11901-538">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="11901-538">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="11901-539">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="11901-539">Method isRestricted</span></span>

<span data-ttu-id="11901-540">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-540">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="11901-541">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="11901-541">Return Value - isRestricted</span></span>

<span data-ttu-id="11901-542">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="11901-542">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="11901-543">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="11901-543">Method isUserSetupEnabled</span></span>

<span data-ttu-id="11901-544">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="11901-544">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="11901-545">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="11901-545">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="11901-546">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="11901-546">neededSetupRights</span></span>  
<span data-ttu-id="11901-547">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="11901-547">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="11901-548">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="11901-548">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="11901-549">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="11901-549">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="11901-550">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="11901-550">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="11901-551">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="11901-551">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="11901-552">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="11901-552">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11901-553">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="11901-553">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="11901-554">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="11901-554">No changes can be made to the control.</span></span> <span data-ttu-id="11901-555">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="11901-555">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="11901-556">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="11901-556">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="11901-557">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="11901-557">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="11901-558">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="11901-558">The user cannot move the control.</span></span>   |
| <span data-ttu-id="11901-559">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="11901-559">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="11901-560">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="11901-560">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="11901-561">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="11901-561">The user can also move the control.</span></span> |

## <a name="method-leave"></a><span data-ttu-id="11901-562">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="11901-562">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="11901-563">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="11901-563">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="11901-564">メソッド left</span><span class="sxs-lookup"><span data-stu-id="11901-564">Method left</span></span>

<span data-ttu-id="11901-565">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-565">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="11901-566">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="11901-566">Parameters - left</span></span>

<span data-ttu-id="11901-567">値</span><span class="sxs-lookup"><span data-stu-id="11901-567">value</span></span>  
<span data-ttu-id="11901-568">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-568">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="11901-569">モード</span><span class="sxs-lookup"><span data-stu-id="11901-569">mode</span></span>  
<span data-ttu-id="11901-570">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-570">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="11901-571">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="11901-571">Return Value - left</span></span>

<span data-ttu-id="11901-572">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="11901-572">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="11901-573">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="11901-573">Method leftMode</span></span>

<span data-ttu-id="11901-574">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-574">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="11901-575">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="11901-575">Parameters - leftMode</span></span>

<span data-ttu-id="11901-576">値</span><span class="sxs-lookup"><span data-stu-id="11901-576">value</span></span>  
<span data-ttu-id="11901-577">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-577">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="11901-578">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="11901-578">Return Value - leftMode</span></span>

<span data-ttu-id="11901-579">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="11901-579">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="11901-580">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="11901-580">Method leftValue</span></span>

<span data-ttu-id="11901-581">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-581">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="11901-582">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="11901-582">Parameters - leftValue</span></span>

<span data-ttu-id="11901-583">値</span><span class="sxs-lookup"><span data-stu-id="11901-583">value</span></span>  
<span data-ttu-id="11901-584">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-584">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="11901-585">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="11901-585">Return Value - leftValue</span></span>

<span data-ttu-id="11901-586">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="11901-586">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="11901-587">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="11901-587">Method markAsUserAdd</span></span>

<span data-ttu-id="11901-588">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="11901-588">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="11901-589">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="11901-589">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="11901-590">値</span><span class="sxs-lookup"><span data-stu-id="11901-590">value</span></span>  
<span data-ttu-id="11901-591">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-591">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="11901-592">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="11901-592">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="11901-593">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="11901-593">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="11901-594">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="11901-594">Method mouseDblClick</span></span>

<span data-ttu-id="11901-595">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-595">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="11901-596">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="11901-596">Parameters - mouseDblClick</span></span>

<span data-ttu-id="11901-597">x</span><span class="sxs-lookup"><span data-stu-id="11901-597">x</span></span>  
<span data-ttu-id="11901-598">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-598">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-599">y</span><span class="sxs-lookup"><span data-stu-id="11901-599">y</span></span>  
<span data-ttu-id="11901-600">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-600">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-601">ボタン</span><span class="sxs-lookup"><span data-stu-id="11901-601">button</span></span>  
<span data-ttu-id="11901-602">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-602">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-603">Ctrl</span><span class="sxs-lookup"><span data-stu-id="11901-603">Ctrl</span></span>  
<span data-ttu-id="11901-604">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-604">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-605">シフト</span><span class="sxs-lookup"><span data-stu-id="11901-605">Shift</span></span>  
<span data-ttu-id="11901-606">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-606">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="11901-607">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="11901-607">Return Value - mouseDblClick</span></span>

<span data-ttu-id="11901-608">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="11901-608">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="11901-609">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="11901-609">Remarks - mouseDblClick</span></span>

<span data-ttu-id="11901-610">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="11901-610">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="11901-611">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="11901-611">Method mouseDown</span></span>

<span data-ttu-id="11901-612">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-612">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="11901-613">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="11901-613">Parameters - mouseDown</span></span>

<span data-ttu-id="11901-614">x</span><span class="sxs-lookup"><span data-stu-id="11901-614">x</span></span>  
<span data-ttu-id="11901-615">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-615">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-616">y</span><span class="sxs-lookup"><span data-stu-id="11901-616">y</span></span>  
<span data-ttu-id="11901-617">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-617">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-618">ボタン</span><span class="sxs-lookup"><span data-stu-id="11901-618">button</span></span>  
<span data-ttu-id="11901-619">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-619">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-620">Ctrl</span><span class="sxs-lookup"><span data-stu-id="11901-620">Ctrl</span></span>  
<span data-ttu-id="11901-621">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-621">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-622">シフト</span><span class="sxs-lookup"><span data-stu-id="11901-622">Shift</span></span>  
<span data-ttu-id="11901-623">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-623">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="11901-624">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="11901-624">Return Value - mouseDown</span></span>

<span data-ttu-id="11901-625">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="11901-625">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="11901-626">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="11901-626">Remarks - mouseDown</span></span>

<span data-ttu-id="11901-627">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="11901-627">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="11901-628">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-628">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="11901-629">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="11901-629">Method mouseMove</span></span>

<span data-ttu-id="11901-630">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-630">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="11901-631">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="11901-631">Parameters - mouseMove</span></span>

<span data-ttu-id="11901-632">x</span><span class="sxs-lookup"><span data-stu-id="11901-632">x</span></span>  
<span data-ttu-id="11901-633">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-633">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-634">y</span><span class="sxs-lookup"><span data-stu-id="11901-634">y</span></span>  
<span data-ttu-id="11901-635">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-635">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-636">ボタン</span><span class="sxs-lookup"><span data-stu-id="11901-636">button</span></span>  
<span data-ttu-id="11901-637">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-637">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-638">Ctrl</span><span class="sxs-lookup"><span data-stu-id="11901-638">Ctrl</span></span>  
<span data-ttu-id="11901-639">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-639">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-640">シフト</span><span class="sxs-lookup"><span data-stu-id="11901-640">Shift</span></span>  
<span data-ttu-id="11901-641">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-641">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="11901-642">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="11901-642">Return Value - mouseMove</span></span>

<span data-ttu-id="11901-643">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="11901-643">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="11901-644">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="11901-644">Remarks - mouseMove</span></span>

<span data-ttu-id="11901-645">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="11901-645">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="11901-646">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="11901-646">Method mouseUp</span></span>

<span data-ttu-id="11901-647">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-647">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="11901-648">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="11901-648">Parameters - mouseUp</span></span>

<span data-ttu-id="11901-649">x</span><span class="sxs-lookup"><span data-stu-id="11901-649">x</span></span>  
<span data-ttu-id="11901-650">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-650">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-651">y</span><span class="sxs-lookup"><span data-stu-id="11901-651">y</span></span>  
<span data-ttu-id="11901-652">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-652">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-653">ボタン</span><span class="sxs-lookup"><span data-stu-id="11901-653">button</span></span>  
<span data-ttu-id="11901-654">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-654">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-655">Ctrl</span><span class="sxs-lookup"><span data-stu-id="11901-655">Ctrl</span></span>  
<span data-ttu-id="11901-656">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-656">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-657">シフト</span><span class="sxs-lookup"><span data-stu-id="11901-657">Shift</span></span>  
<span data-ttu-id="11901-658">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-658">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="11901-659">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="11901-659">Return Value - mouseUp</span></span>

<span data-ttu-id="11901-660">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="11901-660">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="11901-661">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="11901-661">Remarks - mouseUp</span></span>

<span data-ttu-id="11901-662">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="11901-662">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="11901-663">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-663">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="11901-664">メソッド名</span><span class="sxs-lookup"><span data-stu-id="11901-664">Method name</span></span>

<span data-ttu-id="11901-665">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-665">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="11901-666">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="11901-666">Parameters - name</span></span>

<span data-ttu-id="11901-667">値</span><span class="sxs-lookup"><span data-stu-id="11901-667">value</span></span>  
<span data-ttu-id="11901-668">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="11901-668">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="11901-669">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="11901-669">Return Value - name</span></span>

<span data-ttu-id="11901-670">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="11901-670">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="11901-671">備考 - name</span><span class="sxs-lookup"><span data-stu-id="11901-671">Remarks - name</span></span>

<span data-ttu-id="11901-672">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="11901-672">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="11901-673">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="11901-673">It must start with a letter.</span></span>
-   <span data-ttu-id="11901-674">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="11901-674">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="11901-675">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="11901-675">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="11901-676">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="11901-676">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="11901-677">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="11901-677">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="11901-678">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="11901-678">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="11901-679">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="11901-679">Parameters - neededPermission</span></span>

<span data-ttu-id="11901-680">値</span><span class="sxs-lookup"><span data-stu-id="11901-680">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="11901-681">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="11901-681">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="11901-682">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="11901-682">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="11901-683">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="11901-683">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="11901-684">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="11901-684">Method parentControl</span></span>

<span data-ttu-id="11901-685">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-685">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="11901-686">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="11901-686">Return Value - parentControl</span></span>

<span data-ttu-id="11901-687">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="11901-687">The parent control for the control.</span></span>

## <a name="method-pos"></a><span data-ttu-id="11901-688">メソッド pos</span><span class="sxs-lookup"><span data-stu-id="11901-688">Method pos</span></span>

```xpp
public int pos([int value])
```

### <a name="parameters---pos"></a><span data-ttu-id="11901-689">パラメーター - pos</span><span class="sxs-lookup"><span data-stu-id="11901-689">Parameters - pos</span></span>

<span data-ttu-id="11901-690">値</span><span class="sxs-lookup"><span data-stu-id="11901-690">value</span></span>  

### <a name="return-value---pos"></a><span data-ttu-id="11901-691">戻り値 - pos</span><span class="sxs-lookup"><span data-stu-id="11901-691">Return Value - pos</span></span>

## <a name="method-progresstype"></a><span data-ttu-id="11901-692">メソッド progressType</span><span class="sxs-lookup"><span data-stu-id="11901-692">Method progressType</span></span>

```xpp
public int progressType([int value])
```

### <a name="parameters---progresstype"></a><span data-ttu-id="11901-693">パラメーター - progressType</span><span class="sxs-lookup"><span data-stu-id="11901-693">Parameters - progressType</span></span>

<span data-ttu-id="11901-694">値</span><span class="sxs-lookup"><span data-stu-id="11901-694">value</span></span>  

### <a name="return-value---progresstype"></a><span data-ttu-id="11901-695">戻り値 - progressType</span><span class="sxs-lookup"><span data-stu-id="11901-695">Return Value - progressType</span></span>

## <a name="method-rangehi"></a><span data-ttu-id="11901-696">メソッド rangeHi</span><span class="sxs-lookup"><span data-stu-id="11901-696">Method rangeHi</span></span>

```xpp
public int rangeHi([int value])
```

### <a name="parameters---rangehi"></a><span data-ttu-id="11901-697">パラメーター - rangeHi</span><span class="sxs-lookup"><span data-stu-id="11901-697">Parameters - rangeHi</span></span>

<span data-ttu-id="11901-698">値</span><span class="sxs-lookup"><span data-stu-id="11901-698">value</span></span>  

### <a name="return-value---rangehi"></a><span data-ttu-id="11901-699">戻り値 - rangeHi</span><span class="sxs-lookup"><span data-stu-id="11901-699">Return Value - rangeHi</span></span>

## <a name="method-rangelo"></a><span data-ttu-id="11901-700">メソッド rangeLo</span><span class="sxs-lookup"><span data-stu-id="11901-700">Method rangeLo</span></span>

```xpp
public int rangeLo([int value])
```

### <a name="parameters---rangelo"></a><span data-ttu-id="11901-701">パラメーター - rangeLo</span><span class="sxs-lookup"><span data-stu-id="11901-701">Parameters - rangeLo</span></span>

<span data-ttu-id="11901-702">値</span><span class="sxs-lookup"><span data-stu-id="11901-702">value</span></span>  

### <a name="return-value---rangelo"></a><span data-ttu-id="11901-703">戻り値 - rangeLo</span><span class="sxs-lookup"><span data-stu-id="11901-703">Return Value - rangeLo</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="11901-704">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="11901-704">Method securityKey</span></span>

<span data-ttu-id="11901-705">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-705">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="11901-706">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="11901-706">Parameters - securityKey</span></span>

<span data-ttu-id="11901-707">値</span><span class="sxs-lookup"><span data-stu-id="11901-707">value</span></span>  
<span data-ttu-id="11901-708">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-708">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="11901-709">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="11901-709">Return Value - securityKey</span></span>

<span data-ttu-id="11901-710">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="11901-710">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="11901-711">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="11901-711">Method showContextMenu</span></span>

<span data-ttu-id="11901-712">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="11901-712">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="11901-713">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="11901-713">Parameters - showContextMenu</span></span>

<span data-ttu-id="11901-714">menuHandle</span><span class="sxs-lookup"><span data-stu-id="11901-714">menuHandle</span></span>  
<span data-ttu-id="11901-715">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="11901-715">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="11901-716">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="11901-716">Return Value - showContextMenu</span></span>

<span data-ttu-id="11901-717">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-717">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="11901-718">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="11901-718">Method skip</span></span>

<span data-ttu-id="11901-719">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-719">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="11901-720">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="11901-720">Parameters - skip</span></span>

<span data-ttu-id="11901-721">値</span><span class="sxs-lookup"><span data-stu-id="11901-721">value</span></span>  
<span data-ttu-id="11901-722">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-722">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="11901-723">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="11901-723">Return Value - skip</span></span>

<span data-ttu-id="11901-724">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="11901-724">true if the control is skipped when the user presses the TAB key to move to the control; otherwise false.</span></span>

## <a name="method-step"></a><span data-ttu-id="11901-725">メソッド step</span><span class="sxs-lookup"><span data-stu-id="11901-725">Method step</span></span>

```xpp
public int step([int value])
```

### <a name="parameters---step"></a><span data-ttu-id="11901-726">パラメーター - step</span><span class="sxs-lookup"><span data-stu-id="11901-726">Parameters - step</span></span>

<span data-ttu-id="11901-727">値</span><span class="sxs-lookup"><span data-stu-id="11901-727">value</span></span>  

### <a name="return-value---step"></a><span data-ttu-id="11901-728">戻り値 - step</span><span class="sxs-lookup"><span data-stu-id="11901-728">Return Value - step</span></span>

## <a name="method-style"></a><span data-ttu-id="11901-729">メソッド style</span><span class="sxs-lookup"><span data-stu-id="11901-729">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="11901-730">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="11901-730">Parameters - style</span></span>

<span data-ttu-id="11901-731">値</span><span class="sxs-lookup"><span data-stu-id="11901-731">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="11901-732">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="11901-732">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="11901-733">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="11901-733">Method toolTip</span></span>

<span data-ttu-id="11901-734">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="11901-734">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="11901-735">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="11901-735">Return Value - toolTip</span></span>

<span data-ttu-id="11901-736">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="11901-736">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="11901-737">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="11901-737">Remarks - toolTip</span></span>

<span data-ttu-id="11901-738">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="11901-738">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="11901-739">メソッド top</span><span class="sxs-lookup"><span data-stu-id="11901-739">Method top</span></span>

<span data-ttu-id="11901-740">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-740">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="11901-741">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="11901-741">Parameters - top</span></span>

<span data-ttu-id="11901-742">値</span><span class="sxs-lookup"><span data-stu-id="11901-742">value</span></span>  
<span data-ttu-id="11901-743">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-743">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="11901-744">モード</span><span class="sxs-lookup"><span data-stu-id="11901-744">mode</span></span>  
<span data-ttu-id="11901-745">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-745">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="11901-746">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="11901-746">Return Value - top</span></span>

<span data-ttu-id="11901-747">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="11901-747">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="11901-748">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="11901-748">Method topMode</span></span>

<span data-ttu-id="11901-749">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-749">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="11901-750">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="11901-750">Parameters - topMode</span></span>

<span data-ttu-id="11901-751">値</span><span class="sxs-lookup"><span data-stu-id="11901-751">value</span></span>  
<span data-ttu-id="11901-752">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-752">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="11901-753">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="11901-753">Return Value - topMode</span></span>

<span data-ttu-id="11901-754">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="11901-754">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="11901-755">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="11901-755">Method topValue</span></span>

<span data-ttu-id="11901-756">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-756">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="11901-757">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="11901-757">Parameters - topValue</span></span>

<span data-ttu-id="11901-758">値</span><span class="sxs-lookup"><span data-stu-id="11901-758">value</span></span>  
<span data-ttu-id="11901-759">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-759">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="11901-760">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="11901-760">Return Value - topValue</span></span>

<span data-ttu-id="11901-761">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="11901-761">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="11901-762">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="11901-762">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="11901-763">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="11901-763">Parameters - type</span></span>

<span data-ttu-id="11901-764">値</span><span class="sxs-lookup"><span data-stu-id="11901-764">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="11901-765">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="11901-765">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="11901-766">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="11901-766">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="11901-767">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="11901-767">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="11901-768">データ</span><span class="sxs-lookup"><span data-stu-id="11901-768">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="11901-769">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="11901-769">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="11901-770">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="11901-770">Method userData</span></span>

<span data-ttu-id="11901-771">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-771">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="11901-772">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="11901-772">Parameters - userData</span></span>

<span data-ttu-id="11901-773">値</span><span class="sxs-lookup"><span data-stu-id="11901-773">value</span></span>  
<span data-ttu-id="11901-774">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-774">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="11901-775">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="11901-775">Return Value - userData</span></span>

<span data-ttu-id="11901-776">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="11901-776">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="11901-777">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="11901-777">Method userDataItem</span></span>

<span data-ttu-id="11901-778">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-778">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="11901-779">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="11901-779">Parameters - userDataItem</span></span>

<span data-ttu-id="11901-780">値</span><span class="sxs-lookup"><span data-stu-id="11901-780">value</span></span>  
<span data-ttu-id="11901-781">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-781">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="11901-782">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="11901-782">Return Value - userDataItem</span></span>

<span data-ttu-id="11901-783">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="11901-783">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="11901-784">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="11901-784">Method userDataItems</span></span>

<span data-ttu-id="11901-785">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-785">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="11901-786">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="11901-786">Parameters - userDataItems</span></span>

<span data-ttu-id="11901-787">値</span><span class="sxs-lookup"><span data-stu-id="11901-787">value</span></span>  
<span data-ttu-id="11901-788">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-788">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="11901-789">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="11901-789">Return Value - userDataItems</span></span>

<span data-ttu-id="11901-790">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="11901-790">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="11901-791">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="11901-791">Method userDisable</span></span>

<span data-ttu-id="11901-792">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-792">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="11901-793">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="11901-793">Parameters - userDisable</span></span>

<span data-ttu-id="11901-794">値</span><span class="sxs-lookup"><span data-stu-id="11901-794">value</span></span>  
<span data-ttu-id="11901-795">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-795">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="11901-796">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="11901-796">Return Value - userDisable</span></span>

<span data-ttu-id="11901-797">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="11901-797">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="11901-798">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="11901-798">Method userHeight</span></span>

<span data-ttu-id="11901-799">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-799">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="11901-800">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="11901-800">Parameters - userHeight</span></span>

<span data-ttu-id="11901-801">値</span><span class="sxs-lookup"><span data-stu-id="11901-801">value</span></span>  
<span data-ttu-id="11901-802">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-802">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="11901-803">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="11901-803">Return Value - userHeight</span></span>

<span data-ttu-id="11901-804">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="11901-804">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="11901-805">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="11901-805">Method userHide</span></span>

<span data-ttu-id="11901-806">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-806">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="11901-807">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="11901-807">Parameters - userHide</span></span>

<span data-ttu-id="11901-808">値</span><span class="sxs-lookup"><span data-stu-id="11901-808">value</span></span>  
<span data-ttu-id="11901-809">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-809">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="11901-810">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="11901-810">Return Value - userHide</span></span>

<span data-ttu-id="11901-811">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="11901-811">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="11901-812">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="11901-812">Remarks - userHide</span></span>

<span data-ttu-id="11901-813">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="11901-813">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="11901-814">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="11901-814">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="11901-815">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="11901-815">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="11901-816">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="11901-816">Method userOrgContainer</span></span>

<span data-ttu-id="11901-817">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-817">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="11901-818">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="11901-818">Parameters - userOrgContainer</span></span>

<span data-ttu-id="11901-819">値</span><span class="sxs-lookup"><span data-stu-id="11901-819">value</span></span>  
<span data-ttu-id="11901-820">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-820">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="11901-821">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="11901-821">Return Value - userOrgContainer</span></span>

<span data-ttu-id="11901-822">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="11901-822">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="11901-823">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="11901-823">Method userOrgSibling</span></span>

<span data-ttu-id="11901-824">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-824">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="11901-825">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="11901-825">Parameters - userOrgSibling</span></span>

<span data-ttu-id="11901-826">値</span><span class="sxs-lookup"><span data-stu-id="11901-826">value</span></span>  
<span data-ttu-id="11901-827">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-827">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="11901-828">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="11901-828">Return Value - userOrgSibling</span></span>

<span data-ttu-id="11901-829">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="11901-829">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="11901-830">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="11901-830">Method userPromptText</span></span>

<span data-ttu-id="11901-831">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-831">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="11901-832">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="11901-832">Parameters - userPromptText</span></span>

<span data-ttu-id="11901-833">値</span><span class="sxs-lookup"><span data-stu-id="11901-833">value</span></span>  
<span data-ttu-id="11901-834">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-834">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="11901-835">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="11901-835">Return Value - userPromptText</span></span>

<span data-ttu-id="11901-836">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="11901-836">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="11901-837">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="11901-837">Method userSecurityLevel</span></span>

<span data-ttu-id="11901-838">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-838">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="11901-839">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="11901-839">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="11901-840">値</span><span class="sxs-lookup"><span data-stu-id="11901-840">value</span></span>  
<span data-ttu-id="11901-841">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-841">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="11901-842">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="11901-842">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="11901-843">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="11901-843">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="11901-844">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="11901-844">Method userSkip</span></span>

<span data-ttu-id="11901-845">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-845">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="11901-846">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="11901-846">Parameters - userSkip</span></span>

<span data-ttu-id="11901-847">値</span><span class="sxs-lookup"><span data-stu-id="11901-847">value</span></span>  
<span data-ttu-id="11901-848">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-848">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="11901-849">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="11901-849">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="11901-850">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="11901-850">Return Value - userSkip</span></span>

<span data-ttu-id="11901-851">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="11901-851">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="11901-852">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="11901-852">Method userWidth</span></span>

<span data-ttu-id="11901-853">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-853">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="11901-854">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="11901-854">Parameters - userWidth</span></span>

<span data-ttu-id="11901-855">値</span><span class="sxs-lookup"><span data-stu-id="11901-855">value</span></span>  
<span data-ttu-id="11901-856">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-856">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="11901-857">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="11901-857">Return Value - userWidth</span></span>

<span data-ttu-id="11901-858">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="11901-858">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="11901-859">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="11901-859">Remarks - userWidth</span></span>

<span data-ttu-id="11901-860">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="11901-860">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="11901-861">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="11901-861">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="11901-862">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="11901-862">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="11901-863">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="11901-863">Method verticalSpacing</span></span>

<span data-ttu-id="11901-864">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-864">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="11901-865">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="11901-865">Parameters - verticalSpacing</span></span>

<span data-ttu-id="11901-866">値</span><span class="sxs-lookup"><span data-stu-id="11901-866">value</span></span>  
<span data-ttu-id="11901-867">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-867">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="11901-868">モード</span><span class="sxs-lookup"><span data-stu-id="11901-868">mode</span></span>  
<span data-ttu-id="11901-869">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-869">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="11901-870">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="11901-870">Return Value - verticalSpacing</span></span>

<span data-ttu-id="11901-871">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="11901-871">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="11901-872">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="11901-872">Method verticalSpacingMode</span></span>

<span data-ttu-id="11901-873">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-873">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="11901-874">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="11901-874">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="11901-875">モード</span><span class="sxs-lookup"><span data-stu-id="11901-875">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="11901-876">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="11901-876">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="11901-877">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="11901-877">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="11901-878">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="11901-878">Method verticalSpacingValue</span></span>

<span data-ttu-id="11901-879">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-879">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="11901-880">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="11901-880">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="11901-881">値</span><span class="sxs-lookup"><span data-stu-id="11901-881">value</span></span>  
<span data-ttu-id="11901-882">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-882">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="11901-883">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="11901-883">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="11901-884">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="11901-884">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="11901-885">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="11901-885">Method visible</span></span>

<span data-ttu-id="11901-886">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="11901-886">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="11901-887">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="11901-887">Parameters - visible</span></span>

<span data-ttu-id="11901-888">値</span><span class="sxs-lookup"><span data-stu-id="11901-888">value</span></span>  
<span data-ttu-id="11901-889">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-889">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="11901-890">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="11901-890">Return Value - visible</span></span>

<span data-ttu-id="11901-891">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="11901-891">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="11901-892">メソッド width</span><span class="sxs-lookup"><span data-stu-id="11901-892">Method width</span></span>

<span data-ttu-id="11901-893">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-893">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="11901-894">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="11901-894">Parameters - width</span></span>

<span data-ttu-id="11901-895">値</span><span class="sxs-lookup"><span data-stu-id="11901-895">value</span></span>  
<span data-ttu-id="11901-896">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-896">An integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="11901-897">モード</span><span class="sxs-lookup"><span data-stu-id="11901-897">mode</span></span>  
<span data-ttu-id="11901-898">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-898">An integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="11901-899">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="11901-899">Return Value - width</span></span>

<span data-ttu-id="11901-900">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="11901-900">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="11901-901">備考 - width</span><span class="sxs-lookup"><span data-stu-id="11901-901">Remarks - width</span></span>

<span data-ttu-id="11901-902">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="11901-902">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="11901-903">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="11901-903">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="11901-904">モード</span><span class="sxs-lookup"><span data-stu-id="11901-904">Mode</span></span>           | <span data-ttu-id="11901-905">幅計算</span><span class="sxs-lookup"><span data-stu-id="11901-905">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11901-906">-1 正確</span><span class="sxs-lookup"><span data-stu-id="11901-906">-1 Exact</span></span>       | <span data-ttu-id="11901-907">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="11901-907">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="11901-908">0 自動</span><span class="sxs-lookup"><span data-stu-id="11901-908">0 Auto</span></span>         | <span data-ttu-id="11901-909">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="11901-909">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="11901-910">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="11901-910">1 Column width</span></span> | <span data-ttu-id="11901-911">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="11901-911">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="11901-912">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="11901-912">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="11901-913">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="11901-913">Method widthMode</span></span>

<span data-ttu-id="11901-914">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-914">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="11901-915">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="11901-915">Parameters - widthMode</span></span>

<span data-ttu-id="11901-916">値</span><span class="sxs-lookup"><span data-stu-id="11901-916">value</span></span>  
<span data-ttu-id="11901-917">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-917">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="11901-918">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="11901-918">Return Value - widthMode</span></span>

<span data-ttu-id="11901-919">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-919">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="11901-920">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="11901-920">Remarks - widthMode</span></span>

<span data-ttu-id="11901-921">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="11901-921">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="11901-922">モード</span><span class="sxs-lookup"><span data-stu-id="11901-922">Mode</span></span>         | <span data-ttu-id="11901-923">幅計算</span><span class="sxs-lookup"><span data-stu-id="11901-923">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11901-924">正確</span><span class="sxs-lookup"><span data-stu-id="11901-924">Exact</span></span>        | <span data-ttu-id="11901-925">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="11901-925">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="11901-926">自動</span><span class="sxs-lookup"><span data-stu-id="11901-926">Auto</span></span>         | <span data-ttu-id="11901-927">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="11901-927">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="11901-928">列の幅</span><span class="sxs-lookup"><span data-stu-id="11901-928">Column width</span></span> | <span data-ttu-id="11901-929">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="11901-929">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="11901-930">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="11901-930">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="11901-931">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="11901-931">Method widthValue</span></span>

<span data-ttu-id="11901-932">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-932">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="11901-933">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="11901-933">Parameters - widthValue</span></span>

<span data-ttu-id="11901-934">値</span><span class="sxs-lookup"><span data-stu-id="11901-934">value</span></span>  
<span data-ttu-id="11901-935">幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="11901-935">An integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="11901-936">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="11901-936">Return Value - widthValue</span></span>

<span data-ttu-id="11901-937">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="11901-937">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="11901-938">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="11901-938">Remarks - widthValue</span></span>

<span data-ttu-id="11901-939">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="11901-939">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-context"></a><span data-ttu-id="11901-940">メソッド context</span><span class="sxs-lookup"><span data-stu-id="11901-940">Method context</span></span>

<span data-ttu-id="11901-941">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="11901-941">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enddrag"></a><span data-ttu-id="11901-942">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="11901-942">Method endDrag</span></span>

<span data-ttu-id="11901-943">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-943">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="11901-944">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="11901-944">Remarks - endDrag</span></span>

<span data-ttu-id="11901-945">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="11901-945">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="11901-946">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="11901-946">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-inputsearch"></a><span data-ttu-id="11901-947">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="11901-947">Method inputSearch</span></span>

<span data-ttu-id="11901-948">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="11901-948">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="11901-949">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="11901-949">Parameters - inputSearch</span></span>

<span data-ttu-id="11901-950">searchStr</span><span class="sxs-lookup"><span data-stu-id="11901-950">searchStr</span></span>  
<span data-ttu-id="11901-951">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11901-951">The string value to use to filter data; optional.</span></span>

## <a name="method-paste"></a><span data-ttu-id="11901-952">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="11901-952">Method paste</span></span>

<span data-ttu-id="11901-953">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="11901-953">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-enter"></a><span data-ttu-id="11901-954">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="11901-954">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-mouseenter"></a><span data-ttu-id="11901-955">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="11901-955">Method mouseEnter</span></span>

<span data-ttu-id="11901-956">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11901-956">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="11901-957">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="11901-957">Parameters - mouseEnter</span></span>

<span data-ttu-id="11901-958">x</span><span class="sxs-lookup"><span data-stu-id="11901-958">x</span></span>  
<span data-ttu-id="11901-959">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-959">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-960">y</span><span class="sxs-lookup"><span data-stu-id="11901-960">y</span></span>  
<span data-ttu-id="11901-961">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-961">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-962">ボタン</span><span class="sxs-lookup"><span data-stu-id="11901-962">button</span></span>  
<span data-ttu-id="11901-963">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-963">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-964">Ctrl</span><span class="sxs-lookup"><span data-stu-id="11901-964">Ctrl</span></span>  
<span data-ttu-id="11901-965">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-965">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="11901-966">シフト</span><span class="sxs-lookup"><span data-stu-id="11901-966">Shift</span></span>  
<span data-ttu-id="11901-967">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="11901-967">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="11901-968">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="11901-968">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="11901-969">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="11901-969">Parameters - OnLostFocus</span></span>

<span data-ttu-id="11901-970">sender</span><span class="sxs-lookup"><span data-stu-id="11901-970">sender</span></span>  

<!-- -->

<span data-ttu-id="11901-971">e</span><span class="sxs-lookup"><span data-stu-id="11901-971">e</span></span>  

## <a name="method-drop"></a><span data-ttu-id="11901-972">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="11901-972">Method drop</span></span>

<span data-ttu-id="11901-973">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-973">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="11901-974">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="11901-974">Parameters - drop</span></span>

<span data-ttu-id="11901-975">dragSource</span><span class="sxs-lookup"><span data-stu-id="11901-975">dragSource</span></span>  
<span data-ttu-id="11901-976">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-976">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-977">dragMode</span><span class="sxs-lookup"><span data-stu-id="11901-977">dragMode</span></span>  
<span data-ttu-id="11901-978">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-978">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-979">x</span><span class="sxs-lookup"><span data-stu-id="11901-979">x</span></span>  
<span data-ttu-id="11901-980">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-980">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-981">y</span><span class="sxs-lookup"><span data-stu-id="11901-981">y</span></span>  
<span data-ttu-id="11901-982">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-982">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onleaving"></a><span data-ttu-id="11901-983">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="11901-983">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="11901-984">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="11901-984">Parameters - OnLeaving</span></span>

<span data-ttu-id="11901-985">sender</span><span class="sxs-lookup"><span data-stu-id="11901-985">sender</span></span>  

<!-- -->

<span data-ttu-id="11901-986">e</span><span class="sxs-lookup"><span data-stu-id="11901-986">e</span></span>  

## <a name="method-ongotfocus"></a><span data-ttu-id="11901-987">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="11901-987">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="11901-988">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="11901-988">Parameters - OnGotFocus</span></span>

<span data-ttu-id="11901-989">sender</span><span class="sxs-lookup"><span data-stu-id="11901-989">sender</span></span>  

<!-- -->

<span data-ttu-id="11901-990">e</span><span class="sxs-lookup"><span data-stu-id="11901-990">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="11901-991">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="11901-991">Method mouseLeave</span></span>

<span data-ttu-id="11901-992">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="11901-992">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-dropex"></a><span data-ttu-id="11901-993">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="11901-993">Method dropEx</span></span>

<span data-ttu-id="11901-994">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-994">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="11901-995">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="11901-995">Parameters - dropEx</span></span>

<span data-ttu-id="11901-996">dragSource</span><span class="sxs-lookup"><span data-stu-id="11901-996">dragSource</span></span>  
<span data-ttu-id="11901-997">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-997">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-998">dragMode</span><span class="sxs-lookup"><span data-stu-id="11901-998">dragMode</span></span>  
<span data-ttu-id="11901-999">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-999">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-1000">x</span><span class="sxs-lookup"><span data-stu-id="11901-1000">x</span></span>  
<span data-ttu-id="11901-1001">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-1001">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="11901-1002">y</span><span class="sxs-lookup"><span data-stu-id="11901-1002">y</span></span>  
<span data-ttu-id="11901-1003">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="11901-1003">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="11901-1004">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="11901-1004">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="11901-1005">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="11901-1005">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="11901-1006">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="11901-1006">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="11901-1007">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="11901-1007">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="11901-1008">overrideObject</span><span class="sxs-lookup"><span data-stu-id="11901-1008">overrideObject</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="11901-1009">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="11901-1009">Method dragLeave</span></span>

<span data-ttu-id="11901-1010">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="11901-1010">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="11901-1011">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="11901-1011">Method displayControl</span></span>

<span data-ttu-id="11901-1012">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="11901-1012">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-cut"></a><span data-ttu-id="11901-1013">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="11901-1013">Method cut</span></span>

<span data-ttu-id="11901-1014">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="11901-1014">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-stepit"></a><span data-ttu-id="11901-1015">メソッド stepIt</span><span class="sxs-lookup"><span data-stu-id="11901-1015">Method stepIt</span></span>

```xpp
public void stepIt()
```

## <a name="method-deltapos"></a><span data-ttu-id="11901-1016">メソッド deltaPos</span><span class="sxs-lookup"><span data-stu-id="11901-1016">Method deltaPos</span></span>

```xpp
public void deltaPos(int inc)
```

### <a name="parameters---deltapos"></a><span data-ttu-id="11901-1017">パラメーター - deltaPos</span><span class="sxs-lookup"><span data-stu-id="11901-1017">Parameters - deltaPos</span></span>

<span data-ttu-id="11901-1018">inc</span><span class="sxs-lookup"><span data-stu-id="11901-1018">inc</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="11901-1019">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="11901-1019">Method lostFocus</span></span>

<span data-ttu-id="11901-1020">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="11901-1020">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-copy"></a><span data-ttu-id="11901-1021">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="11901-1021">Method copy</span></span>

<span data-ttu-id="11901-1022">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="11901-1022">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="11901-1023">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="11901-1023">Method prefColumnSize</span></span>

<span data-ttu-id="11901-1024">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="11901-1024">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="11901-1025">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="11901-1025">Parameters - prefColumnSize</span></span>

<span data-ttu-id="11901-1026">width</span><span class="sxs-lookup"><span data-stu-id="11901-1026">width</span></span>  
<span data-ttu-id="11901-1027">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="11901-1027">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="11901-1028">height</span><span class="sxs-lookup"><span data-stu-id="11901-1028">height</span></span>  
<span data-ttu-id="11901-1029">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="11901-1029">The preferred height of the control.</span></span>

## <a name="method-onenter"></a><span data-ttu-id="11901-1030">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="11901-1030">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="11901-1031">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="11901-1031">Parameters - OnEnter</span></span>

<span data-ttu-id="11901-1032">sender</span><span class="sxs-lookup"><span data-stu-id="11901-1032">sender</span></span>  

<!-- -->

<span data-ttu-id="11901-1033">e</span><span class="sxs-lookup"><span data-stu-id="11901-1033">e</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="11901-1034">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="11901-1034">Method setFocus</span></span>

<span data-ttu-id="11901-1035">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="11901-1035">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="11901-1036">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="11901-1036">Method resetUserSetting</span></span>

<span data-ttu-id="11901-1037">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="11901-1037">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-gotfocus"></a><span data-ttu-id="11901-1038">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="11901-1038">Method gotFocus</span></span>

<span data-ttu-id="11901-1039">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="11901-1039">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

