---
title: FormAnimateControl クラス
description: このトピックでは、FormAnimateControl クラスについて説明します。
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
ms.openlocfilehash: 17e29595bb98eebb5b98391b2afe35ebaf790d04
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502662"
---
# <a name="class-formanimatecontrol"></a><span data-ttu-id="a34b8-103">クラス FormAnimateControl</span><span class="sxs-lookup"><span data-stu-id="a34b8-103">Class FormAnimateControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormAnimateControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="a34b8-104">備考</span><span class="sxs-lookup"><span data-stu-id="a34b8-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="a34b8-105">例</span><span class="sxs-lookup"><span data-stu-id="a34b8-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a34b8-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="a34b8-106">Methods</span></span>

| <span data-ttu-id="a34b8-107">方法</span><span class="sxs-lookup"><span data-stu-id="a34b8-107">Method</span></span>                                                                                                      | <span data-ttu-id="a34b8-108">説明</span><span class="sxs-lookup"><span data-stu-id="a34b8-108">Description</span></span>                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34b8-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="a34b8-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-110">Determines whether to align the control.</span></span>                                                                                                             |
| <span data-ttu-id="a34b8-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="a34b8-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-112">Determines whether the user can change the contents of the control.</span></span>                                                                                  |
| <span data-ttu-id="a34b8-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="a34b8-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="a34b8-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                  |
| <span data-ttu-id="a34b8-115">public str animateFile(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-115">public str animateFile(\[str value\])</span></span>                                                                       |                                                                                                                                                      |
| <span data-ttu-id="a34b8-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="a34b8-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                   |
| <span data-ttu-id="a34b8-118">public boolean autoPlay(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-118">public boolean autoPlay(\[boolean value\])</span></span>                                                                  |                                                                                                                                                      |
| <span data-ttu-id="a34b8-119">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="a34b8-119">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="a34b8-120">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-120">Is called when the user starts to drag a form control.</span></span>                                                                                               |
| <span data-ttu-id="a34b8-121">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-121">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="a34b8-122">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-122">Gets or sets the style of the borderline of the control.</span></span>                                                                                             |
| <span data-ttu-id="a34b8-123">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="a34b8-123">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="a34b8-124">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-124">Retrieves the size of the control.</span></span>                                                                                                                   |
| <span data-ttu-id="a34b8-125">public boolean center(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-125">public boolean center(\[boolean value\])</span></span>                                                                    |                                                                                                                                                      |
| <span data-ttu-id="a34b8-126">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-126">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="a34b8-127">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-127">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                  |
| <span data-ttu-id="a34b8-128">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="a34b8-128">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="a34b8-129">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-129">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                     |
| <span data-ttu-id="a34b8-130">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-130">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="a34b8-131">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-131">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                       |
| <span data-ttu-id="a34b8-132">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-132">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="a34b8-133">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-133">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                        |
| <span data-ttu-id="a34b8-134">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-134">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="a34b8-135">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-135">Gets or sets the value that indicates whether the control is displayed in the client, or in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="a34b8-136">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-136">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="a34b8-137">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-137">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                    |
| <span data-ttu-id="a34b8-138">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="a34b8-138">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="a34b8-139">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-139">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                       |
| <span data-ttu-id="a34b8-140">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="a34b8-140">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="a34b8-141">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-141">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                     |
| <span data-ttu-id="a34b8-142">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="a34b8-142">public str dragText()</span></span>                                                                                       | <span data-ttu-id="a34b8-143">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-143">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                               |
| <span data-ttu-id="a34b8-144">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-144">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="a34b8-145">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-145">Determines whether to enable or disable the object.</span></span>                                                                                                  |
| <span data-ttu-id="a34b8-146">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-146">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="a34b8-147">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-147">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                             |
| <span data-ttu-id="a34b8-148">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="a34b8-148">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="a34b8-149">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-149">Indicates whether the control has custom user settings.</span></span>                                                                                              |
| <span data-ttu-id="a34b8-150">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-150">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="a34b8-151">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-151">Gets or sets the height of the control.</span></span>                                                                                                              |
| <span data-ttu-id="a34b8-152">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-152">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="a34b8-153">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-153">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                       |
| <span data-ttu-id="a34b8-154">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-154">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="a34b8-155">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-155">Gets or sets the height of the control.</span></span>                                                                                                              |
| <span data-ttu-id="a34b8-156">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="a34b8-156">public str helpField()</span></span>                                                                                      | <span data-ttu-id="a34b8-157">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-157">Retrieves the Help text for the control.</span></span>                                                                                                             |
| <span data-ttu-id="a34b8-158">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-158">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="a34b8-159">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-159">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                             |
| <span data-ttu-id="a34b8-160">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-160">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="a34b8-161">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-161">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                      |
| <span data-ttu-id="a34b8-162">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="a34b8-162">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="a34b8-163">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-163">Retrieves the Windows handle for the control.</span></span>                                                                                                        |
| <span data-ttu-id="a34b8-164">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="a34b8-164">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                      |
| <span data-ttu-id="a34b8-165">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="a34b8-165">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="a34b8-166">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-166">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                   |
| <span data-ttu-id="a34b8-167">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="a34b8-167">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="a34b8-168">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-168">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                  |
| <span data-ttu-id="a34b8-169">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="a34b8-169">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="a34b8-170">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-170">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                  |
| <span data-ttu-id="a34b8-171">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="a34b8-171">public boolean leave()</span></span>                                                                                      |                                                                                                                                                      |
| <span data-ttu-id="a34b8-172">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-172">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="a34b8-173">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-173">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                     |
| <span data-ttu-id="a34b8-174">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-174">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="a34b8-175">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-175">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="a34b8-176">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-176">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="a34b8-177">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-177">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                     |
| <span data-ttu-id="a34b8-178">public int loops(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-178">public int loops(\[int value\])</span></span>                                                                             |                                                                                                                                                      |
| <span data-ttu-id="a34b8-179">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-179">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="a34b8-180">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="a34b8-180">Marks or unmarks the control as a user-added control.</span></span>                                                                                                |
| <span data-ttu-id="a34b8-181">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="a34b8-181">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="a34b8-182">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-182">Is called when the control is double-clicked by the user.</span></span>                                                                                            |
| <span data-ttu-id="a34b8-183">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="a34b8-183">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="a34b8-184">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-184">Is called when the user clicks the mouse button over the control.</span></span>                                                                                    |
| <span data-ttu-id="a34b8-185">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="a34b8-185">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="a34b8-186">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-186">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                    |
| <span data-ttu-id="a34b8-187">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="a34b8-187">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="a34b8-188">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-188">Is called when the user releases the mouse button over the control area.</span></span>                                                                             |
| <span data-ttu-id="a34b8-189">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-189">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="a34b8-190">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-190">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>              |
| <span data-ttu-id="a34b8-191">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-191">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                      |
| <span data-ttu-id="a34b8-192">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="a34b8-192">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                      |
| <span data-ttu-id="a34b8-193">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="a34b8-193">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="a34b8-194">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-194">Retrieves the parent control for the control.</span></span>                                                                                                        |
| <span data-ttu-id="a34b8-195">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-195">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="a34b8-196">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-196">Sets or returns the ID of the security key for the control.</span></span>                                                                                          |
| <span data-ttu-id="a34b8-197">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="a34b8-197">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="a34b8-198">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-198">Shows the shortcut menu for the control.</span></span>                                                                                                             |
| <span data-ttu-id="a34b8-199">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-199">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="a34b8-200">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-200">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                      |
| <span data-ttu-id="a34b8-201">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="a34b8-201">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="a34b8-202">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-202">Retrieves the tooltip text for the control.</span></span>                                                                                                          |
| <span data-ttu-id="a34b8-203">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-203">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="a34b8-204">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-204">Gets or sets the vertical position of the control in the form.</span></span>                                                                                       |
| <span data-ttu-id="a34b8-205">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-205">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="a34b8-206">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-206">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                          |
| <span data-ttu-id="a34b8-207">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-207">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="a34b8-208">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-208">Gets or sets the vertical position of the control in the form.</span></span>                                                                                       |
| <span data-ttu-id="a34b8-209">public boolean transparent(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-209">public boolean transparent(\[boolean value\])</span></span>                                                               |                                                                                                                                                      |
| <span data-ttu-id="a34b8-210">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-210">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                      |
| <span data-ttu-id="a34b8-211">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="a34b8-211">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                      |
| <span data-ttu-id="a34b8-212">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-212">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="a34b8-213">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-213">Gets or sets the user data for the control.</span></span>                                                                                                          |
| <span data-ttu-id="a34b8-214">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-214">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="a34b8-215">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-215">Gets or sets the user data item for the control.</span></span>                                                                                                     |
| <span data-ttu-id="a34b8-216">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-216">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="a34b8-217">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-217">Gets or sets the number of user data items for the control.</span></span>                                                                                          |
| <span data-ttu-id="a34b8-218">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-218">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="a34b8-219">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-219">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                  |
| <span data-ttu-id="a34b8-220">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-220">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="a34b8-221">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-221">Gets or sets the custom user height for the control.</span></span>                                                                                                 |
| <span data-ttu-id="a34b8-222">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-222">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="a34b8-223">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-223">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                   |
| <span data-ttu-id="a34b8-224">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-224">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="a34b8-225">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-225">Gets or sets the organization container for the control.</span></span>                                                                                             |
| <span data-ttu-id="a34b8-226">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-226">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="a34b8-227">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-227">Gets or sets the organization sibling for the control.</span></span>                                                                                               |
| <span data-ttu-id="a34b8-228">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-228">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="a34b8-229">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-229">Gets or sets the user label text for the control.</span></span>                                                                                                    |
| <span data-ttu-id="a34b8-230">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-230">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="a34b8-231">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-231">Gets or sets the user security level for the control.</span></span>                                                                                                |
| <span data-ttu-id="a34b8-232">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-232">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="a34b8-233">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-233">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span> |
| <span data-ttu-id="a34b8-234">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-234">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="a34b8-235">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-235">Sets or returns the width of the control in pixels.</span></span>                                                                                                  |
| <span data-ttu-id="a34b8-236">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-236">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="a34b8-237">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-237">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="a34b8-238">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-238">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="a34b8-239">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-239">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                          |
| <span data-ttu-id="a34b8-240">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-240">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="a34b8-241">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-241">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="a34b8-242">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-242">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="a34b8-243">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-243">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                               |
| <span data-ttu-id="a34b8-244">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-244">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="a34b8-245">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-245">Gets or sets the width of the control.</span></span>                                                                                                               |
| <span data-ttu-id="a34b8-246">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-246">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="a34b8-247">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-247">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                       |
| <span data-ttu-id="a34b8-248">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-248">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="a34b8-249">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-249">Gets or sets the width of the control.</span></span>                                                                                                               |
| <span data-ttu-id="a34b8-250">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-250">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                      |
| <span data-ttu-id="a34b8-251">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="a34b8-251">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="a34b8-252">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-252">Performs data filtering for the control, based on the specified string.</span></span>                                                                              |
| <span data-ttu-id="a34b8-253">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="a34b8-253">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="a34b8-254">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-254">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                 |
| <span data-ttu-id="a34b8-255">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="a34b8-255">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="a34b8-256">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-256">Indicates that the control has lost focus.</span></span>                                                                                                           |
| <span data-ttu-id="a34b8-257">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="a34b8-257">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="a34b8-258">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-258">Sets the focus on the control.</span></span>                                                                                                                       |
| <span data-ttu-id="a34b8-259">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="a34b8-259">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="a34b8-260">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-260">Specifies the preferred column width and height for the form control.</span></span>                                                                                |
| <span data-ttu-id="a34b8-261">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="a34b8-261">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="a34b8-262">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-262">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                               |
| <span data-ttu-id="a34b8-263">public void paste()</span><span class="sxs-lookup"><span data-stu-id="a34b8-263">public void paste()</span></span>                                                                                         | <span data-ttu-id="a34b8-264">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-264">Pastes the contents of the clipboard into the control.</span></span>                                                                                               |
| <span data-ttu-id="a34b8-265">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="a34b8-265">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="a34b8-266">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-266">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                   |
| <span data-ttu-id="a34b8-267">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-267">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                      |
| <span data-ttu-id="a34b8-268">public void enter()</span><span class="sxs-lookup"><span data-stu-id="a34b8-268">public void enter()</span></span>                                                                                         |                                                                                                                                                      |
| <span data-ttu-id="a34b8-269">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="a34b8-269">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="a34b8-270">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-270">Indicates that the mouse pointer has left the control.</span></span>                                                                                               |
| <span data-ttu-id="a34b8-271">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="a34b8-271">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="a34b8-272">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-272">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                     |
| <span data-ttu-id="a34b8-273">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-273">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                      |
| <span data-ttu-id="a34b8-274">public void copy()</span><span class="sxs-lookup"><span data-stu-id="a34b8-274">public void copy()</span></span>                                                                                          | <span data-ttu-id="a34b8-275">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a34b8-275">Copies the contents of the control to the clipboard.</span></span>                                                                                                 |
| <span data-ttu-id="a34b8-276">public void context()</span><span class="sxs-lookup"><span data-stu-id="a34b8-276">public void context()</span></span>                                                                                       | <span data-ttu-id="a34b8-277">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-277">Shows the shortcut menu for the control.</span></span>                                                                                                             |
| <span data-ttu-id="a34b8-278">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="a34b8-278">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="a34b8-279">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-279">Is called when the user has finished dragging a form control.</span></span>                                                                                        |
| <span data-ttu-id="a34b8-280">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="a34b8-280">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="a34b8-281">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="a34b8-281">Resets the user settings for the control.</span></span>                                                                                                            |
| <span data-ttu-id="a34b8-282">public void play(\[int firstFrame\], \[int lastFrame\], \[int loops\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-282">public void play(\[int firstFrame\], \[int lastFrame\], \[int loops\])</span></span>                                      |                                                                                                                                                      |
| <span data-ttu-id="a34b8-283">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-283">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                      |
| <span data-ttu-id="a34b8-284">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="a34b8-284">public void displayControl()</span></span>                                                                                | <span data-ttu-id="a34b8-285">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-285">Displays the control.</span></span>                                                                                                                                |
| <span data-ttu-id="a34b8-286">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="a34b8-286">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="a34b8-287">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-287">Indicates that the control has received focus.</span></span>                                                                                                       |
| <span data-ttu-id="a34b8-288">public void cut()</span><span class="sxs-lookup"><span data-stu-id="a34b8-288">public void cut()</span></span>                                                                                           | <span data-ttu-id="a34b8-289">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="a34b8-289">Cuts the contents of the control.</span></span>                                                                                                                    |
| <span data-ttu-id="a34b8-290">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="a34b8-290">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                      |
| <span data-ttu-id="a34b8-291">public void stop()</span><span class="sxs-lookup"><span data-stu-id="a34b8-291">public void stop()</span></span>                                                                                          |                                                                                                                                                      |

## <a name="method-aligncontrol"></a><span data-ttu-id="a34b8-292">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="a34b8-292">Method alignControl</span></span>

<span data-ttu-id="a34b8-293">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-293">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="a34b8-294">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="a34b8-294">Parameters - alignControl</span></span>

<span data-ttu-id="a34b8-295">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-295">value</span></span>  
<span data-ttu-id="a34b8-296">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-296">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="a34b8-297">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="a34b8-297">Return Value - alignControl</span></span>

<span data-ttu-id="a34b8-298">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-298">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="a34b8-299">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="a34b8-299">Remarks - alignControl</span></span>

<span data-ttu-id="a34b8-300">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-300">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="a34b8-301">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="a34b8-301">Method allowEdit</span></span>

<span data-ttu-id="a34b8-302">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-302">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="a34b8-303">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a34b8-303">Parameters - allowEdit</span></span>

<span data-ttu-id="a34b8-304">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-304">value</span></span>  
<span data-ttu-id="a34b8-305">allowEdit プロパティに割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-305">The value to be assigned to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="a34b8-306">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a34b8-306">Return Value - allowEdit</span></span>

<span data-ttu-id="a34b8-307">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-307">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="a34b8-308">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a34b8-308">Remarks - allowEdit</span></span>

<span data-ttu-id="a34b8-309">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-309">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="a34b8-310">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="a34b8-310">Method allowSysSetup</span></span>

<span data-ttu-id="a34b8-311">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-311">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="a34b8-312">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="a34b8-312">Return Value - allowSysSetup</span></span>

<span data-ttu-id="a34b8-313">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-313">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-animatefile"></a><span data-ttu-id="a34b8-314">メソッド animateFile</span><span class="sxs-lookup"><span data-stu-id="a34b8-314">Method animateFile</span></span>

```xpp
public str animateFile([str value])
```

### <a name="parameters---animatefile"></a><span data-ttu-id="a34b8-315">パラメーター - animateFile</span><span class="sxs-lookup"><span data-stu-id="a34b8-315">Parameters - animateFile</span></span>

<span data-ttu-id="a34b8-316">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-316">value</span></span>  

### <a name="return-value---animatefile"></a><span data-ttu-id="a34b8-317">戻り値 - animateFile</span><span class="sxs-lookup"><span data-stu-id="a34b8-317">Return Value - animateFile</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="a34b8-318">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a34b8-318">Method autoDeclaration</span></span>

<span data-ttu-id="a34b8-319">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-319">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="a34b8-320">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a34b8-320">Parameters - autoDeclaration</span></span>

<span data-ttu-id="a34b8-321">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-321">value</span></span>  
<span data-ttu-id="a34b8-322">指定されている場合、プロパティはこの値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-322">The property is set to this value, if supplied.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="a34b8-323">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a34b8-323">Return Value - autoDeclaration</span></span>

<span data-ttu-id="a34b8-324">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-324">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="a34b8-325">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a34b8-325">Remarks - autoDeclaration</span></span>

<span data-ttu-id="a34b8-326">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-326">Controls cannot have identical names.</span></span>

## <a name="method-autoplay"></a><span data-ttu-id="a34b8-327">メソッド autoPlay</span><span class="sxs-lookup"><span data-stu-id="a34b8-327">Method autoPlay</span></span>

```xpp
public boolean autoPlay([boolean value])
```

### <a name="parameters---autoplay"></a><span data-ttu-id="a34b8-328">パラメーター - autoPlay</span><span class="sxs-lookup"><span data-stu-id="a34b8-328">Parameters - autoPlay</span></span>

<span data-ttu-id="a34b8-329">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-329">value</span></span>  

### <a name="return-value---autoplay"></a><span data-ttu-id="a34b8-330">戻り値 - autoPlay</span><span class="sxs-lookup"><span data-stu-id="a34b8-330">Return Value - autoPlay</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="a34b8-331">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="a34b8-331">Method beginDrag</span></span>

<span data-ttu-id="a34b8-332">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-332">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="a34b8-333">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="a34b8-333">Parameters - beginDrag</span></span>

<span data-ttu-id="a34b8-334">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-334">x</span></span>  
<span data-ttu-id="a34b8-335">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-335">An integer value that indicates the y-coordinate of the mouse pointer.</span></span>

<!-- -->

<span data-ttu-id="a34b8-336">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-336">y</span></span>  
<span data-ttu-id="a34b8-337">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-337">An integer value that indicates the y-coordinate of the mouse pointer.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="a34b8-338">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="a34b8-338">Return Value - beginDrag</span></span>

<span data-ttu-id="a34b8-339">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-339">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="a34b8-340">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="a34b8-340">Remarks - beginDrag</span></span>

<span data-ttu-id="a34b8-341">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-341">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="a34b8-342">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-342">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-border"></a><span data-ttu-id="a34b8-343">メソッド border</span><span class="sxs-lookup"><span data-stu-id="a34b8-343">Method border</span></span>

<span data-ttu-id="a34b8-344">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-344">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="a34b8-345">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="a34b8-345">Parameters - border</span></span>

<span data-ttu-id="a34b8-346">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-346">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="a34b8-347">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="a34b8-347">Return Value - border</span></span>

<span data-ttu-id="a34b8-348">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="a34b8-348">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="a34b8-349">備考 - border</span><span class="sxs-lookup"><span data-stu-id="a34b8-349">Remarks - border</span></span>

<span data-ttu-id="a34b8-350">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-350">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="a34b8-351">値です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-351">Value.</span></span> | <span data-ttu-id="a34b8-352">説明。</span><span class="sxs-lookup"><span data-stu-id="a34b8-352">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="a34b8-353">0</span><span class="sxs-lookup"><span data-stu-id="a34b8-353">0</span></span>      | <span data-ttu-id="a34b8-354">自動。</span><span class="sxs-lookup"><span data-stu-id="a34b8-354">Auto.</span></span>        |
| <span data-ttu-id="a34b8-355">1</span><span class="sxs-lookup"><span data-stu-id="a34b8-355">1</span></span>      | <span data-ttu-id="a34b8-356">3D。</span><span class="sxs-lookup"><span data-stu-id="a34b8-356">3D.</span></span>          |
| <span data-ttu-id="a34b8-357">2</span><span class="sxs-lookup"><span data-stu-id="a34b8-357">2</span></span>      | <span data-ttu-id="a34b8-358">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="a34b8-358">Single line.</span></span> |
| <span data-ttu-id="a34b8-359">3</span><span class="sxs-lookup"><span data-stu-id="a34b8-359">3</span></span>      | <span data-ttu-id="a34b8-360">均一。</span><span class="sxs-lookup"><span data-stu-id="a34b8-360">Flat.</span></span>        |
| <span data-ttu-id="a34b8-361">4</span><span class="sxs-lookup"><span data-stu-id="a34b8-361">4</span></span>      | <span data-ttu-id="a34b8-362">なし。</span><span class="sxs-lookup"><span data-stu-id="a34b8-362">None.</span></span>        |

## <a name="method-calccontrolsize"></a><span data-ttu-id="a34b8-363">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="a34b8-363">Method calcControlSize</span></span>

<span data-ttu-id="a34b8-364">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-364">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="a34b8-365">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="a34b8-365">Parameters - calcControlSize</span></span>

<span data-ttu-id="a34b8-366">chars</span><span class="sxs-lookup"><span data-stu-id="a34b8-366">chars</span></span>  
<span data-ttu-id="a34b8-367">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="a34b8-367">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="a34b8-368">明細行</span><span class="sxs-lookup"><span data-stu-id="a34b8-368">lines</span></span>  
<span data-ttu-id="a34b8-369">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="a34b8-369">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="a34b8-370">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="a34b8-370">Return Value - calcControlSize</span></span>

<span data-ttu-id="a34b8-371">幅と高さのあるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="a34b8-371">The container that has the width and height.</span></span>

## <a name="method-center"></a><span data-ttu-id="a34b8-372">メソッド center</span><span class="sxs-lookup"><span data-stu-id="a34b8-372">Method center</span></span>

```xpp
public boolean center([boolean value])
```

### <a name="parameters---center"></a><span data-ttu-id="a34b8-373">パラメーター - center</span><span class="sxs-lookup"><span data-stu-id="a34b8-373">Parameters - center</span></span>

<span data-ttu-id="a34b8-374">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-374">value</span></span>  

### <a name="return-value---center"></a><span data-ttu-id="a34b8-375">戻り値 - center</span><span class="sxs-lookup"><span data-stu-id="a34b8-375">Return Value - center</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="a34b8-376">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="a34b8-376">Method configurationKey</span></span>

<span data-ttu-id="a34b8-377">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-377">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="a34b8-378">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a34b8-378">Parameters - configurationKey</span></span>

<span data-ttu-id="a34b8-379">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-379">value</span></span>  
<span data-ttu-id="a34b8-380">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-380">The ID of the configuration key that is being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="a34b8-381">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a34b8-381">Return Value - configurationKey</span></span>

<span data-ttu-id="a34b8-382">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="a34b8-382">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="a34b8-383">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a34b8-383">Remarks - configurationKey</span></span>

<span data-ttu-id="a34b8-384">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-384">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="a34b8-385">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-385">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="a34b8-386">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="a34b8-386">Method configurationKeyEx</span></span>

<span data-ttu-id="a34b8-387">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-387">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="a34b8-388">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="a34b8-388">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="a34b8-389">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="a34b8-389">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="a34b8-390">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="a34b8-390">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="a34b8-391">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-391">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="a34b8-392">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-392">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="a34b8-393">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-393">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="a34b8-394">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a34b8-394">Method countryRegionCodes</span></span>

<span data-ttu-id="a34b8-395">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-395">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="a34b8-396">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a34b8-396">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="a34b8-397">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-397">value</span></span>  
<span data-ttu-id="a34b8-398">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-398">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="a34b8-399">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a34b8-399">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="a34b8-400">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="a34b8-400">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="a34b8-401">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a34b8-401">Method dataRelationPath</span></span>

<span data-ttu-id="a34b8-402">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-402">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="a34b8-403">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a34b8-403">Parameters - dataRelationPath</span></span>

<span data-ttu-id="a34b8-404">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-404">value</span></span>  
<span data-ttu-id="a34b8-405">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-405">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="a34b8-406">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a34b8-406">Return Value - dataRelationPath</span></span>

<span data-ttu-id="a34b8-407">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="a34b8-407">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="a34b8-408">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a34b8-408">Remarks - dataRelationPath</span></span>

<span data-ttu-id="a34b8-409">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-409">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="a34b8-410">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="a34b8-410">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="a34b8-411">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="a34b8-411">Method displayTarget</span></span>

<span data-ttu-id="a34b8-412">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-412">Gets or sets the value that indicates whether the control is displayed in the client, or in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="a34b8-413">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="a34b8-413">Parameters - displayTarget</span></span>

<span data-ttu-id="a34b8-414">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-414">value</span></span>  
<span data-ttu-id="a34b8-415">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-415">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="a34b8-416">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="a34b8-416">Return Value - displayTarget</span></span>

<span data-ttu-id="a34b8-417">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-417">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="a34b8-418">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="a34b8-418">Method dragDrop</span></span>

<span data-ttu-id="a34b8-419">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-419">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="a34b8-420">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="a34b8-420">Parameters - dragDrop</span></span>

<span data-ttu-id="a34b8-421">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-421">value</span></span>  
<span data-ttu-id="a34b8-422">ドラッグ アンド ドロップの動作が有効かどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-422">An Integer data type that indicates whether the drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="a34b8-423">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="a34b8-423">Return Value - dragDrop</span></span>

<span data-ttu-id="a34b8-424">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-424">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="a34b8-425">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="a34b8-425">Remarks - dragDrop</span></span>

<span data-ttu-id="a34b8-426">FormControl::dragLeave、FormControl::dragOver、および FormControl::dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-426">Use the FormControl::dragLeave, FormControl::dragOver, and FormControl::dragOverEx methods to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="a34b8-427">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="a34b8-427">Method dragOver</span></span>

<span data-ttu-id="a34b8-428">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-428">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="a34b8-429">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="a34b8-429">Parameters - dragOver</span></span>

<span data-ttu-id="a34b8-430">dragSource</span><span class="sxs-lookup"><span data-stu-id="a34b8-430">dragSource</span></span>  
<span data-ttu-id="a34b8-431">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-431">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-432">dragMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-432">dragMode</span></span>  
<span data-ttu-id="a34b8-433">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-433">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-434">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-434">x</span></span>  
<span data-ttu-id="a34b8-435">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-435">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-436">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-436">y</span></span>  
<span data-ttu-id="a34b8-437">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-437">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="a34b8-438">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="a34b8-438">Return Value - dragOver</span></span>

<span data-ttu-id="a34b8-439">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-439">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="a34b8-440">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="a34b8-440">Method dragOverEx</span></span>

<span data-ttu-id="a34b8-441">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-441">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="a34b8-442">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="a34b8-442">Parameters - dragOverEx</span></span>

<span data-ttu-id="a34b8-443">dragSource</span><span class="sxs-lookup"><span data-stu-id="a34b8-443">dragSource</span></span>  
<span data-ttu-id="a34b8-444">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-444">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-445">dragMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-445">dragMode</span></span>  
<span data-ttu-id="a34b8-446">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-446">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-447">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-447">x</span></span>  
<span data-ttu-id="a34b8-448">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-448">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-449">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-449">y</span></span>  
<span data-ttu-id="a34b8-450">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-450">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="a34b8-451">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="a34b8-451">Return Value - dragOverEx</span></span>

<span data-ttu-id="a34b8-452">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-452">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="a34b8-453">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="a34b8-453">Method dragText</span></span>

<span data-ttu-id="a34b8-454">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-454">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="a34b8-455">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="a34b8-455">Return Value - dragText</span></span>

<span data-ttu-id="a34b8-456">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="a34b8-456">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="a34b8-457">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="a34b8-457">Method enabled</span></span>

<span data-ttu-id="a34b8-458">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-458">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="a34b8-459">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="a34b8-459">Parameters - enabled</span></span>

<span data-ttu-id="a34b8-460">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-460">value</span></span>  
<span data-ttu-id="a34b8-461">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-461">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="a34b8-462">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="a34b8-462">Return Value - enabled</span></span>

<span data-ttu-id="a34b8-463">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-463">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="a34b8-464">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="a34b8-464">Remarks - enabled</span></span>

<span data-ttu-id="a34b8-465">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-465">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="a34b8-466">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-466">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="a34b8-467">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-467">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="a34b8-468">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="a34b8-468">Method hasChanged</span></span>

<span data-ttu-id="a34b8-469">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-469">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="a34b8-470">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="a34b8-470">Parameters - hasChanged</span></span>

<span data-ttu-id="a34b8-471">val</span><span class="sxs-lookup"><span data-stu-id="a34b8-471">val</span></span>  
<span data-ttu-id="a34b8-472">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-472">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="a34b8-473">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="a34b8-473">Return Value - hasChanged</span></span>

<span data-ttu-id="a34b8-474">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-474">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="a34b8-475">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="a34b8-475">Method hasUserSetting</span></span>

<span data-ttu-id="a34b8-476">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-476">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="a34b8-477">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="a34b8-477">Return Value - hasUserSetting</span></span>

<span data-ttu-id="a34b8-478">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-478">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="a34b8-479">メソッド height</span><span class="sxs-lookup"><span data-stu-id="a34b8-479">Method height</span></span>

<span data-ttu-id="a34b8-480">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-480">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="a34b8-481">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="a34b8-481">Parameters - height</span></span>

<span data-ttu-id="a34b8-482">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-482">value</span></span>  
<span data-ttu-id="a34b8-483">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="a34b8-483">An Integer data type that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="a34b8-484">モード</span><span class="sxs-lookup"><span data-stu-id="a34b8-484">mode</span></span>  
<span data-ttu-id="a34b8-485">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="a34b8-485">An Integer data type that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="a34b8-486">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="a34b8-486">Return Value - height</span></span>

<span data-ttu-id="a34b8-487">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="a34b8-487">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="a34b8-488">備考 - height</span><span class="sxs-lookup"><span data-stu-id="a34b8-488">Remarks - height</span></span>

<span data-ttu-id="a34b8-489">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-489">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="a34b8-490">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="a34b8-490">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="a34b8-491">モード。</span><span class="sxs-lookup"><span data-stu-id="a34b8-491">Mode.</span></span>            | <span data-ttu-id="a34b8-492">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="a34b8-492">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34b8-493">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="a34b8-493">-1 Exact.</span></span>        | <span data-ttu-id="a34b8-494">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-494">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a34b8-495">0 自動。</span><span class="sxs-lookup"><span data-stu-id="a34b8-495">0 Auto.</span></span>          | <span data-ttu-id="a34b8-496">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-496">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a34b8-497">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="a34b8-497">1 Column height.</span></span> | <span data-ttu-id="a34b8-498">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-498">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="a34b8-499">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-499">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="a34b8-500">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-500">Method heightMode</span></span>

<span data-ttu-id="a34b8-501">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-501">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="a34b8-502">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-502">Parameters - heightMode</span></span>

<span data-ttu-id="a34b8-503">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-503">value</span></span>  
<span data-ttu-id="a34b8-504">コントロールの高さの計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-504">An Integer data type value that indicates how the control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="a34b8-505">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-505">Return Value - heightMode</span></span>

<span data-ttu-id="a34b8-506">計算モード。</span><span class="sxs-lookup"><span data-stu-id="a34b8-506">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="a34b8-507">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-507">Remarks - heightMode</span></span>

<span data-ttu-id="a34b8-508">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="a34b8-508">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="a34b8-509">モード。</span><span class="sxs-lookup"><span data-stu-id="a34b8-509">Mode.</span></span>          | <span data-ttu-id="a34b8-510">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="a34b8-510">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34b8-511">正確。</span><span class="sxs-lookup"><span data-stu-id="a34b8-511">Exact.</span></span>         | <span data-ttu-id="a34b8-512">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-512">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a34b8-513">自動。</span><span class="sxs-lookup"><span data-stu-id="a34b8-513">Auto.</span></span>          | <span data-ttu-id="a34b8-514">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-514">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a34b8-515">列の高さ</span><span class="sxs-lookup"><span data-stu-id="a34b8-515">Column height.</span></span> | <span data-ttu-id="a34b8-516">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-516">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="a34b8-517">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-517">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="a34b8-518">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-518">Method heightValue</span></span>

<span data-ttu-id="a34b8-519">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-519">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="a34b8-520">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-520">Parameters - heightValue</span></span>

<span data-ttu-id="a34b8-521">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-521">value</span></span>  
<span data-ttu-id="a34b8-522">高さをピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-522">An Integer data type that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="a34b8-523">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-523">Return Value - heightValue</span></span>

<span data-ttu-id="a34b8-524">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="a34b8-524">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="a34b8-525">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-525">Remarks - heightValue</span></span>

<span data-ttu-id="a34b8-526">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-526">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="a34b8-527">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="a34b8-527">Method helpField</span></span>

<span data-ttu-id="a34b8-528">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-528">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="a34b8-529">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="a34b8-529">Return Value - helpField</span></span>

<span data-ttu-id="a34b8-530">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="a34b8-530">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="a34b8-531">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="a34b8-531">Remarks - helpField</span></span>

<span data-ttu-id="a34b8-532">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-532">The helpField method cannot be used to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="a34b8-533">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="a34b8-533">Method helpText</span></span>

<span data-ttu-id="a34b8-534">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-534">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="a34b8-535">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="a34b8-535">Parameters - helpText</span></span>

<span data-ttu-id="a34b8-536">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-536">value</span></span>  
<span data-ttu-id="a34b8-537">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-537">The value that is assigned as the help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="a34b8-538">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="a34b8-538">Return Value - helpText</span></span>

<span data-ttu-id="a34b8-539">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="a34b8-539">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="a34b8-540">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="a34b8-540">Remarks - helpText</span></span>

<span data-ttu-id="a34b8-541">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-541">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="a34b8-542">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-542">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="a34b8-543">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a34b8-543">Method hierarchyParent</span></span>

<span data-ttu-id="a34b8-544">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-544">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="a34b8-545">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a34b8-545">Parameters - hierarchyParent</span></span>

<span data-ttu-id="a34b8-546">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-546">value</span></span>  
<span data-ttu-id="a34b8-547">コントロールの HierarchyParent 値として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-547">The value to assign as the HierarchyParent value of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="a34b8-548">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a34b8-548">Return Value - hierarchyParent</span></span>

<span data-ttu-id="a34b8-549">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-549">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="a34b8-550">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="a34b8-550">Method hWnd</span></span>

<span data-ttu-id="a34b8-551">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-551">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="a34b8-552">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="a34b8-552">Return Value - hWnd</span></span>

<span data-ttu-id="a34b8-553">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="a34b8-553">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="a34b8-554">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="a34b8-554">Remarks - hWnd</span></span>

<span data-ttu-id="a34b8-555">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-555">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="a34b8-556">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="a34b8-556">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="a34b8-557">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="a34b8-557">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="a34b8-558">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="a34b8-558">Method isDisplayed</span></span>

<span data-ttu-id="a34b8-559">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-559">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="a34b8-560">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="a34b8-560">Return Value - isDisplayed</span></span>

<span data-ttu-id="a34b8-561">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-561">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="a34b8-562">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="a34b8-562">Remarks - isDisplayed</span></span>

<span data-ttu-id="a34b8-563">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-563">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="a34b8-564">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="a34b8-564">Method isRestricted</span></span>

<span data-ttu-id="a34b8-565">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-565">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="a34b8-566">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="a34b8-566">Return Value - isRestricted</span></span>

<span data-ttu-id="a34b8-567">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-567">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="a34b8-568">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="a34b8-568">Method isUserSetupEnabled</span></span>

<span data-ttu-id="a34b8-569">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-569">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="a34b8-570">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="a34b8-570">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="a34b8-571">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="a34b8-571">neededSetupRights</span></span>  
<span data-ttu-id="a34b8-572">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-572">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span> <span data-ttu-id="a34b8-573">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a34b8-573">For more information, see �Remarks.�</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="a34b8-574">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="a34b8-574">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="a34b8-575">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-575">true if the control, design, and parent container allow for the level of customization that is specified by the neededSetupRights parameter; otherwise false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="a34b8-576">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="a34b8-576">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="a34b8-577">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-577">The following table describes the values for the neededSetupRights parameters.</span></span>

|                                  |                                                                                                                                 |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34b8-578">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="a34b8-578">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="a34b8-579">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-579">No changes can be made to the control.</span></span> <span data-ttu-id="a34b8-580">neededSetupRights にこの値を使用すると、常に、true が返ってきます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-580">Using this value for neededSetupRights always returns true.</span></span>                              |
| <span data-ttu-id="a34b8-581">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="a34b8-581">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="a34b8-582">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-582">The user can change the editable, visible, skip, label and width properties of the control.</span></span> <span data-ttu-id="a34b8-583">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-583">The user cannot move the control.</span></span>   |
| <span data-ttu-id="a34b8-584">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="a34b8-584">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="a34b8-585">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-585">The user can change the editable, visible, skip, label and width properties of the control.</span></span> <span data-ttu-id="a34b8-586">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-586">The user can also move the control.</span></span> |

<span data-ttu-id="a34b8-587">このメソッドは、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメーターで指定されたレベル以上の場合にのみ true を返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-587">This method returns true only if the AllowUserSetup property for the design and all parent containers is at least as high as the level that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-leave"></a><span data-ttu-id="a34b8-588">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="a34b8-588">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="a34b8-589">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="a34b8-589">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="a34b8-590">メソッド left</span><span class="sxs-lookup"><span data-stu-id="a34b8-590">Method left</span></span>

<span data-ttu-id="a34b8-591">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-591">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="a34b8-592">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="a34b8-592">Parameters - left</span></span>

<span data-ttu-id="a34b8-593">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-593">value</span></span>  
<span data-ttu-id="a34b8-594">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-594">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="a34b8-595">モード</span><span class="sxs-lookup"><span data-stu-id="a34b8-595">mode</span></span>  
<span data-ttu-id="a34b8-596">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-596">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="a34b8-597">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="a34b8-597">Return Value - left</span></span>

<span data-ttu-id="a34b8-598">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="a34b8-598">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="a34b8-599">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-599">Method leftMode</span></span>

<span data-ttu-id="a34b8-600">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-600">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="a34b8-601">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-601">Parameters - leftMode</span></span>

<span data-ttu-id="a34b8-602">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-602">value</span></span>  
<span data-ttu-id="a34b8-603">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-603">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="a34b8-604">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-604">Return Value - leftMode</span></span>

<span data-ttu-id="a34b8-605">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="a34b8-605">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="a34b8-606">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-606">Method leftValue</span></span>

<span data-ttu-id="a34b8-607">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-607">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="a34b8-608">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-608">Parameters - leftValue</span></span>

<span data-ttu-id="a34b8-609">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-609">value</span></span>  
<span data-ttu-id="a34b8-610">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-610">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="a34b8-611">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-611">Return Value - leftValue</span></span>

<span data-ttu-id="a34b8-612">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="a34b8-612">The horizontal position of the control in the form.</span></span>

## <a name="method-loops"></a><span data-ttu-id="a34b8-613">メソッド loops</span><span class="sxs-lookup"><span data-stu-id="a34b8-613">Method loops</span></span>

```xpp
public int loops([int value])
```

### <a name="parameters---loops"></a><span data-ttu-id="a34b8-614">パラメーター - loops</span><span class="sxs-lookup"><span data-stu-id="a34b8-614">Parameters - loops</span></span>

<span data-ttu-id="a34b8-615">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-615">value</span></span>  

### <a name="return-value---loops"></a><span data-ttu-id="a34b8-616">戻り値 - loops</span><span class="sxs-lookup"><span data-stu-id="a34b8-616">Return Value - loops</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="a34b8-617">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="a34b8-617">Method markAsUserAdd</span></span>

<span data-ttu-id="a34b8-618">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="a34b8-618">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="a34b8-619">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="a34b8-619">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="a34b8-620">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-620">value</span></span>  
<span data-ttu-id="a34b8-621">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-621">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="a34b8-622">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="a34b8-622">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="a34b8-623">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-623">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="a34b8-624">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="a34b8-624">Method mouseDblClick</span></span>

<span data-ttu-id="a34b8-625">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-625">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="a34b8-626">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="a34b8-626">Parameters - mouseDblClick</span></span>

<span data-ttu-id="a34b8-627">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-627">x</span></span>  
<span data-ttu-id="a34b8-628">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-628">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-629">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-629">y</span></span>  
<span data-ttu-id="a34b8-630">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-630">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-631">ボタン</span><span class="sxs-lookup"><span data-stu-id="a34b8-631">button</span></span>  
<span data-ttu-id="a34b8-632">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-632">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-633">Ctrl</span><span class="sxs-lookup"><span data-stu-id="a34b8-633">Ctrl</span></span>  
<span data-ttu-id="a34b8-634">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-634">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-635">シフト</span><span class="sxs-lookup"><span data-stu-id="a34b8-635">Shift</span></span>  
<span data-ttu-id="a34b8-636">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-636">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="a34b8-637">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="a34b8-637">Return Value - mouseDblClick</span></span>

<span data-ttu-id="a34b8-638">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-638">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="a34b8-639">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="a34b8-639">Remarks - mouseDblClick</span></span>

<span data-ttu-id="a34b8-640">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-640">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="a34b8-641">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="a34b8-641">Method mouseDown</span></span>

<span data-ttu-id="a34b8-642">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-642">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="a34b8-643">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="a34b8-643">Parameters - mouseDown</span></span>

<span data-ttu-id="a34b8-644">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-644">x</span></span>  
<span data-ttu-id="a34b8-645">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-645">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-646">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-646">y</span></span>  
<span data-ttu-id="a34b8-647">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-647">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-648">ボタン</span><span class="sxs-lookup"><span data-stu-id="a34b8-648">button</span></span>  
<span data-ttu-id="a34b8-649">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-649">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-650">Ctrl</span><span class="sxs-lookup"><span data-stu-id="a34b8-650">Ctrl</span></span>  
<span data-ttu-id="a34b8-651">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-651">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-652">シフト</span><span class="sxs-lookup"><span data-stu-id="a34b8-652">Shift</span></span>  
<span data-ttu-id="a34b8-653">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-653">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="a34b8-654">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="a34b8-654">Return Value - mouseDown</span></span>

<span data-ttu-id="a34b8-655">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-655">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="a34b8-656">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="a34b8-656">Remarks - mouseDown</span></span>

<span data-ttu-id="a34b8-657">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-657">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="a34b8-658">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-658">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="a34b8-659">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="a34b8-659">Method mouseMove</span></span>

<span data-ttu-id="a34b8-660">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-660">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="a34b8-661">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="a34b8-661">Parameters - mouseMove</span></span>

<span data-ttu-id="a34b8-662">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-662">x</span></span>  
<span data-ttu-id="a34b8-663">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-663">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-664">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-664">y</span></span>  
<span data-ttu-id="a34b8-665">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-665">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-666">ボタン</span><span class="sxs-lookup"><span data-stu-id="a34b8-666">button</span></span>  
<span data-ttu-id="a34b8-667">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-667">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-668">Ctrl</span><span class="sxs-lookup"><span data-stu-id="a34b8-668">Ctrl</span></span>  
<span data-ttu-id="a34b8-669">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-669">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-670">シフト</span><span class="sxs-lookup"><span data-stu-id="a34b8-670">Shift</span></span>  
<span data-ttu-id="a34b8-671">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-671">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="a34b8-672">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="a34b8-672">Return Value - mouseMove</span></span>

<span data-ttu-id="a34b8-673">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-673">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="a34b8-674">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="a34b8-674">Remarks - mouseMove</span></span>

<span data-ttu-id="a34b8-675">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-675">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="a34b8-676">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="a34b8-676">Method mouseUp</span></span>

<span data-ttu-id="a34b8-677">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-677">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="a34b8-678">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="a34b8-678">Parameters - mouseUp</span></span>

<span data-ttu-id="a34b8-679">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-679">x</span></span>  
<span data-ttu-id="a34b8-680">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-680">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-681">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-681">y</span></span>  
<span data-ttu-id="a34b8-682">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-682">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-683">ボタン</span><span class="sxs-lookup"><span data-stu-id="a34b8-683">button</span></span>  
<span data-ttu-id="a34b8-684">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-684">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-685">Ctrl</span><span class="sxs-lookup"><span data-stu-id="a34b8-685">Ctrl</span></span>  
<span data-ttu-id="a34b8-686">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-686">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-687">シフト</span><span class="sxs-lookup"><span data-stu-id="a34b8-687">Shift</span></span>  
<span data-ttu-id="a34b8-688">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-688">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="a34b8-689">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="a34b8-689">Return Value - mouseUp</span></span>

<span data-ttu-id="a34b8-690">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-690">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="a34b8-691">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="a34b8-691">Remarks - mouseUp</span></span>

<span data-ttu-id="a34b8-692">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-692">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="a34b8-693">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-693">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="a34b8-694">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a34b8-694">Method name</span></span>

<span data-ttu-id="a34b8-695">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-695">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="a34b8-696">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="a34b8-696">Parameters - name</span></span>

<span data-ttu-id="a34b8-697">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-697">value</span></span>  
<span data-ttu-id="a34b8-698">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-698">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="a34b8-699">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="a34b8-699">Return Value - name</span></span>

<span data-ttu-id="a34b8-700">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="a34b8-700">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="a34b8-701">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="a34b8-701">Remarks - name</span></span>

<span data-ttu-id="a34b8-702">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-702">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="a34b8-703">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-703">It must begin with a letter.</span></span>
-   <span data-ttu-id="a34b8-704">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-704">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="a34b8-705">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-705">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="a34b8-706">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-706">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="a34b8-707">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-707">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="a34b8-708">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="a34b8-708">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="a34b8-709">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="a34b8-709">Parameters - neededPermission</span></span>

<span data-ttu-id="a34b8-710">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-710">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="a34b8-711">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="a34b8-711">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="a34b8-712">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="a34b8-712">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="a34b8-713">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="a34b8-713">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="a34b8-714">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="a34b8-714">Method parentControl</span></span>

<span data-ttu-id="a34b8-715">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-715">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="a34b8-716">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="a34b8-716">Return Value - parentControl</span></span>

<span data-ttu-id="a34b8-717">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="a34b8-717">The parent control for the control.</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="a34b8-718">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="a34b8-718">Method securityKey</span></span>

<span data-ttu-id="a34b8-719">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-719">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="a34b8-720">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="a34b8-720">Parameters - securityKey</span></span>

<span data-ttu-id="a34b8-721">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-721">value</span></span>  
<span data-ttu-id="a34b8-722">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-722">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="a34b8-723">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="a34b8-723">Return Value - securityKey</span></span>

<span data-ttu-id="a34b8-724">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-724">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="a34b8-725">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="a34b8-725">Method showContextMenu</span></span>

<span data-ttu-id="a34b8-726">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-726">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="a34b8-727">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="a34b8-727">Parameters - showContextMenu</span></span>

<span data-ttu-id="a34b8-728">menuHandle</span><span class="sxs-lookup"><span data-stu-id="a34b8-728">menuHandle</span></span>  
<span data-ttu-id="a34b8-729">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="a34b8-729">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="a34b8-730">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="a34b8-730">Return Value - showContextMenu</span></span>

<span data-ttu-id="a34b8-731">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-731">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="a34b8-732">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="a34b8-732">Method skip</span></span>

<span data-ttu-id="a34b8-733">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-733">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="a34b8-734">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="a34b8-734">Parameters - skip</span></span>

<span data-ttu-id="a34b8-735">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-735">value</span></span>  
<span data-ttu-id="a34b8-736">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-736">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="a34b8-737">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="a34b8-737">Return Value - skip</span></span>

<span data-ttu-id="a34b8-738">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-738">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="a34b8-739">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="a34b8-739">Method toolTip</span></span>

<span data-ttu-id="a34b8-740">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-740">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="a34b8-741">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="a34b8-741">Return Value - toolTip</span></span>

<span data-ttu-id="a34b8-742">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="a34b8-742">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="a34b8-743">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="a34b8-743">Remarks - toolTip</span></span>

<span data-ttu-id="a34b8-744">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-744">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="a34b8-745">メソッド top</span><span class="sxs-lookup"><span data-stu-id="a34b8-745">Method top</span></span>

<span data-ttu-id="a34b8-746">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-746">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="a34b8-747">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="a34b8-747">Parameters - top</span></span>

<span data-ttu-id="a34b8-748">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-748">value</span></span>  
<span data-ttu-id="a34b8-749">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-749">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="a34b8-750">モード</span><span class="sxs-lookup"><span data-stu-id="a34b8-750">mode</span></span>  
<span data-ttu-id="a34b8-751">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-751">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="a34b8-752">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="a34b8-752">Return Value - top</span></span>

<span data-ttu-id="a34b8-753">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="a34b8-753">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="a34b8-754">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-754">Method topMode</span></span>

<span data-ttu-id="a34b8-755">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-755">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="a34b8-756">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-756">Parameters - topMode</span></span>

<span data-ttu-id="a34b8-757">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-757">value</span></span>  
<span data-ttu-id="a34b8-758">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-758">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="a34b8-759">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-759">Return Value - topMode</span></span>

<span data-ttu-id="a34b8-760">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="a34b8-760">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="a34b8-761">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-761">Method topValue</span></span>

<span data-ttu-id="a34b8-762">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-762">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="a34b8-763">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-763">Parameters - topValue</span></span>

<span data-ttu-id="a34b8-764">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-764">value</span></span>  
<span data-ttu-id="a34b8-765">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-765">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="a34b8-766">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-766">Return Value - topValue</span></span>

<span data-ttu-id="a34b8-767">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="a34b8-767">The vertical position of the control in the form.</span></span>

## <a name="method-transparent"></a><span data-ttu-id="a34b8-768">メソッド transparent</span><span class="sxs-lookup"><span data-stu-id="a34b8-768">Method transparent</span></span>

```xpp
public boolean transparent([boolean value])
```

### <a name="parameters---transparent"></a><span data-ttu-id="a34b8-769">パラメーター - transparent</span><span class="sxs-lookup"><span data-stu-id="a34b8-769">Parameters - transparent</span></span>

<span data-ttu-id="a34b8-770">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-770">value</span></span>  

### <a name="return-value---transparent"></a><span data-ttu-id="a34b8-771">戻り値 - transparent</span><span class="sxs-lookup"><span data-stu-id="a34b8-771">Return Value - transparent</span></span>

## <a name="method-type"></a><span data-ttu-id="a34b8-772">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="a34b8-772">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="a34b8-773">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="a34b8-773">Parameters - type</span></span>

<span data-ttu-id="a34b8-774">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-774">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="a34b8-775">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="a34b8-775">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="a34b8-776">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="a34b8-776">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="a34b8-777">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="a34b8-777">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="a34b8-778">データ</span><span class="sxs-lookup"><span data-stu-id="a34b8-778">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="a34b8-779">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="a34b8-779">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="a34b8-780">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="a34b8-780">Method userData</span></span>

<span data-ttu-id="a34b8-781">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-781">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="a34b8-782">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="a34b8-782">Parameters - userData</span></span>

<span data-ttu-id="a34b8-783">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-783">value</span></span>  
<span data-ttu-id="a34b8-784">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-784">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="a34b8-785">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="a34b8-785">Return Value - userData</span></span>

<span data-ttu-id="a34b8-786">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="a34b8-786">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="a34b8-787">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="a34b8-787">Method userDataItem</span></span>

<span data-ttu-id="a34b8-788">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-788">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="a34b8-789">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="a34b8-789">Parameters - userDataItem</span></span>

<span data-ttu-id="a34b8-790">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-790">value</span></span>  
<span data-ttu-id="a34b8-791">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-791">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="a34b8-792">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="a34b8-792">Return Value - userDataItem</span></span>

<span data-ttu-id="a34b8-793">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="a34b8-793">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="a34b8-794">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="a34b8-794">Method userDataItems</span></span>

<span data-ttu-id="a34b8-795">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-795">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="a34b8-796">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="a34b8-796">Parameters - userDataItems</span></span>

<span data-ttu-id="a34b8-797">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-797">value</span></span>  
<span data-ttu-id="a34b8-798">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-798">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="a34b8-799">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="a34b8-799">Return Value - userDataItems</span></span>

<span data-ttu-id="a34b8-800">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="a34b8-800">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="a34b8-801">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="a34b8-801">Method userDisable</span></span>

<span data-ttu-id="a34b8-802">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-802">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="a34b8-803">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="a34b8-803">Parameters - userDisable</span></span>

<span data-ttu-id="a34b8-804">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-804">value</span></span>  
<span data-ttu-id="a34b8-805">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-805">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="a34b8-806">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="a34b8-806">Return Value - userDisable</span></span>

<span data-ttu-id="a34b8-807">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-807">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="a34b8-808">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="a34b8-808">Method userHeight</span></span>

<span data-ttu-id="a34b8-809">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-809">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="a34b8-810">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="a34b8-810">Parameters - userHeight</span></span>

<span data-ttu-id="a34b8-811">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-811">value</span></span>  
<span data-ttu-id="a34b8-812">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-812">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="a34b8-813">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="a34b8-813">Return Value - userHeight</span></span>

<span data-ttu-id="a34b8-814">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="a34b8-814">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="a34b8-815">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="a34b8-815">Method userHide</span></span>

<span data-ttu-id="a34b8-816">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-816">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="a34b8-817">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="a34b8-817">Parameters - userHide</span></span>

<span data-ttu-id="a34b8-818">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-818">value</span></span>  
<span data-ttu-id="a34b8-819">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-819">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="a34b8-820">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="a34b8-820">Return Value - userHide</span></span>

<span data-ttu-id="a34b8-821">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-821">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="a34b8-822">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="a34b8-822">Remarks - userHide</span></span>

<span data-ttu-id="a34b8-823">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-823">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="a34b8-824">右クリックすると、コントロールを非表示または表示できるメニューが起動します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-824">Right-clicking invokes a menu that enables the control to be hidden or displayed.</span></span> <span data-ttu-id="a34b8-825">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-825">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="a34b8-826">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="a34b8-826">Method userOrgContainer</span></span>

<span data-ttu-id="a34b8-827">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-827">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="a34b8-828">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="a34b8-828">Parameters - userOrgContainer</span></span>

<span data-ttu-id="a34b8-829">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-829">value</span></span>  
<span data-ttu-id="a34b8-830">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-830">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="a34b8-831">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="a34b8-831">Return Value - userOrgContainer</span></span>

<span data-ttu-id="a34b8-832">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="a34b8-832">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="a34b8-833">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="a34b8-833">Method userOrgSibling</span></span>

<span data-ttu-id="a34b8-834">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-834">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="a34b8-835">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="a34b8-835">Parameters - userOrgSibling</span></span>

<span data-ttu-id="a34b8-836">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-836">value</span></span>  
<span data-ttu-id="a34b8-837">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-837">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="a34b8-838">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="a34b8-838">Return Value - userOrgSibling</span></span>

<span data-ttu-id="a34b8-839">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="a34b8-839">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="a34b8-840">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="a34b8-840">Method userPromptText</span></span>

<span data-ttu-id="a34b8-841">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-841">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="a34b8-842">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="a34b8-842">Parameters - userPromptText</span></span>

<span data-ttu-id="a34b8-843">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-843">value</span></span>  
<span data-ttu-id="a34b8-844">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-844">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="a34b8-845">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="a34b8-845">Return Value - userPromptText</span></span>

<span data-ttu-id="a34b8-846">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="a34b8-846">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="a34b8-847">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a34b8-847">Method userSecurityLevel</span></span>

<span data-ttu-id="a34b8-848">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-848">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="a34b8-849">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a34b8-849">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="a34b8-850">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-850">value</span></span>  
<span data-ttu-id="a34b8-851">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-851">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="a34b8-852">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a34b8-852">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="a34b8-853">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="a34b8-853">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="a34b8-854">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="a34b8-854">Method userSkip</span></span>

<span data-ttu-id="a34b8-855">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-855">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="a34b8-856">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="a34b8-856">Parameters - userSkip</span></span>

<span data-ttu-id="a34b8-857">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-857">value</span></span>  
<span data-ttu-id="a34b8-858">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-858">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="a34b8-859">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-859">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="a34b8-860">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="a34b8-860">Return Value - userSkip</span></span>

<span data-ttu-id="a34b8-861">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="a34b8-861">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="a34b8-862">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="a34b8-862">Method userWidth</span></span>

<span data-ttu-id="a34b8-863">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-863">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="a34b8-864">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="a34b8-864">Parameters - userWidth</span></span>

<span data-ttu-id="a34b8-865">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-865">value</span></span>  
<span data-ttu-id="a34b8-866">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-866">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="a34b8-867">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="a34b8-867">Return Value - userWidth</span></span>

<span data-ttu-id="a34b8-868">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-868">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="a34b8-869">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="a34b8-869">Remarks - userWidth</span></span>

<span data-ttu-id="a34b8-870">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-870">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="a34b8-871">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻りは 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-871">For example, if the user has specified 30 characters as the width for the control, the return is 6 \* 30 = 180.</span></span> <span data-ttu-id="a34b8-872">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-872">To specify the width of the control in characters, users can right-click the control to invoke the setup form in which the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="a34b8-873">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a34b8-873">Method verticalSpacing</span></span>

<span data-ttu-id="a34b8-874">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-874">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="a34b8-875">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a34b8-875">Parameters - verticalSpacing</span></span>

<span data-ttu-id="a34b8-876">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-876">value</span></span>  
<span data-ttu-id="a34b8-877">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-877">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="a34b8-878">モード</span><span class="sxs-lookup"><span data-stu-id="a34b8-878">mode</span></span>  
<span data-ttu-id="a34b8-879">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-879">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="a34b8-880">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a34b8-880">Return Value - verticalSpacing</span></span>

<span data-ttu-id="a34b8-881">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="a34b8-881">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="a34b8-882">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-882">Method verticalSpacingMode</span></span>

<span data-ttu-id="a34b8-883">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-883">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="a34b8-884">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-884">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="a34b8-885">モード</span><span class="sxs-lookup"><span data-stu-id="a34b8-885">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="a34b8-886">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-886">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="a34b8-887">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="a34b8-887">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="a34b8-888">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-888">Method verticalSpacingValue</span></span>

<span data-ttu-id="a34b8-889">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-889">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="a34b8-890">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-890">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="a34b8-891">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-891">value</span></span>  
<span data-ttu-id="a34b8-892">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="a34b8-892">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="a34b8-893">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-893">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="a34b8-894">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="a34b8-894">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="a34b8-895">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="a34b8-895">Method visible</span></span>

<span data-ttu-id="a34b8-896">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-896">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="a34b8-897">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="a34b8-897">Parameters - visible</span></span>

<span data-ttu-id="a34b8-898">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-898">value</span></span>  
<span data-ttu-id="a34b8-899">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-899">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="a34b8-900">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="a34b8-900">Return Value - visible</span></span>

<span data-ttu-id="a34b8-901">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="a34b8-901">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="a34b8-902">メソッド width</span><span class="sxs-lookup"><span data-stu-id="a34b8-902">Method width</span></span>

<span data-ttu-id="a34b8-903">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-903">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="a34b8-904">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="a34b8-904">Parameters - width</span></span>

<span data-ttu-id="a34b8-905">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-905">value</span></span>  
<span data-ttu-id="a34b8-906">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="a34b8-906">An Integer data type that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="a34b8-907">モード</span><span class="sxs-lookup"><span data-stu-id="a34b8-907">mode</span></span>  
<span data-ttu-id="a34b8-908">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="a34b8-908">An Integer data type that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="a34b8-909">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="a34b8-909">Return Value - width</span></span>

<span data-ttu-id="a34b8-910">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="a34b8-910">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="a34b8-911">備考 - width</span><span class="sxs-lookup"><span data-stu-id="a34b8-911">Remarks - width</span></span>

<span data-ttu-id="a34b8-912">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-912">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="a34b8-913">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="a34b8-913">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="a34b8-914">モード。</span><span class="sxs-lookup"><span data-stu-id="a34b8-914">Mode.</span></span>           | <span data-ttu-id="a34b8-915">幅計算。</span><span class="sxs-lookup"><span data-stu-id="a34b8-915">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34b8-916">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="a34b8-916">-1 Exact.</span></span>       | <span data-ttu-id="a34b8-917">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-917">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a34b8-918">0 自動。</span><span class="sxs-lookup"><span data-stu-id="a34b8-918">0 Auto.</span></span>         | <span data-ttu-id="a34b8-919">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-919">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a34b8-920">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="a34b8-920">1 Column width.</span></span> | <span data-ttu-id="a34b8-921">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-921">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="a34b8-922">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-922">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="a34b8-923">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-923">Method widthMode</span></span>

<span data-ttu-id="a34b8-924">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-924">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="a34b8-925">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-925">Parameters - widthMode</span></span>

<span data-ttu-id="a34b8-926">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-926">value</span></span>  
<span data-ttu-id="a34b8-927">コントロールの幅の計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-927">An Integer data type value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="a34b8-928">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-928">Return Value - widthMode</span></span>

<span data-ttu-id="a34b8-929">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-929">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="a34b8-930">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-930">Remarks - widthMode</span></span>

<span data-ttu-id="a34b8-931">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="a34b8-931">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="a34b8-932">モード。</span><span class="sxs-lookup"><span data-stu-id="a34b8-932">Mode.</span></span>         | <span data-ttu-id="a34b8-933">幅計算。</span><span class="sxs-lookup"><span data-stu-id="a34b8-933">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34b8-934">正確。</span><span class="sxs-lookup"><span data-stu-id="a34b8-934">Exact.</span></span>        | <span data-ttu-id="a34b8-935">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-935">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a34b8-936">自動。</span><span class="sxs-lookup"><span data-stu-id="a34b8-936">Auto.</span></span>         | <span data-ttu-id="a34b8-937">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-937">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a34b8-938">列の幅。</span><span class="sxs-lookup"><span data-stu-id="a34b8-938">Column width.</span></span> | <span data-ttu-id="a34b8-939">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-939">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="a34b8-940">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="a34b8-940">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="a34b8-941">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-941">Method widthValue</span></span>

<span data-ttu-id="a34b8-942">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-942">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="a34b8-943">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-943">Parameters - widthValue</span></span>

<span data-ttu-id="a34b8-944">値</span><span class="sxs-lookup"><span data-stu-id="a34b8-944">value</span></span>  
<span data-ttu-id="a34b8-945">幅をピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-945">An Integer data type that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="a34b8-946">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-946">Return Value - widthValue</span></span>

<span data-ttu-id="a34b8-947">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="a34b8-947">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="a34b8-948">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="a34b8-948">Remarks - widthValue</span></span>

<span data-ttu-id="a34b8-949">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-949">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-onleaving"></a><span data-ttu-id="a34b8-950">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="a34b8-950">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="a34b8-951">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="a34b8-951">Parameters - OnLeaving</span></span>

<span data-ttu-id="a34b8-952">sender</span><span class="sxs-lookup"><span data-stu-id="a34b8-952">sender</span></span>  

<!-- -->

<span data-ttu-id="a34b8-953">e</span><span class="sxs-lookup"><span data-stu-id="a34b8-953">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="a34b8-954">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="a34b8-954">Method inputSearch</span></span>

<span data-ttu-id="a34b8-955">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-955">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="a34b8-956">パラメーター - inputSerach</span><span class="sxs-lookup"><span data-stu-id="a34b8-956">Parameters - inputSearch</span></span>

<span data-ttu-id="a34b8-957">searchStr</span><span class="sxs-lookup"><span data-stu-id="a34b8-957">searchStr</span></span>  
<span data-ttu-id="a34b8-958">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a34b8-958">The string value to use to filter data; optional.</span></span>

## <a name="method-dropex"></a><span data-ttu-id="a34b8-959">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="a34b8-959">Method dropEx</span></span>

<span data-ttu-id="a34b8-960">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-960">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="a34b8-961">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="a34b8-961">Parameters - dropEx</span></span>

<span data-ttu-id="a34b8-962">dragSource</span><span class="sxs-lookup"><span data-stu-id="a34b8-962">dragSource</span></span>  
<span data-ttu-id="a34b8-963">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-963">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-964">dragMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-964">dragMode</span></span>  
<span data-ttu-id="a34b8-965">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-965">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-966">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-966">x</span></span>  
<span data-ttu-id="a34b8-967">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-967">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-968">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-968">y</span></span>  
<span data-ttu-id="a34b8-969">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-969">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="a34b8-970">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="a34b8-970">Method lostFocus</span></span>

<span data-ttu-id="a34b8-971">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-971">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-setfocus"></a><span data-ttu-id="a34b8-972">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="a34b8-972">Method setFocus</span></span>

<span data-ttu-id="a34b8-973">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-973">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="a34b8-974">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="a34b8-974">Method prefColumnSize</span></span>

<span data-ttu-id="a34b8-975">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-975">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="a34b8-976">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="a34b8-976">Parameters - prefColumnSize</span></span>

<span data-ttu-id="a34b8-977">width</span><span class="sxs-lookup"><span data-stu-id="a34b8-977">width</span></span>  
<span data-ttu-id="a34b8-978">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="a34b8-978">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="a34b8-979">height</span><span class="sxs-lookup"><span data-stu-id="a34b8-979">height</span></span>  
<span data-ttu-id="a34b8-980">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="a34b8-980">The preferred height of the control.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="a34b8-981">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="a34b8-981">Method mouseEnter</span></span>

<span data-ttu-id="a34b8-982">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-982">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="a34b8-983">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="a34b8-983">Parameters - mouseEnter</span></span>

<span data-ttu-id="a34b8-984">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-984">x</span></span>  
<span data-ttu-id="a34b8-985">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-985">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-986">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-986">y</span></span>  
<span data-ttu-id="a34b8-987">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-987">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-988">ボタン</span><span class="sxs-lookup"><span data-stu-id="a34b8-988">button</span></span>  
<span data-ttu-id="a34b8-989">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-989">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-990">Ctrl</span><span class="sxs-lookup"><span data-stu-id="a34b8-990">Ctrl</span></span>  
<span data-ttu-id="a34b8-991">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-991">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="a34b8-992">シフト</span><span class="sxs-lookup"><span data-stu-id="a34b8-992">Shift</span></span>  
<span data-ttu-id="a34b8-993">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-993">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-paste"></a><span data-ttu-id="a34b8-994">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="a34b8-994">Method paste</span></span>

<span data-ttu-id="a34b8-995">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-995">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-drop"></a><span data-ttu-id="a34b8-996">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="a34b8-996">Method drop</span></span>

<span data-ttu-id="a34b8-997">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-997">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="a34b8-998">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="a34b8-998">Parameters - drop</span></span>

<span data-ttu-id="a34b8-999">dragSource</span><span class="sxs-lookup"><span data-stu-id="a34b8-999">dragSource</span></span>  
<span data-ttu-id="a34b8-1000">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1000">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-1001">dragMode</span><span class="sxs-lookup"><span data-stu-id="a34b8-1001">dragMode</span></span>  
<span data-ttu-id="a34b8-1002">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1002">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-1003">x</span><span class="sxs-lookup"><span data-stu-id="a34b8-1003">x</span></span>  
<span data-ttu-id="a34b8-1004">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1004">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="a34b8-1005">y</span><span class="sxs-lookup"><span data-stu-id="a34b8-1005">y</span></span>  
<span data-ttu-id="a34b8-1006">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1006">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onenter"></a><span data-ttu-id="a34b8-1007">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="a34b8-1007">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="a34b8-1008">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="a34b8-1008">Parameters - OnEnter</span></span>

<span data-ttu-id="a34b8-1009">sender</span><span class="sxs-lookup"><span data-stu-id="a34b8-1009">sender</span></span>  

<!-- -->

<span data-ttu-id="a34b8-1010">e</span><span class="sxs-lookup"><span data-stu-id="a34b8-1010">e</span></span>  

## <a name="method-enter"></a><span data-ttu-id="a34b8-1011">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="a34b8-1011">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-mouseleave"></a><span data-ttu-id="a34b8-1012">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="a34b8-1012">Method mouseLeave</span></span>

<span data-ttu-id="a34b8-1013">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1013">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-dragleave"></a><span data-ttu-id="a34b8-1014">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="a34b8-1014">Method dragLeave</span></span>

<span data-ttu-id="a34b8-1015">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1015">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="a34b8-1016">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="a34b8-1016">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="a34b8-1017">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="a34b8-1017">Parameters - OnLostFocus</span></span>

<span data-ttu-id="a34b8-1018">sender</span><span class="sxs-lookup"><span data-stu-id="a34b8-1018">sender</span></span>  

<!-- -->

<span data-ttu-id="a34b8-1019">e</span><span class="sxs-lookup"><span data-stu-id="a34b8-1019">e</span></span>  

## <a name="method-copy"></a><span data-ttu-id="a34b8-1020">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="a34b8-1020">Method copy</span></span>

<span data-ttu-id="a34b8-1021">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1021">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-context"></a><span data-ttu-id="a34b8-1022">メソッド context</span><span class="sxs-lookup"><span data-stu-id="a34b8-1022">Method context</span></span>

<span data-ttu-id="a34b8-1023">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1023">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enddrag"></a><span data-ttu-id="a34b8-1024">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="a34b8-1024">Method endDrag</span></span>

<span data-ttu-id="a34b8-1025">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1025">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="a34b8-1026">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="a34b8-1026">Remarks - endDrag</span></span>

<span data-ttu-id="a34b8-1027">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1027">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="a34b8-1028">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1028">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="a34b8-1029">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="a34b8-1029">Method resetUserSetting</span></span>

<span data-ttu-id="a34b8-1030">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1030">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-play"></a><span data-ttu-id="a34b8-1031">メソッド play</span><span class="sxs-lookup"><span data-stu-id="a34b8-1031">Method play</span></span>

```xpp
public void play([int firstFrame], [int lastFrame], [int loops])
```

### <a name="parameters---play"></a><span data-ttu-id="a34b8-1032">パラメーター - play</span><span class="sxs-lookup"><span data-stu-id="a34b8-1032">Parameters - play</span></span>

<span data-ttu-id="a34b8-1033">firstFrame</span><span class="sxs-lookup"><span data-stu-id="a34b8-1033">firstFrame</span></span>  

<!-- -->

<span data-ttu-id="a34b8-1034">lastFrame</span><span class="sxs-lookup"><span data-stu-id="a34b8-1034">lastFrame</span></span>  

<!-- -->

<span data-ttu-id="a34b8-1035">loops</span><span class="sxs-lookup"><span data-stu-id="a34b8-1035">loops</span></span>  

## <a name="method-ongotfocus"></a><span data-ttu-id="a34b8-1036">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="a34b8-1036">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="a34b8-1037">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="a34b8-1037">Parameters - OnGotFocus</span></span>

<span data-ttu-id="a34b8-1038">sender</span><span class="sxs-lookup"><span data-stu-id="a34b8-1038">sender</span></span>  

<!-- -->

<span data-ttu-id="a34b8-1039">e</span><span class="sxs-lookup"><span data-stu-id="a34b8-1039">e</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="a34b8-1040">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="a34b8-1040">Method displayControl</span></span>

<span data-ttu-id="a34b8-1041">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1041">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-gotfocus"></a><span data-ttu-id="a34b8-1042">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="a34b8-1042">Method gotFocus</span></span>

<span data-ttu-id="a34b8-1043">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1043">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-cut"></a><span data-ttu-id="a34b8-1044">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="a34b8-1044">Method cut</span></span>

<span data-ttu-id="a34b8-1045">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="a34b8-1045">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="a34b8-1046">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="a34b8-1046">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="a34b8-1047">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="a34b8-1047">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="a34b8-1048">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="a34b8-1048">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="a34b8-1049">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="a34b8-1049">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="a34b8-1050">overrideObject</span><span class="sxs-lookup"><span data-stu-id="a34b8-1050">overrideObject</span></span>  

## <a name="method-stop"></a><span data-ttu-id="a34b8-1051">メソッド stop</span><span class="sxs-lookup"><span data-stu-id="a34b8-1051">Method stop</span></span>

```xpp
public void stop()
```

