---
title: FormHTMLControl クラス
description: このトピックでは、FormHTMLControl クラスについて説明します。
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
ms.openlocfilehash: da1ef8e8341006a396475b8e0659ac2d6c02f352
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502935"
---
# <a name="class-formhtmlcontrol"></a><span data-ttu-id="b35fc-103">クラス FormHTMLControl</span><span class="sxs-lookup"><span data-stu-id="b35fc-103">Class FormHTMLControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormHTMLControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="b35fc-104">備考</span><span class="sxs-lookup"><span data-stu-id="b35fc-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b35fc-105">例</span><span class="sxs-lookup"><span data-stu-id="b35fc-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b35fc-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b35fc-106">Methods</span></span>

| <span data-ttu-id="b35fc-107">方法</span><span class="sxs-lookup"><span data-stu-id="b35fc-107">Method</span></span>                                                                                                      | <span data-ttu-id="b35fc-108">説明</span><span class="sxs-lookup"><span data-stu-id="b35fc-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35fc-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="b35fc-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="b35fc-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="b35fc-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="b35fc-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="b35fc-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="b35fc-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="b35fc-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="b35fc-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="b35fc-117">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="b35fc-117">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="b35fc-118">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-118">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="b35fc-119">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="b35fc-119">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="b35fc-120">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-120">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="b35fc-121">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-121">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="b35fc-122">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-122">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="b35fc-123">public str className(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-123">public str className(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="b35fc-125">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-125">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="b35fc-126">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="b35fc-126">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="b35fc-127">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-127">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="b35fc-128">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-128">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="b35fc-129">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-129">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="b35fc-130">public str custom(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-130">public str custom(\[str value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-131">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-131">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="b35fc-132">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-132">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="b35fc-133">public AnyType dispatch(VarArg )</span><span class="sxs-lookup"><span data-stu-id="b35fc-133">public AnyType dispatch(VarArg )</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-134">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-134">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="b35fc-135">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-135">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="b35fc-136">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-136">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="b35fc-137">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-137">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="b35fc-138">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="b35fc-138">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="b35fc-139">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-139">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="b35fc-140">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="b35fc-140">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="b35fc-141">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-141">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="b35fc-142">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="b35fc-142">public str dragText()</span></span>                                                                                       | <span data-ttu-id="b35fc-143">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-143">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="b35fc-144">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-144">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="b35fc-145">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-145">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="b35fc-146">public COMError error()</span><span class="sxs-lookup"><span data-stu-id="b35fc-146">public COMError error()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-147">public str getText()</span><span class="sxs-lookup"><span data-stu-id="b35fc-147">public str getText()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-148">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-148">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="b35fc-149">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-149">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="b35fc-150">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="b35fc-150">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="b35fc-151">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-151">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="b35fc-152">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-152">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="b35fc-153">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-153">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="b35fc-154">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-154">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="b35fc-155">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-155">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="b35fc-156">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-156">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="b35fc-157">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-157">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="b35fc-158">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="b35fc-158">public str helpField()</span></span>                                                                                      | <span data-ttu-id="b35fc-159">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-159">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="b35fc-160">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-160">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="b35fc-161">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-161">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="b35fc-162">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-162">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="b35fc-163">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-163">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="b35fc-164">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="b35fc-164">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="b35fc-165">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-165">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="b35fc-166">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="b35fc-166">public ComInterface interface()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-167">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="b35fc-167">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-168">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="b35fc-168">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="b35fc-169">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-169">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="b35fc-170">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="b35fc-170">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="b35fc-171">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-171">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="b35fc-172">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="b35fc-172">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="b35fc-173">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-173">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="b35fc-174">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="b35fc-174">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-175">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-175">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="b35fc-176">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-176">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="b35fc-177">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-177">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="b35fc-178">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-178">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="b35fc-179">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-179">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="b35fc-180">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-180">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="b35fc-181">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-181">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="b35fc-182">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="b35fc-182">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="b35fc-183">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="b35fc-183">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="b35fc-184">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-184">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="b35fc-185">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="b35fc-185">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="b35fc-186">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-186">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="b35fc-187">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="b35fc-187">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="b35fc-188">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-188">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="b35fc-189">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="b35fc-189">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="b35fc-190">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-190">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="b35fc-191">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-191">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="b35fc-192">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-192">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="b35fc-193">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-193">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-194">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="b35fc-194">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-195">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="b35fc-195">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="b35fc-196">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-196">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="b35fc-197">public str processPicture(str picture)</span><span class="sxs-lookup"><span data-stu-id="b35fc-197">public str processPicture(str picture)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-198">public boolean rTLCapable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-198">public boolean rTLCapable(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-199">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-199">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="b35fc-200">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-200">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="b35fc-201">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="b35fc-201">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="b35fc-202">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-202">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="b35fc-203">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-203">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="b35fc-204">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-204">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="b35fc-205">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="b35fc-205">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="b35fc-206">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-206">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="b35fc-207">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-207">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="b35fc-208">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-208">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="b35fc-209">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-209">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="b35fc-210">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-210">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="b35fc-211">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-211">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="b35fc-212">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-212">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="b35fc-213">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-213">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-214">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="b35fc-214">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-215">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-215">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="b35fc-216">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-216">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="b35fc-217">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-217">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="b35fc-218">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-218">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="b35fc-219">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-219">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="b35fc-220">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-220">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="b35fc-221">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-221">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="b35fc-222">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-222">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="b35fc-223">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-223">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="b35fc-224">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-224">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="b35fc-225">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-225">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="b35fc-226">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-226">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="b35fc-227">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-227">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="b35fc-228">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-228">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="b35fc-229">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-229">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="b35fc-230">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-230">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="b35fc-231">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-231">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="b35fc-232">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-232">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="b35fc-233">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-233">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="b35fc-234">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-234">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="b35fc-235">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-235">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="b35fc-236">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-236">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="b35fc-237">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-237">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="b35fc-238">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-238">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="b35fc-239">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-239">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="b35fc-240">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-240">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="b35fc-241">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-241">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="b35fc-242">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-242">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="b35fc-243">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-243">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="b35fc-244">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-244">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="b35fc-245">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-245">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="b35fc-246">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-246">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="b35fc-247">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-247">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="b35fc-248">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-248">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="b35fc-249">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-249">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="b35fc-250">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-250">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="b35fc-251">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-251">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="b35fc-252">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-252">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="b35fc-253">public void copy()</span><span class="sxs-lookup"><span data-stu-id="b35fc-253">public void copy()</span></span>                                                                                          | <span data-ttu-id="b35fc-254">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b35fc-254">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="b35fc-255">public void insertText(str Text, \[NoYes repaint\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-255">public void insertText(str Text, \[NoYes repaint\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-256">public void cut()</span><span class="sxs-lookup"><span data-stu-id="b35fc-256">public void cut()</span></span>                                                                                           | <span data-ttu-id="b35fc-257">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="b35fc-257">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="b35fc-258">public void processBase(str base)</span><span class="sxs-lookup"><span data-stu-id="b35fc-258">public void processBase(str base)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-259">public void setFont(int fontid, HtmlFont htmlFont, \[NoYes repaint\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-259">public void setFont(int fontid, HtmlFont htmlFont, \[NoYes repaint\])</span></span>                                       |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-260">public void getFont(int fontid, HtmlFont htmlFont)</span><span class="sxs-lookup"><span data-stu-id="b35fc-260">public void getFont(int fontid, HtmlFont htmlFont)</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-261">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="b35fc-261">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="b35fc-262">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-262">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="b35fc-263">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-263">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-264">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="b35fc-264">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="b35fc-265">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-265">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="b35fc-266">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="b35fc-266">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="b35fc-267">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-267">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="b35fc-268">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="b35fc-268">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="b35fc-269">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-269">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="b35fc-270">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="b35fc-270">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="b35fc-271">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-271">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="b35fc-272">public void updateSize()</span><span class="sxs-lookup"><span data-stu-id="b35fc-272">public void updateSize()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-273">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="b35fc-273">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="b35fc-274">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-274">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="b35fc-275">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-275">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-276">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="b35fc-276">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="b35fc-277">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-277">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="b35fc-278">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="b35fc-278">public void displayControl()</span></span>                                                                                | <span data-ttu-id="b35fc-279">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-279">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="b35fc-280">public void processLink(str link)</span><span class="sxs-lookup"><span data-stu-id="b35fc-280">public void processLink(str link)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-281">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="b35fc-281">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="b35fc-282">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-282">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="b35fc-283">public void processTitle(str title)</span><span class="sxs-lookup"><span data-stu-id="b35fc-283">public void processTitle(str title)</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-284">public void read(str FileName, \[str TagName\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-284">public void read(str FileName, \[str TagName\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-285">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="b35fc-285">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="b35fc-286">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-286">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="b35fc-287">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-287">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-288">public void setText(str Text, \[str TagName\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-288">public void setText(str Text, \[str TagName\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-289">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-289">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-290">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="b35fc-290">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="b35fc-291">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="b35fc-291">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="b35fc-292">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-292">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-293">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="b35fc-293">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="b35fc-294">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-294">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="b35fc-295">public void save(str FileName)</span><span class="sxs-lookup"><span data-stu-id="b35fc-295">public void save(str FileName)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-296">public void command(int command)</span><span class="sxs-lookup"><span data-stu-id="b35fc-296">public void command(int command)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-297">public void paste()</span><span class="sxs-lookup"><span data-stu-id="b35fc-297">public void paste()</span></span>                                                                                         | <span data-ttu-id="b35fc-298">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-298">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="b35fc-299">public void insertLink(str Text, str Url, str Name, \[NoYes repaint\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-299">public void insertLink(str Text, str Url, str Name, \[NoYes repaint\])</span></span>                                      |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-300">public void context()</span><span class="sxs-lookup"><span data-stu-id="b35fc-300">public void context()</span></span>                                                                                       | <span data-ttu-id="b35fc-301">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-301">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="b35fc-302">public void enter()</span><span class="sxs-lookup"><span data-stu-id="b35fc-302">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-303">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="b35fc-303">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="b35fc-304">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-304">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="b35fc-305">public void clearWindow()</span><span class="sxs-lookup"><span data-stu-id="b35fc-305">public void clearWindow()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-306">public void processForm(int formHandle)</span><span class="sxs-lookup"><span data-stu-id="b35fc-306">public void processForm(int formHandle)</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="b35fc-307">public void setMargin(int Left, int Right, int Top, int Bottom, \[NoYes repaint\])</span><span class="sxs-lookup"><span data-stu-id="b35fc-307">public void setMargin(int Left, int Right, int Top, int Bottom, \[NoYes repaint\])</span></span>                          |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="b35fc-308">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="b35fc-308">Method alignControl</span></span>

<span data-ttu-id="b35fc-309">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-309">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="b35fc-310">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="b35fc-310">Parameters - alignControl</span></span>

<span data-ttu-id="b35fc-311">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-311">value</span></span>  
<span data-ttu-id="b35fc-312">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-312">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="b35fc-313">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="b35fc-313">Return Value - alignControl</span></span>

<span data-ttu-id="b35fc-314">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-314">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="b35fc-315">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="b35fc-315">Remarks - alignControl</span></span>

<span data-ttu-id="b35fc-316">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-316">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="b35fc-317">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="b35fc-317">Method allowEdit</span></span>

<span data-ttu-id="b35fc-318">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-318">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="b35fc-319">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b35fc-319">Parameters - allowEdit</span></span>

<span data-ttu-id="b35fc-320">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-320">value</span></span>  
<span data-ttu-id="b35fc-321">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-321">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="b35fc-322">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b35fc-322">Return Value - allowEdit</span></span>

<span data-ttu-id="b35fc-323">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-323">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="b35fc-324">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b35fc-324">Remarks - allowEdit</span></span>

<span data-ttu-id="b35fc-325">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-325">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="b35fc-326">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="b35fc-326">Method allowSysSetup</span></span>

<span data-ttu-id="b35fc-327">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-327">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="b35fc-328">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="b35fc-328">Return Value - allowSysSetup</span></span>

<span data-ttu-id="b35fc-329">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-329">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="b35fc-330">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b35fc-330">Method autoDeclaration</span></span>

<span data-ttu-id="b35fc-331">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-331">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="b35fc-332">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b35fc-332">Parameters - autoDeclaration</span></span>

<span data-ttu-id="b35fc-333">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-333">value</span></span>  
<span data-ttu-id="b35fc-334">指定されている場合、プロパティはこの値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-334">If supplied, the property is set to this value.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="b35fc-335">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b35fc-335">Return Value - autoDeclaration</span></span>

<span data-ttu-id="b35fc-336">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-336">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="b35fc-337">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b35fc-337">Remarks - autoDeclaration</span></span>

<span data-ttu-id="b35fc-338">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-338">Controls cannot have identical names.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="b35fc-339">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="b35fc-339">Method beginDrag</span></span>

<span data-ttu-id="b35fc-340">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-340">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="b35fc-341">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="b35fc-341">Parameters - beginDrag</span></span>

<span data-ttu-id="b35fc-342">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-342">x</span></span>  
<span data-ttu-id="b35fc-343">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-343">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="b35fc-344">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="b35fc-344">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="b35fc-345">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-345">y</span></span>  
<span data-ttu-id="b35fc-346">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-346">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="b35fc-347">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="b35fc-347">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="b35fc-348">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="b35fc-348">Return Value - beginDrag</span></span>

<span data-ttu-id="b35fc-349">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-349">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="b35fc-350">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="b35fc-350">Remarks - beginDrag</span></span>

<span data-ttu-id="b35fc-351">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-351">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="b35fc-352">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-352">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="b35fc-353">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="b35fc-353">Method calcControlSize</span></span>

<span data-ttu-id="b35fc-354">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-354">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="b35fc-355">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="b35fc-355">Parameters - calcControlSize</span></span>

<span data-ttu-id="b35fc-356">chars</span><span class="sxs-lookup"><span data-stu-id="b35fc-356">chars</span></span>  
<span data-ttu-id="b35fc-357">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="b35fc-357">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="b35fc-358">明細行</span><span class="sxs-lookup"><span data-stu-id="b35fc-358">lines</span></span>  
<span data-ttu-id="b35fc-359">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="b35fc-359">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="b35fc-360">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="b35fc-360">Return Value - calcControlSize</span></span>

<span data-ttu-id="b35fc-361">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="b35fc-361">The container that holds the width and height.</span></span>

## <a name="method-caption"></a><span data-ttu-id="b35fc-362">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="b35fc-362">Method caption</span></span>

<span data-ttu-id="b35fc-363">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-363">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="b35fc-364">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="b35fc-364">Parameters - caption</span></span>

<span data-ttu-id="b35fc-365">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-365">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="b35fc-366">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="b35fc-366">Return Value - caption</span></span>

<span data-ttu-id="b35fc-367">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="b35fc-367">The string that is used as the caption of the control.</span></span>

## <a name="method-classname"></a><span data-ttu-id="b35fc-368">メソッド className</span><span class="sxs-lookup"><span data-stu-id="b35fc-368">Method className</span></span>

```xpp
public str className([str value])
```

### <a name="parameters---classname"></a><span data-ttu-id="b35fc-369">パラメーター - className</span><span class="sxs-lookup"><span data-stu-id="b35fc-369">Parameters - className</span></span>

<span data-ttu-id="b35fc-370">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-370">value</span></span>  

### <a name="return-value---classname"></a><span data-ttu-id="b35fc-371">戻り値 - className</span><span class="sxs-lookup"><span data-stu-id="b35fc-371">Return Value - className</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="b35fc-372">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="b35fc-372">Method configurationKey</span></span>

<span data-ttu-id="b35fc-373">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-373">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="b35fc-374">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b35fc-374">Parameters - configurationKey</span></span>

<span data-ttu-id="b35fc-375">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-375">value</span></span>  
<span data-ttu-id="b35fc-376">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-376">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="b35fc-377">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b35fc-377">Return Value - configurationKey</span></span>

<span data-ttu-id="b35fc-378">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="b35fc-378">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="b35fc-379">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b35fc-379">Remarks - configurationKey</span></span>

<span data-ttu-id="b35fc-380">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-380">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="b35fc-381">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-381">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="b35fc-382">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="b35fc-382">Method configurationKeyEx</span></span>

<span data-ttu-id="b35fc-383">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-383">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="b35fc-384">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="b35fc-384">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="b35fc-385">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="b35fc-385">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="b35fc-386">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="b35fc-386">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="b35fc-387">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-387">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="b35fc-388">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-388">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="b35fc-389">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-389">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="b35fc-390">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b35fc-390">Method countryRegionCodes</span></span>

<span data-ttu-id="b35fc-391">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-391">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="b35fc-392">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b35fc-392">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="b35fc-393">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-393">value</span></span>  
<span data-ttu-id="b35fc-394">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-394">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="b35fc-395">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b35fc-395">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="b35fc-396">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="b35fc-396">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-custom"></a><span data-ttu-id="b35fc-397">メソッド custom</span><span class="sxs-lookup"><span data-stu-id="b35fc-397">Method custom</span></span>

```xpp
public str custom([str value])
```

### <a name="parameters---custom"></a><span data-ttu-id="b35fc-398">パラメーター - custom</span><span class="sxs-lookup"><span data-stu-id="b35fc-398">Parameters - custom</span></span>

<span data-ttu-id="b35fc-399">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-399">value</span></span>  

### <a name="return-value---custom"></a><span data-ttu-id="b35fc-400">戻り値 - custom</span><span class="sxs-lookup"><span data-stu-id="b35fc-400">Return Value - custom</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="b35fc-401">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b35fc-401">Method dataRelationPath</span></span>

<span data-ttu-id="b35fc-402">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-402">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="b35fc-403">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b35fc-403">Parameters - dataRelationPath</span></span>

<span data-ttu-id="b35fc-404">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-404">value</span></span>  
<span data-ttu-id="b35fc-405">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-405">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="b35fc-406">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b35fc-406">Return Value - dataRelationPath</span></span>

<span data-ttu-id="b35fc-407">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="b35fc-407">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="b35fc-408">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b35fc-408">Remarks - dataRelationPath</span></span>

<span data-ttu-id="b35fc-409">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-409">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="b35fc-410">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="b35fc-410">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-dispatch"></a><span data-ttu-id="b35fc-411">メソッド dispatch</span><span class="sxs-lookup"><span data-stu-id="b35fc-411">Method dispatch</span></span>

```xpp
public AnyType dispatch(VarArg )
```

### <a name="parameters---dispatch"></a><span data-ttu-id="b35fc-412">パラメーター - dispatch</span><span class="sxs-lookup"><span data-stu-id="b35fc-412">Parameters - dispatch</span></span>


### <a name="return-value---dispatch"></a><span data-ttu-id="b35fc-413">戻り値 - dispatch</span><span class="sxs-lookup"><span data-stu-id="b35fc-413">Return Value - dispatch</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="b35fc-414">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="b35fc-414">Method displayTarget</span></span>

<span data-ttu-id="b35fc-415">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-415">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="b35fc-416">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="b35fc-416">Parameters - displayTarget</span></span>

<span data-ttu-id="b35fc-417">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-417">value</span></span>  
<span data-ttu-id="b35fc-418">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-418">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="b35fc-419">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="b35fc-419">Return Value - displayTarget</span></span>

<span data-ttu-id="b35fc-420">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-420">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="b35fc-421">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="b35fc-421">Method dragDrop</span></span>

<span data-ttu-id="b35fc-422">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-422">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="b35fc-423">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b35fc-423">Parameters - dragDrop</span></span>

<span data-ttu-id="b35fc-424">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-424">value</span></span>  
<span data-ttu-id="b35fc-425">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-425">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="b35fc-426">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b35fc-426">Return Value - dragDrop</span></span>

<span data-ttu-id="b35fc-427">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-427">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="b35fc-428">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b35fc-428">Remarks - dragDrop</span></span>

<span data-ttu-id="b35fc-429">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-429">Use the dragLeave, the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="b35fc-430">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="b35fc-430">Method dragOver</span></span>

<span data-ttu-id="b35fc-431">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-431">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="b35fc-432">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="b35fc-432">Parameters - dragOver</span></span>

<span data-ttu-id="b35fc-433">dragSource</span><span class="sxs-lookup"><span data-stu-id="b35fc-433">dragSource</span></span>  
<span data-ttu-id="b35fc-434">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-434">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-435">dragMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-435">dragMode</span></span>  
<span data-ttu-id="b35fc-436">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-436">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-437">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-437">x</span></span>  
<span data-ttu-id="b35fc-438">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-438">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-439">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-439">y</span></span>  
<span data-ttu-id="b35fc-440">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-440">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="b35fc-441">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="b35fc-441">Return Value - dragOver</span></span>

<span data-ttu-id="b35fc-442">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-442">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="b35fc-443">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="b35fc-443">Method dragOverEx</span></span>

<span data-ttu-id="b35fc-444">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-444">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="b35fc-445">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="b35fc-445">Parameters - dragOverEx</span></span>

<span data-ttu-id="b35fc-446">dragSource</span><span class="sxs-lookup"><span data-stu-id="b35fc-446">dragSource</span></span>  
<span data-ttu-id="b35fc-447">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-447">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-448">dragMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-448">dragMode</span></span>  
<span data-ttu-id="b35fc-449">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-449">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-450">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-450">x</span></span>  
<span data-ttu-id="b35fc-451">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-451">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-452">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-452">y</span></span>  
<span data-ttu-id="b35fc-453">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-453">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="b35fc-454">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="b35fc-454">Return Value - dragOverEx</span></span>

<span data-ttu-id="b35fc-455">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-455">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="b35fc-456">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="b35fc-456">Method dragText</span></span>

<span data-ttu-id="b35fc-457">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-457">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="b35fc-458">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="b35fc-458">Return Value - dragText</span></span>

<span data-ttu-id="b35fc-459">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="b35fc-459">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="b35fc-460">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="b35fc-460">Method enabled</span></span>

<span data-ttu-id="b35fc-461">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-461">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="b35fc-462">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="b35fc-462">Parameters - enabled</span></span>

<span data-ttu-id="b35fc-463">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-463">value</span></span>  
<span data-ttu-id="b35fc-464">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-464">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="b35fc-465">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="b35fc-465">Return Value - enabled</span></span>

<span data-ttu-id="b35fc-466">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-466">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="b35fc-467">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="b35fc-467">Remarks - enabled</span></span>

<span data-ttu-id="b35fc-468">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-468">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="b35fc-469">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-469">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="b35fc-470">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-470">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-error"></a><span data-ttu-id="b35fc-471">メソッド error</span><span class="sxs-lookup"><span data-stu-id="b35fc-471">Method error</span></span>

```xpp
public COMError error()
```

### <a name="return-value---error"></a><span data-ttu-id="b35fc-472">戻り値 - error</span><span class="sxs-lookup"><span data-stu-id="b35fc-472">Return Value - error</span></span>

## <a name="method-gettext"></a><span data-ttu-id="b35fc-473">メソッド getText</span><span class="sxs-lookup"><span data-stu-id="b35fc-473">Method getText</span></span>

```xpp
public str getText()
```

### <a name="return-value---gettext"></a><span data-ttu-id="b35fc-474">戻り値 - getText</span><span class="sxs-lookup"><span data-stu-id="b35fc-474">Return Value - getText</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="b35fc-475">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="b35fc-475">Method hasChanged</span></span>

<span data-ttu-id="b35fc-476">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-476">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="b35fc-477">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="b35fc-477">Parameters - hasChanged</span></span>

<span data-ttu-id="b35fc-478">val</span><span class="sxs-lookup"><span data-stu-id="b35fc-478">val</span></span>  
<span data-ttu-id="b35fc-479">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-479">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="b35fc-480">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="b35fc-480">Return Value - hasChanged</span></span>

<span data-ttu-id="b35fc-481">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-481">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="b35fc-482">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="b35fc-482">Method hasUserSetting</span></span>

<span data-ttu-id="b35fc-483">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-483">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="b35fc-484">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="b35fc-484">Return Value - hasUserSetting</span></span>

<span data-ttu-id="b35fc-485">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-485">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="b35fc-486">メソッド height</span><span class="sxs-lookup"><span data-stu-id="b35fc-486">Method height</span></span>

<span data-ttu-id="b35fc-487">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-487">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="b35fc-488">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="b35fc-488">Parameters - height</span></span>

<span data-ttu-id="b35fc-489">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-489">value</span></span>  
<span data-ttu-id="b35fc-490">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-490">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="b35fc-491">モード</span><span class="sxs-lookup"><span data-stu-id="b35fc-491">mode</span></span>  
<span data-ttu-id="b35fc-492">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-492">An integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="b35fc-493">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="b35fc-493">Return Value - height</span></span>

<span data-ttu-id="b35fc-494">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="b35fc-494">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="b35fc-495">備考 - height</span><span class="sxs-lookup"><span data-stu-id="b35fc-495">Remarks - height</span></span>

<span data-ttu-id="b35fc-496">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-496">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b35fc-497">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b35fc-497">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b35fc-498">モード。</span><span class="sxs-lookup"><span data-stu-id="b35fc-498">Mode.</span></span>            | <span data-ttu-id="b35fc-499">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b35fc-499">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35fc-500">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b35fc-500">-1 Exact.</span></span>        | <span data-ttu-id="b35fc-501">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-501">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b35fc-502">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b35fc-502">0 Auto.</span></span>          | <span data-ttu-id="b35fc-503">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-503">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b35fc-504">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="b35fc-504">1 Column height.</span></span> | <span data-ttu-id="b35fc-505">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-505">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b35fc-506">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-506">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="b35fc-507">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-507">Method heightMode</span></span>

<span data-ttu-id="b35fc-508">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-508">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="b35fc-509">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-509">Parameters - heightMode</span></span>

<span data-ttu-id="b35fc-510">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-510">value</span></span>  
<span data-ttu-id="b35fc-511">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-511">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="b35fc-512">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-512">Return Value - heightMode</span></span>

<span data-ttu-id="b35fc-513">計算モード。</span><span class="sxs-lookup"><span data-stu-id="b35fc-513">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="b35fc-514">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-514">Remarks - heightMode</span></span>

<span data-ttu-id="b35fc-515">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b35fc-515">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b35fc-516">モード。</span><span class="sxs-lookup"><span data-stu-id="b35fc-516">Mode.</span></span>          | <span data-ttu-id="b35fc-517">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b35fc-517">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35fc-518">正確。</span><span class="sxs-lookup"><span data-stu-id="b35fc-518">Exact.</span></span>         | <span data-ttu-id="b35fc-519">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-519">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b35fc-520">自動。</span><span class="sxs-lookup"><span data-stu-id="b35fc-520">Auto.</span></span>          | <span data-ttu-id="b35fc-521">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-521">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b35fc-522">列の高さ</span><span class="sxs-lookup"><span data-stu-id="b35fc-522">Column height.</span></span> | <span data-ttu-id="b35fc-523">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-523">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b35fc-524">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-524">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="b35fc-525">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-525">Method heightValue</span></span>

<span data-ttu-id="b35fc-526">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-526">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="b35fc-527">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-527">Parameters - heightValue</span></span>

<span data-ttu-id="b35fc-528">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-528">value</span></span>  
<span data-ttu-id="b35fc-529">高さをピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-529">An integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="b35fc-530">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-530">Return Value - heightValue</span></span>

<span data-ttu-id="b35fc-531">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="b35fc-531">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="b35fc-532">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-532">Remarks - heightValue</span></span>

<span data-ttu-id="b35fc-533">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-533">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="b35fc-534">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="b35fc-534">Method helpField</span></span>

<span data-ttu-id="b35fc-535">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-535">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="b35fc-536">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="b35fc-536">Return Value - helpField</span></span>

<span data-ttu-id="b35fc-537">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="b35fc-537">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="b35fc-538">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="b35fc-538">Remarks - helpField</span></span>

<span data-ttu-id="b35fc-539">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-539">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="b35fc-540">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-540">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="b35fc-541">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="b35fc-541">Method helpText</span></span>

<span data-ttu-id="b35fc-542">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-542">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="b35fc-543">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="b35fc-543">Parameters - helpText</span></span>

<span data-ttu-id="b35fc-544">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-544">value</span></span>  
<span data-ttu-id="b35fc-545">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-545">The value to assign as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="b35fc-546">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="b35fc-546">Return Value - helpText</span></span>

<span data-ttu-id="b35fc-547">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="b35fc-547">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="b35fc-548">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="b35fc-548">Remarks - helpText</span></span>

<span data-ttu-id="b35fc-549">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-549">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="b35fc-550">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-550">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="b35fc-551">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b35fc-551">Method hierarchyParent</span></span>

<span data-ttu-id="b35fc-552">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-552">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="b35fc-553">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b35fc-553">Parameters - hierarchyParent</span></span>

<span data-ttu-id="b35fc-554">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-554">value</span></span>  
<span data-ttu-id="b35fc-555">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-555">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="b35fc-556">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b35fc-556">Return Value - hierarchyParent</span></span>

<span data-ttu-id="b35fc-557">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-557">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="b35fc-558">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="b35fc-558">Method hWnd</span></span>

<span data-ttu-id="b35fc-559">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-559">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="b35fc-560">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="b35fc-560">Return Value - hWnd</span></span>

<span data-ttu-id="b35fc-561">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="b35fc-561">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="b35fc-562">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="b35fc-562">Remarks - hWnd</span></span>

<span data-ttu-id="b35fc-563">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-563">The handle can be used with the Windows API.</span></span>

## <a name="method-interface"></a><span data-ttu-id="b35fc-564">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="b35fc-564">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="b35fc-565">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="b35fc-565">Return Value - interface</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="b35fc-566">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="b35fc-566">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="b35fc-567">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="b35fc-567">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="b35fc-568">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="b35fc-568">Method isDisplayed</span></span>

<span data-ttu-id="b35fc-569">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-569">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="b35fc-570">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="b35fc-570">Return Value - isDisplayed</span></span>

<span data-ttu-id="b35fc-571">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-571">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="b35fc-572">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="b35fc-572">Remarks - isDisplayed</span></span>

<span data-ttu-id="b35fc-573">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-573">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="b35fc-574">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="b35fc-574">Method isRestricted</span></span>

<span data-ttu-id="b35fc-575">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-575">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="b35fc-576">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="b35fc-576">Return Value - isRestricted</span></span>

<span data-ttu-id="b35fc-577">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-577">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="b35fc-578">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="b35fc-578">Method isUserSetupEnabled</span></span>

<span data-ttu-id="b35fc-579">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-579">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="b35fc-580">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="b35fc-580">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="b35fc-581">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="b35fc-581">neededSetupRights</span></span>  
<span data-ttu-id="b35fc-582">コントロールに要求されているカスタマイズのレベルを指定する FormAllowUserSetup 列挙値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-582">A FormAllowUserSetup enumeration value that specifies the level of customization that is being requested for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="b35fc-583">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="b35fc-583">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="b35fc-584">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-584">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="b35fc-585">「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメータで指定されたレベル以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-585">For this method to return true, the AllowUserSetup property for the design and all parent containers must be at least as high as the level that is specified by the neededSetupRights parameter.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="b35fc-586">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="b35fc-586">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="b35fc-587">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-587">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35fc-588">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="b35fc-588">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="b35fc-589">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-589">No changes can be made to the control.</span></span> <span data-ttu-id="b35fc-590">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-590">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="b35fc-591">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="b35fc-591">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="b35fc-592">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-592">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="b35fc-593">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-593">The user cannot move the control.</span></span>   |
| <span data-ttu-id="b35fc-594">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="b35fc-594">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="b35fc-595">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-595">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="b35fc-596">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-596">The user can also move the control.</span></span> |

## <a name="method-leave"></a><span data-ttu-id="b35fc-597">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="b35fc-597">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="b35fc-598">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="b35fc-598">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="b35fc-599">メソッド left</span><span class="sxs-lookup"><span data-stu-id="b35fc-599">Method left</span></span>

<span data-ttu-id="b35fc-600">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-600">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="b35fc-601">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="b35fc-601">Parameters - left</span></span>

<span data-ttu-id="b35fc-602">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-602">value</span></span>  
<span data-ttu-id="b35fc-603">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-603">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="b35fc-604">モード</span><span class="sxs-lookup"><span data-stu-id="b35fc-604">mode</span></span>  
<span data-ttu-id="b35fc-605">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-605">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="b35fc-606">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="b35fc-606">Return Value - left</span></span>

<span data-ttu-id="b35fc-607">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="b35fc-607">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="b35fc-608">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-608">Method leftMode</span></span>

<span data-ttu-id="b35fc-609">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-609">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="b35fc-610">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-610">Parameters - leftMode</span></span>

<span data-ttu-id="b35fc-611">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-611">value</span></span>  
<span data-ttu-id="b35fc-612">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-612">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="b35fc-613">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-613">Return Value - leftMode</span></span>

<span data-ttu-id="b35fc-614">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="b35fc-614">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="b35fc-615">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-615">Method leftValue</span></span>

<span data-ttu-id="b35fc-616">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-616">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="b35fc-617">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-617">Parameters - leftValue</span></span>

<span data-ttu-id="b35fc-618">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-618">value</span></span>  
<span data-ttu-id="b35fc-619">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-619">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="b35fc-620">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-620">Return Value - leftValue</span></span>

<span data-ttu-id="b35fc-621">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="b35fc-621">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="b35fc-622">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="b35fc-622">Method markAsUserAdd</span></span>

<span data-ttu-id="b35fc-623">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="b35fc-623">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="b35fc-624">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="b35fc-624">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="b35fc-625">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-625">value</span></span>  
<span data-ttu-id="b35fc-626">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-626">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="b35fc-627">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="b35fc-627">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="b35fc-628">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-628">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="b35fc-629">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="b35fc-629">Method mouseDblClick</span></span>

<span data-ttu-id="b35fc-630">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-630">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="b35fc-631">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="b35fc-631">Parameters - mouseDblClick</span></span>

<span data-ttu-id="b35fc-632">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-632">x</span></span>  
<span data-ttu-id="b35fc-633">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-633">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-634">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-634">y</span></span>  
<span data-ttu-id="b35fc-635">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-635">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-636">ボタン</span><span class="sxs-lookup"><span data-stu-id="b35fc-636">button</span></span>  
<span data-ttu-id="b35fc-637">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-637">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-638">Ctrl</span><span class="sxs-lookup"><span data-stu-id="b35fc-638">Ctrl</span></span>  
<span data-ttu-id="b35fc-639">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-639">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-640">シフト</span><span class="sxs-lookup"><span data-stu-id="b35fc-640">Shift</span></span>  
<span data-ttu-id="b35fc-641">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-641">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="b35fc-642">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="b35fc-642">Return Value - mouseDblClick</span></span>

<span data-ttu-id="b35fc-643">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-643">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="b35fc-644">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="b35fc-644">Remarks - mouseDblClick</span></span>

<span data-ttu-id="b35fc-645">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-645">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="b35fc-646">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="b35fc-646">Method mouseDown</span></span>

<span data-ttu-id="b35fc-647">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-647">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="b35fc-648">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="b35fc-648">Parameters - mouseDown</span></span>

<span data-ttu-id="b35fc-649">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-649">x</span></span>  
<span data-ttu-id="b35fc-650">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-650">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-651">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-651">y</span></span>  
<span data-ttu-id="b35fc-652">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-652">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-653">ボタン</span><span class="sxs-lookup"><span data-stu-id="b35fc-653">button</span></span>  
<span data-ttu-id="b35fc-654">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-654">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-655">Ctrl</span><span class="sxs-lookup"><span data-stu-id="b35fc-655">Ctrl</span></span>  
<span data-ttu-id="b35fc-656">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-656">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-657">シフト</span><span class="sxs-lookup"><span data-stu-id="b35fc-657">Shift</span></span>  
<span data-ttu-id="b35fc-658">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-658">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="b35fc-659">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="b35fc-659">Return Value - mouseDown</span></span>

<span data-ttu-id="b35fc-660">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-660">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="b35fc-661">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="b35fc-661">Remarks - mouseDown</span></span>

<span data-ttu-id="b35fc-662">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-662">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="b35fc-663">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-663">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="b35fc-664">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="b35fc-664">Method mouseMove</span></span>

<span data-ttu-id="b35fc-665">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-665">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="b35fc-666">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="b35fc-666">Parameters - mouseMove</span></span>

<span data-ttu-id="b35fc-667">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-667">x</span></span>  
<span data-ttu-id="b35fc-668">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-668">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-669">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-669">y</span></span>  
<span data-ttu-id="b35fc-670">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-670">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-671">ボタン</span><span class="sxs-lookup"><span data-stu-id="b35fc-671">button</span></span>  
<span data-ttu-id="b35fc-672">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-672">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-673">Ctrl</span><span class="sxs-lookup"><span data-stu-id="b35fc-673">Ctrl</span></span>  
<span data-ttu-id="b35fc-674">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-674">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-675">シフト</span><span class="sxs-lookup"><span data-stu-id="b35fc-675">Shift</span></span>  
<span data-ttu-id="b35fc-676">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-676">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="b35fc-677">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="b35fc-677">Return Value - mouseMove</span></span>

<span data-ttu-id="b35fc-678">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-678">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="b35fc-679">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="b35fc-679">Remarks - mouseMove</span></span>

<span data-ttu-id="b35fc-680">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-680">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="b35fc-681">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="b35fc-681">Method mouseUp</span></span>

<span data-ttu-id="b35fc-682">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-682">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="b35fc-683">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="b35fc-683">Parameters - mouseUp</span></span>

<span data-ttu-id="b35fc-684">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-684">x</span></span>  
<span data-ttu-id="b35fc-685">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-685">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-686">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-686">y</span></span>  
<span data-ttu-id="b35fc-687">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-687">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-688">ボタン</span><span class="sxs-lookup"><span data-stu-id="b35fc-688">button</span></span>  
<span data-ttu-id="b35fc-689">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-689">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-690">Ctrl</span><span class="sxs-lookup"><span data-stu-id="b35fc-690">Ctrl</span></span>  
<span data-ttu-id="b35fc-691">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-691">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-692">シフト</span><span class="sxs-lookup"><span data-stu-id="b35fc-692">Shift</span></span>  
<span data-ttu-id="b35fc-693">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-693">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="b35fc-694">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="b35fc-694">Return Value - mouseUp</span></span>

<span data-ttu-id="b35fc-695">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-695">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="b35fc-696">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="b35fc-696">Remarks - mouseUp</span></span>

<span data-ttu-id="b35fc-697">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-697">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="b35fc-698">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-698">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="b35fc-699">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b35fc-699">Method name</span></span>

<span data-ttu-id="b35fc-700">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-700">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="b35fc-701">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="b35fc-701">Parameters - name</span></span>

<span data-ttu-id="b35fc-702">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-702">value</span></span>  
<span data-ttu-id="b35fc-703">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-703">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="b35fc-704">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b35fc-704">Return Value - name</span></span>

<span data-ttu-id="b35fc-705">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="b35fc-705">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="b35fc-706">備考 - name</span><span class="sxs-lookup"><span data-stu-id="b35fc-706">Remarks - name</span></span>

<span data-ttu-id="b35fc-707">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-707">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="b35fc-708">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-708">It must start with a letter.</span></span>
-   <span data-ttu-id="b35fc-709">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-709">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="b35fc-710">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-710">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="b35fc-711">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-711">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="b35fc-712">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-712">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="b35fc-713">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="b35fc-713">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="b35fc-714">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="b35fc-714">Parameters - neededPermission</span></span>

<span data-ttu-id="b35fc-715">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-715">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="b35fc-716">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="b35fc-716">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="b35fc-717">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b35fc-717">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="b35fc-718">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b35fc-718">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="b35fc-719">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="b35fc-719">Method parentControl</span></span>

<span data-ttu-id="b35fc-720">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-720">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="b35fc-721">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="b35fc-721">Return Value - parentControl</span></span>

<span data-ttu-id="b35fc-722">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="b35fc-722">The parent control for the control.</span></span>

## <a name="method-processpicture"></a><span data-ttu-id="b35fc-723">メソッド processPicture</span><span class="sxs-lookup"><span data-stu-id="b35fc-723">Method processPicture</span></span>

```xpp
public str processPicture(str picture)
```

### <a name="parameters---processpicture"></a><span data-ttu-id="b35fc-724">パラメーター - processPicture</span><span class="sxs-lookup"><span data-stu-id="b35fc-724">Parameters - processPicture</span></span>

<span data-ttu-id="b35fc-725">picture</span><span class="sxs-lookup"><span data-stu-id="b35fc-725">picture</span></span>  

### <a name="return-value---processpicture"></a><span data-ttu-id="b35fc-726">戻り値 - processPicture</span><span class="sxs-lookup"><span data-stu-id="b35fc-726">Return Value - processPicture</span></span>

## <a name="method-rtlcapable"></a><span data-ttu-id="b35fc-727">メソッド rTLCapable</span><span class="sxs-lookup"><span data-stu-id="b35fc-727">Method rTLCapable</span></span>

```xpp
public boolean rTLCapable([boolean value])
```

### <a name="parameters---rtlcapable"></a><span data-ttu-id="b35fc-728">パラメーター - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="b35fc-728">Parameters - rTLCapable</span></span>

<span data-ttu-id="b35fc-729">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-729">value</span></span>  

### <a name="return-value---rtlcapable"></a><span data-ttu-id="b35fc-730">戻り値 - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="b35fc-730">Return Value - rTLCapable</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="b35fc-731">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="b35fc-731">Method securityKey</span></span>

<span data-ttu-id="b35fc-732">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-732">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="b35fc-733">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="b35fc-733">Parameters - securityKey</span></span>

<span data-ttu-id="b35fc-734">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-734">value</span></span>  
<span data-ttu-id="b35fc-735">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-735">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="b35fc-736">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="b35fc-736">Return Value - securityKey</span></span>

<span data-ttu-id="b35fc-737">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-737">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="b35fc-738">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="b35fc-738">Method showContextMenu</span></span>

<span data-ttu-id="b35fc-739">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-739">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="b35fc-740">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="b35fc-740">Parameters - showContextMenu</span></span>

<span data-ttu-id="b35fc-741">menuHandle</span><span class="sxs-lookup"><span data-stu-id="b35fc-741">menuHandle</span></span>  
<span data-ttu-id="b35fc-742">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="b35fc-742">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="b35fc-743">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="b35fc-743">Return Value - showContextMenu</span></span>

<span data-ttu-id="b35fc-744">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-744">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="b35fc-745">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="b35fc-745">Method skip</span></span>

<span data-ttu-id="b35fc-746">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-746">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="b35fc-747">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="b35fc-747">Parameters - skip</span></span>

<span data-ttu-id="b35fc-748">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-748">value</span></span>  
<span data-ttu-id="b35fc-749">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-749">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="b35fc-750">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="b35fc-750">Return Value - skip</span></span>

<span data-ttu-id="b35fc-751">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-751">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="b35fc-752">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="b35fc-752">Method toolTip</span></span>

<span data-ttu-id="b35fc-753">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-753">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="b35fc-754">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="b35fc-754">Return Value - toolTip</span></span>

<span data-ttu-id="b35fc-755">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="b35fc-755">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="b35fc-756">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="b35fc-756">Remarks - toolTip</span></span>

<span data-ttu-id="b35fc-757">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-757">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="b35fc-758">メソッド top</span><span class="sxs-lookup"><span data-stu-id="b35fc-758">Method top</span></span>

<span data-ttu-id="b35fc-759">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-759">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="b35fc-760">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="b35fc-760">Parameters - top</span></span>

<span data-ttu-id="b35fc-761">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-761">value</span></span>  
<span data-ttu-id="b35fc-762">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-762">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="b35fc-763">モード</span><span class="sxs-lookup"><span data-stu-id="b35fc-763">mode</span></span>  
<span data-ttu-id="b35fc-764">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-764">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="b35fc-765">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="b35fc-765">Return Value - top</span></span>

<span data-ttu-id="b35fc-766">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="b35fc-766">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="b35fc-767">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-767">Method topMode</span></span>

<span data-ttu-id="b35fc-768">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-768">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="b35fc-769">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-769">Parameters - topMode</span></span>

<span data-ttu-id="b35fc-770">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-770">value</span></span>  
<span data-ttu-id="b35fc-771">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-771">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="b35fc-772">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-772">Return Value - topMode</span></span>

<span data-ttu-id="b35fc-773">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="b35fc-773">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="b35fc-774">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-774">Method topValue</span></span>

<span data-ttu-id="b35fc-775">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-775">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="b35fc-776">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-776">Parameters - topValue</span></span>

<span data-ttu-id="b35fc-777">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-777">value</span></span>  
<span data-ttu-id="b35fc-778">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-778">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="b35fc-779">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-779">Return Value - topValue</span></span>

<span data-ttu-id="b35fc-780">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="b35fc-780">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="b35fc-781">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="b35fc-781">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="b35fc-782">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="b35fc-782">Parameters - type</span></span>

<span data-ttu-id="b35fc-783">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-783">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="b35fc-784">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="b35fc-784">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="b35fc-785">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b35fc-785">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="b35fc-786">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b35fc-786">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="b35fc-787">データ</span><span class="sxs-lookup"><span data-stu-id="b35fc-787">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="b35fc-788">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b35fc-788">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="b35fc-789">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="b35fc-789">Method userData</span></span>

<span data-ttu-id="b35fc-790">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-790">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="b35fc-791">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="b35fc-791">Parameters - userData</span></span>

<span data-ttu-id="b35fc-792">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-792">value</span></span>  
<span data-ttu-id="b35fc-793">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-793">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="b35fc-794">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="b35fc-794">Return Value - userData</span></span>

<span data-ttu-id="b35fc-795">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="b35fc-795">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="b35fc-796">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="b35fc-796">Method userDataItem</span></span>

<span data-ttu-id="b35fc-797">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-797">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="b35fc-798">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="b35fc-798">Parameters - userDataItem</span></span>

<span data-ttu-id="b35fc-799">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-799">value</span></span>  
<span data-ttu-id="b35fc-800">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-800">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="b35fc-801">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="b35fc-801">Return Value - userDataItem</span></span>

<span data-ttu-id="b35fc-802">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="b35fc-802">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="b35fc-803">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="b35fc-803">Method userDataItems</span></span>

<span data-ttu-id="b35fc-804">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-804">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="b35fc-805">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="b35fc-805">Parameters - userDataItems</span></span>

<span data-ttu-id="b35fc-806">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-806">value</span></span>  
<span data-ttu-id="b35fc-807">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-807">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="b35fc-808">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="b35fc-808">Return Value - userDataItems</span></span>

<span data-ttu-id="b35fc-809">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="b35fc-809">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="b35fc-810">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="b35fc-810">Method userDisable</span></span>

<span data-ttu-id="b35fc-811">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-811">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="b35fc-812">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="b35fc-812">Parameters - userDisable</span></span>

<span data-ttu-id="b35fc-813">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-813">value</span></span>  
<span data-ttu-id="b35fc-814">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-814">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="b35fc-815">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="b35fc-815">Return Value - userDisable</span></span>

<span data-ttu-id="b35fc-816">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-816">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="b35fc-817">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="b35fc-817">Method userHeight</span></span>

<span data-ttu-id="b35fc-818">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-818">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="b35fc-819">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="b35fc-819">Parameters - userHeight</span></span>

<span data-ttu-id="b35fc-820">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-820">value</span></span>  
<span data-ttu-id="b35fc-821">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-821">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="b35fc-822">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="b35fc-822">Return Value - userHeight</span></span>

<span data-ttu-id="b35fc-823">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="b35fc-823">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="b35fc-824">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="b35fc-824">Method userHide</span></span>

<span data-ttu-id="b35fc-825">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-825">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="b35fc-826">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="b35fc-826">Parameters - userHide</span></span>

<span data-ttu-id="b35fc-827">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-827">value</span></span>  
<span data-ttu-id="b35fc-828">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-828">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="b35fc-829">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="b35fc-829">Return Value - userHide</span></span>

<span data-ttu-id="b35fc-830">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-830">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="b35fc-831">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="b35fc-831">Remarks - userHide</span></span>

<span data-ttu-id="b35fc-832">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-832">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="b35fc-833">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-833">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="b35fc-834">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-834">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="b35fc-835">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="b35fc-835">Method userOrgContainer</span></span>

<span data-ttu-id="b35fc-836">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-836">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="b35fc-837">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="b35fc-837">Parameters - userOrgContainer</span></span>

<span data-ttu-id="b35fc-838">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-838">value</span></span>  
<span data-ttu-id="b35fc-839">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-839">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="b35fc-840">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="b35fc-840">Return Value - userOrgContainer</span></span>

<span data-ttu-id="b35fc-841">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="b35fc-841">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="b35fc-842">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="b35fc-842">Method userOrgSibling</span></span>

<span data-ttu-id="b35fc-843">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-843">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="b35fc-844">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="b35fc-844">Parameters - userOrgSibling</span></span>

<span data-ttu-id="b35fc-845">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-845">value</span></span>  
<span data-ttu-id="b35fc-846">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-846">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="b35fc-847">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="b35fc-847">Return Value - userOrgSibling</span></span>

<span data-ttu-id="b35fc-848">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="b35fc-848">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="b35fc-849">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="b35fc-849">Method userPromptText</span></span>

<span data-ttu-id="b35fc-850">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-850">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="b35fc-851">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="b35fc-851">Parameters - userPromptText</span></span>

<span data-ttu-id="b35fc-852">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-852">value</span></span>  
<span data-ttu-id="b35fc-853">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-853">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="b35fc-854">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="b35fc-854">Return Value - userPromptText</span></span>

<span data-ttu-id="b35fc-855">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="b35fc-855">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="b35fc-856">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="b35fc-856">Method userSecurityLevel</span></span>

<span data-ttu-id="b35fc-857">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-857">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="b35fc-858">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="b35fc-858">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="b35fc-859">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-859">value</span></span>  
<span data-ttu-id="b35fc-860">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-860">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="b35fc-861">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="b35fc-861">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="b35fc-862">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="b35fc-862">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="b35fc-863">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="b35fc-863">Method userSkip</span></span>

<span data-ttu-id="b35fc-864">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-864">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="b35fc-865">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="b35fc-865">Parameters - userSkip</span></span>

<span data-ttu-id="b35fc-866">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-866">value</span></span>  
<span data-ttu-id="b35fc-867">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-867">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="b35fc-868">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-868">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="b35fc-869">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="b35fc-869">Return Value - userSkip</span></span>

<span data-ttu-id="b35fc-870">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="b35fc-870">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="b35fc-871">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="b35fc-871">Method userWidth</span></span>

<span data-ttu-id="b35fc-872">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-872">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="b35fc-873">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="b35fc-873">Parameters - userWidth</span></span>

<span data-ttu-id="b35fc-874">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-874">value</span></span>  
<span data-ttu-id="b35fc-875">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-875">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="b35fc-876">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="b35fc-876">Return Value - userWidth</span></span>

<span data-ttu-id="b35fc-877">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-877">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="b35fc-878">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="b35fc-878">Remarks - userWidth</span></span>

<span data-ttu-id="b35fc-879">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-879">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="b35fc-880">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-880">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="b35fc-881">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-881">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="b35fc-882">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b35fc-882">Method verticalSpacing</span></span>

<span data-ttu-id="b35fc-883">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-883">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="b35fc-884">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b35fc-884">Parameters - verticalSpacing</span></span>

<span data-ttu-id="b35fc-885">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-885">value</span></span>  
<span data-ttu-id="b35fc-886">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-886">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="b35fc-887">モード</span><span class="sxs-lookup"><span data-stu-id="b35fc-887">mode</span></span>  
<span data-ttu-id="b35fc-888">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-888">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="b35fc-889">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b35fc-889">Return Value - verticalSpacing</span></span>

<span data-ttu-id="b35fc-890">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="b35fc-890">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="b35fc-891">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-891">Method verticalSpacingMode</span></span>

<span data-ttu-id="b35fc-892">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-892">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="b35fc-893">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-893">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="b35fc-894">モード</span><span class="sxs-lookup"><span data-stu-id="b35fc-894">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="b35fc-895">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-895">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="b35fc-896">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="b35fc-896">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="b35fc-897">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-897">Method verticalSpacingValue</span></span>

<span data-ttu-id="b35fc-898">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-898">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="b35fc-899">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-899">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="b35fc-900">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-900">value</span></span>  
<span data-ttu-id="b35fc-901">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-901">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="b35fc-902">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-902">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="b35fc-903">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="b35fc-903">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="b35fc-904">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="b35fc-904">Method visible</span></span>

<span data-ttu-id="b35fc-905">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-905">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="b35fc-906">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="b35fc-906">Parameters - visible</span></span>

<span data-ttu-id="b35fc-907">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-907">value</span></span>  
<span data-ttu-id="b35fc-908">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-908">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="b35fc-909">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="b35fc-909">Return Value - visible</span></span>

<span data-ttu-id="b35fc-910">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="b35fc-910">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="b35fc-911">メソッド width</span><span class="sxs-lookup"><span data-stu-id="b35fc-911">Method width</span></span>

<span data-ttu-id="b35fc-912">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-912">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="b35fc-913">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="b35fc-913">Parameters - width</span></span>

<span data-ttu-id="b35fc-914">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-914">value</span></span>  
<span data-ttu-id="b35fc-915">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-915">An integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="b35fc-916">モード</span><span class="sxs-lookup"><span data-stu-id="b35fc-916">mode</span></span>  
<span data-ttu-id="b35fc-917">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-917">An integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="b35fc-918">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="b35fc-918">Return Value - width</span></span>

<span data-ttu-id="b35fc-919">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b35fc-919">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="b35fc-920">備考 - width</span><span class="sxs-lookup"><span data-stu-id="b35fc-920">Remarks - width</span></span>

<span data-ttu-id="b35fc-921">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-921">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b35fc-922">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b35fc-922">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b35fc-923">モード。</span><span class="sxs-lookup"><span data-stu-id="b35fc-923">Mode.</span></span>           | <span data-ttu-id="b35fc-924">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b35fc-924">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35fc-925">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b35fc-925">-1 Exact.</span></span>       | <span data-ttu-id="b35fc-926">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-926">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b35fc-927">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b35fc-927">0 Auto.</span></span>         | <span data-ttu-id="b35fc-928">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-928">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b35fc-929">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="b35fc-929">1 Column width.</span></span> | <span data-ttu-id="b35fc-930">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-930">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b35fc-931">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-931">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="b35fc-932">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-932">Method widthMode</span></span>

<span data-ttu-id="b35fc-933">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-933">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="b35fc-934">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-934">Parameters - widthMode</span></span>

<span data-ttu-id="b35fc-935">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-935">value</span></span>  
<span data-ttu-id="b35fc-936">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-936">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="b35fc-937">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-937">Return Value - widthMode</span></span>

<span data-ttu-id="b35fc-938">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-938">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="b35fc-939">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-939">Remarks - widthMode</span></span>

<span data-ttu-id="b35fc-940">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b35fc-940">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b35fc-941">モード。</span><span class="sxs-lookup"><span data-stu-id="b35fc-941">Mode.</span></span>         | <span data-ttu-id="b35fc-942">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b35fc-942">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35fc-943">正確。</span><span class="sxs-lookup"><span data-stu-id="b35fc-943">Exact.</span></span>        | <span data-ttu-id="b35fc-944">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-944">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b35fc-945">自動。</span><span class="sxs-lookup"><span data-stu-id="b35fc-945">Auto.</span></span>         | <span data-ttu-id="b35fc-946">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-946">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b35fc-947">列の幅。</span><span class="sxs-lookup"><span data-stu-id="b35fc-947">Column width.</span></span> | <span data-ttu-id="b35fc-948">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-948">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b35fc-949">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b35fc-949">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="b35fc-950">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-950">Method widthValue</span></span>

<span data-ttu-id="b35fc-951">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-951">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="b35fc-952">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-952">Parameters - widthValue</span></span>

<span data-ttu-id="b35fc-953">値</span><span class="sxs-lookup"><span data-stu-id="b35fc-953">value</span></span>  
<span data-ttu-id="b35fc-954">幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="b35fc-954">An integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="b35fc-955">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-955">Return Value - widthValue</span></span>

<span data-ttu-id="b35fc-956">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b35fc-956">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="b35fc-957">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b35fc-957">Remarks - widthValue</span></span>

<span data-ttu-id="b35fc-958">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-958">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-copy"></a><span data-ttu-id="b35fc-959">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="b35fc-959">Method copy</span></span>

<span data-ttu-id="b35fc-960">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b35fc-960">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-inserttext"></a><span data-ttu-id="b35fc-961">メソッド insertText</span><span class="sxs-lookup"><span data-stu-id="b35fc-961">Method insertText</span></span>

```xpp
public void insertText(str Text, [NoYes repaint])
```

### <a name="parameters---inserttext"></a><span data-ttu-id="b35fc-962">パラメーター - insertText</span><span class="sxs-lookup"><span data-stu-id="b35fc-962">Parameters - insertText</span></span>

<span data-ttu-id="b35fc-963">テキスト</span><span class="sxs-lookup"><span data-stu-id="b35fc-963">Text</span></span>  

<!-- -->

<span data-ttu-id="b35fc-964">repaint</span><span class="sxs-lookup"><span data-stu-id="b35fc-964">repaint</span></span>  

## <a name="method-cut"></a><span data-ttu-id="b35fc-965">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="b35fc-965">Method cut</span></span>

<span data-ttu-id="b35fc-966">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="b35fc-966">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-processbase"></a><span data-ttu-id="b35fc-967">メソッド processBase</span><span class="sxs-lookup"><span data-stu-id="b35fc-967">Method processBase</span></span>

```xpp
public void processBase(str base)
```

### <a name="parameters---processbase"></a><span data-ttu-id="b35fc-968">パラメーター - processBase</span><span class="sxs-lookup"><span data-stu-id="b35fc-968">Parameters - processBase</span></span>

<span data-ttu-id="b35fc-969">基本</span><span class="sxs-lookup"><span data-stu-id="b35fc-969">base</span></span>  

## <a name="method-setfont"></a><span data-ttu-id="b35fc-970">メソッド setFont</span><span class="sxs-lookup"><span data-stu-id="b35fc-970">Method setFont</span></span>

```xpp
public void setFont(int fontid, HtmlFont htmlFont, [NoYes repaint])
```

### <a name="parameters---setfont"></a><span data-ttu-id="b35fc-971">パラメーター - setFont</span><span class="sxs-lookup"><span data-stu-id="b35fc-971">Parameters - setFont</span></span>

<span data-ttu-id="b35fc-972">fontid</span><span class="sxs-lookup"><span data-stu-id="b35fc-972">fontid</span></span>  

<!-- -->

<span data-ttu-id="b35fc-973">htmlFont</span><span class="sxs-lookup"><span data-stu-id="b35fc-973">htmlFont</span></span>  

<!-- -->

<span data-ttu-id="b35fc-974">repaint</span><span class="sxs-lookup"><span data-stu-id="b35fc-974">repaint</span></span>  

## <a name="method-getfont"></a><span data-ttu-id="b35fc-975">メソッド getFont</span><span class="sxs-lookup"><span data-stu-id="b35fc-975">Method getFont</span></span>

```xpp
public void getFont(int fontid, HtmlFont htmlFont)
```

### <a name="parameters---getfont"></a><span data-ttu-id="b35fc-976">パラメーター - getFont</span><span class="sxs-lookup"><span data-stu-id="b35fc-976">Parameters - getFont</span></span>

<span data-ttu-id="b35fc-977">fontid</span><span class="sxs-lookup"><span data-stu-id="b35fc-977">fontid</span></span>  

<!-- -->

<span data-ttu-id="b35fc-978">htmlFont</span><span class="sxs-lookup"><span data-stu-id="b35fc-978">htmlFont</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="b35fc-979">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="b35fc-979">Method gotFocus</span></span>

<span data-ttu-id="b35fc-980">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-980">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-onenter"></a><span data-ttu-id="b35fc-981">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="b35fc-981">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="b35fc-982">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="b35fc-982">Parameters - OnEnter</span></span>

<span data-ttu-id="b35fc-983">sender</span><span class="sxs-lookup"><span data-stu-id="b35fc-983">sender</span></span>  

<!-- -->

<span data-ttu-id="b35fc-984">e</span><span class="sxs-lookup"><span data-stu-id="b35fc-984">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="b35fc-985">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="b35fc-985">Method dragLeave</span></span>

<span data-ttu-id="b35fc-986">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-986">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-mouseleave"></a><span data-ttu-id="b35fc-987">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="b35fc-987">Method mouseLeave</span></span>

<span data-ttu-id="b35fc-988">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-988">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-dropex"></a><span data-ttu-id="b35fc-989">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="b35fc-989">Method dropEx</span></span>

<span data-ttu-id="b35fc-990">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-990">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="b35fc-991">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="b35fc-991">Parameters - dropEx</span></span>

<span data-ttu-id="b35fc-992">dragSource</span><span class="sxs-lookup"><span data-stu-id="b35fc-992">dragSource</span></span>  
<span data-ttu-id="b35fc-993">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-993">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-994">dragMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-994">dragMode</span></span>  
<span data-ttu-id="b35fc-995">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-995">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-996">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-996">x</span></span>  
<span data-ttu-id="b35fc-997">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-997">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-998">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-998">y</span></span>  
<span data-ttu-id="b35fc-999">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-999">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-drop"></a><span data-ttu-id="b35fc-1000">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="b35fc-1000">Method drop</span></span>

<span data-ttu-id="b35fc-1001">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1001">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="b35fc-1002">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="b35fc-1002">Parameters - drop</span></span>

<span data-ttu-id="b35fc-1003">dragSource</span><span class="sxs-lookup"><span data-stu-id="b35fc-1003">dragSource</span></span>  
<span data-ttu-id="b35fc-1004">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1004">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-1005">dragMode</span><span class="sxs-lookup"><span data-stu-id="b35fc-1005">dragMode</span></span>  
<span data-ttu-id="b35fc-1006">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1006">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-1007">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-1007">x</span></span>  
<span data-ttu-id="b35fc-1008">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1008">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="b35fc-1009">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-1009">y</span></span>  
<span data-ttu-id="b35fc-1010">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1010">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-updatesize"></a><span data-ttu-id="b35fc-1011">メソッド updateSize</span><span class="sxs-lookup"><span data-stu-id="b35fc-1011">Method updateSize</span></span>

```xpp
public void updateSize()
```

## <a name="method-mouseenter"></a><span data-ttu-id="b35fc-1012">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="b35fc-1012">Method mouseEnter</span></span>

<span data-ttu-id="b35fc-1013">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1013">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="b35fc-1014">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="b35fc-1014">Parameters - mouseEnter</span></span>

<span data-ttu-id="b35fc-1015">x</span><span class="sxs-lookup"><span data-stu-id="b35fc-1015">x</span></span>  
<span data-ttu-id="b35fc-1016">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1016">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-1017">y</span><span class="sxs-lookup"><span data-stu-id="b35fc-1017">y</span></span>  
<span data-ttu-id="b35fc-1018">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1018">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-1019">ボタン</span><span class="sxs-lookup"><span data-stu-id="b35fc-1019">button</span></span>  
<span data-ttu-id="b35fc-1020">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1020">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-1021">Ctrl</span><span class="sxs-lookup"><span data-stu-id="b35fc-1021">Ctrl</span></span>  
<span data-ttu-id="b35fc-1022">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1022">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="b35fc-1023">シフト</span><span class="sxs-lookup"><span data-stu-id="b35fc-1023">Shift</span></span>  
<span data-ttu-id="b35fc-1024">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1024">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-onleaving"></a><span data-ttu-id="b35fc-1025">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="b35fc-1025">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="b35fc-1026">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="b35fc-1026">Parameters - OnLeaving</span></span>

<span data-ttu-id="b35fc-1027">sender</span><span class="sxs-lookup"><span data-stu-id="b35fc-1027">sender</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1028">e</span><span class="sxs-lookup"><span data-stu-id="b35fc-1028">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="b35fc-1029">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="b35fc-1029">Method lostFocus</span></span>

<span data-ttu-id="b35fc-1030">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1030">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="b35fc-1031">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="b35fc-1031">Method displayControl</span></span>

<span data-ttu-id="b35fc-1032">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1032">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-processlink"></a><span data-ttu-id="b35fc-1033">メソッド processLink</span><span class="sxs-lookup"><span data-stu-id="b35fc-1033">Method processLink</span></span>

```xpp
public void processLink(str link)
```

### <a name="parameters---processlink"></a><span data-ttu-id="b35fc-1034">パラメーター - processLink</span><span class="sxs-lookup"><span data-stu-id="b35fc-1034">Parameters - processLink</span></span>

<span data-ttu-id="b35fc-1035">リンク</span><span class="sxs-lookup"><span data-stu-id="b35fc-1035">link</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="b35fc-1036">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="b35fc-1036">Method prefColumnSize</span></span>

<span data-ttu-id="b35fc-1037">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1037">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="b35fc-1038">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="b35fc-1038">Parameters - prefColumnSize</span></span>

<span data-ttu-id="b35fc-1039">width</span><span class="sxs-lookup"><span data-stu-id="b35fc-1039">width</span></span>  
<span data-ttu-id="b35fc-1040">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1040">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="b35fc-1041">height</span><span class="sxs-lookup"><span data-stu-id="b35fc-1041">height</span></span>  
<span data-ttu-id="b35fc-1042">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1042">The preferred height of the control.</span></span>

## <a name="method-processtitle"></a><span data-ttu-id="b35fc-1043">メソッド processTitle</span><span class="sxs-lookup"><span data-stu-id="b35fc-1043">Method processTitle</span></span>

```xpp
public void processTitle(str title)
```

### <a name="parameters---processtitle"></a><span data-ttu-id="b35fc-1044">パラメーター - processTitle</span><span class="sxs-lookup"><span data-stu-id="b35fc-1044">Parameters - processTitle</span></span>

<span data-ttu-id="b35fc-1045">タイトル</span><span class="sxs-lookup"><span data-stu-id="b35fc-1045">title</span></span>  

## <a name="method-read"></a><span data-ttu-id="b35fc-1046">メソッド read</span><span class="sxs-lookup"><span data-stu-id="b35fc-1046">Method read</span></span>

```xpp
public void read(str FileName, [str TagName])
```

### <a name="parameters---read"></a><span data-ttu-id="b35fc-1047">パラメーター - read</span><span class="sxs-lookup"><span data-stu-id="b35fc-1047">Parameters - read</span></span>

<span data-ttu-id="b35fc-1048">FileName</span><span class="sxs-lookup"><span data-stu-id="b35fc-1048">FileName</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1049">TagName</span><span class="sxs-lookup"><span data-stu-id="b35fc-1049">TagName</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="b35fc-1050">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="b35fc-1050">Method setFocus</span></span>

<span data-ttu-id="b35fc-1051">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1051">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="b35fc-1052">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="b35fc-1052">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="b35fc-1053">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="b35fc-1053">Parameters - OnLostFocus</span></span>

<span data-ttu-id="b35fc-1054">sender</span><span class="sxs-lookup"><span data-stu-id="b35fc-1054">sender</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1055">e</span><span class="sxs-lookup"><span data-stu-id="b35fc-1055">e</span></span>  

## <a name="method-settext"></a><span data-ttu-id="b35fc-1056">メソッド setText</span><span class="sxs-lookup"><span data-stu-id="b35fc-1056">Method setText</span></span>

```xpp
public void setText(str Text, [str TagName])
```

### <a name="parameters---settext"></a><span data-ttu-id="b35fc-1057">パラメーター - setText</span><span class="sxs-lookup"><span data-stu-id="b35fc-1057">Parameters - setText</span></span>

<span data-ttu-id="b35fc-1058">テキスト</span><span class="sxs-lookup"><span data-stu-id="b35fc-1058">Text</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1059">TagName</span><span class="sxs-lookup"><span data-stu-id="b35fc-1059">TagName</span></span>  

## <a name="method-ongotfocus"></a><span data-ttu-id="b35fc-1060">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="b35fc-1060">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="b35fc-1061">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="b35fc-1061">Parameters - OnGotFocus</span></span>

<span data-ttu-id="b35fc-1062">sender</span><span class="sxs-lookup"><span data-stu-id="b35fc-1062">sender</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1063">e</span><span class="sxs-lookup"><span data-stu-id="b35fc-1063">e</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="b35fc-1064">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="b35fc-1064">Method resetUserSetting</span></span>

<span data-ttu-id="b35fc-1065">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1065">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="b35fc-1066">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="b35fc-1066">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="b35fc-1067">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="b35fc-1067">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="b35fc-1068">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="b35fc-1068">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1069">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="b35fc-1069">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1070">overrideObject</span><span class="sxs-lookup"><span data-stu-id="b35fc-1070">overrideObject</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="b35fc-1071">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="b35fc-1071">Method endDrag</span></span>

<span data-ttu-id="b35fc-1072">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1072">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="b35fc-1073">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="b35fc-1073">Remarks - endDrag</span></span>

<span data-ttu-id="b35fc-1074">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1074">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="b35fc-1075">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1075">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-save"></a><span data-ttu-id="b35fc-1076">メソッド save</span><span class="sxs-lookup"><span data-stu-id="b35fc-1076">Method save</span></span>

```xpp
public void save(str FileName)
```

### <a name="parameters---save"></a><span data-ttu-id="b35fc-1077">パラメーター - save</span><span class="sxs-lookup"><span data-stu-id="b35fc-1077">Parameters - save</span></span>

<span data-ttu-id="b35fc-1078">FileName</span><span class="sxs-lookup"><span data-stu-id="b35fc-1078">FileName</span></span>  

## <a name="method-command"></a><span data-ttu-id="b35fc-1079">メソッド command</span><span class="sxs-lookup"><span data-stu-id="b35fc-1079">Method command</span></span>

```xpp
public void command(int command)
```

### <a name="parameters---command"></a><span data-ttu-id="b35fc-1080">パラメーター - command</span><span class="sxs-lookup"><span data-stu-id="b35fc-1080">Parameters - command</span></span>

<span data-ttu-id="b35fc-1081">command</span><span class="sxs-lookup"><span data-stu-id="b35fc-1081">command</span></span>  

## <a name="method-paste"></a><span data-ttu-id="b35fc-1082">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="b35fc-1082">Method paste</span></span>

<span data-ttu-id="b35fc-1083">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1083">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-insertlink"></a><span data-ttu-id="b35fc-1084">メソッド insertLink</span><span class="sxs-lookup"><span data-stu-id="b35fc-1084">Method insertLink</span></span>

```xpp
public void insertLink(str Text, str Url, str Name, [NoYes repaint])
```

### <a name="parameters---insertlink"></a><span data-ttu-id="b35fc-1085">パラメーター - insertLink</span><span class="sxs-lookup"><span data-stu-id="b35fc-1085">Parameters - insertLink</span></span>

<span data-ttu-id="b35fc-1086">テキスト</span><span class="sxs-lookup"><span data-stu-id="b35fc-1086">Text</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1087">URL</span><span class="sxs-lookup"><span data-stu-id="b35fc-1087">Url</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1088">氏名</span><span class="sxs-lookup"><span data-stu-id="b35fc-1088">Name</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1089">repaint</span><span class="sxs-lookup"><span data-stu-id="b35fc-1089">repaint</span></span>  

## <a name="method-context"></a><span data-ttu-id="b35fc-1090">メソッド context</span><span class="sxs-lookup"><span data-stu-id="b35fc-1090">Method context</span></span>

<span data-ttu-id="b35fc-1091">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1091">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enter"></a><span data-ttu-id="b35fc-1092">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="b35fc-1092">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-inputsearch"></a><span data-ttu-id="b35fc-1093">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="b35fc-1093">Method inputSearch</span></span>

<span data-ttu-id="b35fc-1094">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1094">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="b35fc-1095">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="b35fc-1095">Parameters - inputSearch</span></span>

<span data-ttu-id="b35fc-1096">searchStr</span><span class="sxs-lookup"><span data-stu-id="b35fc-1096">searchStr</span></span>  
<span data-ttu-id="b35fc-1097">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b35fc-1097">The string value to use to filter data; optional.</span></span>

## <a name="method-clearwindow"></a><span data-ttu-id="b35fc-1098">メソッド clearWindow</span><span class="sxs-lookup"><span data-stu-id="b35fc-1098">Method clearWindow</span></span>

```xpp
public void clearWindow()
```

## <a name="method-processform"></a><span data-ttu-id="b35fc-1099">メソッド processForm</span><span class="sxs-lookup"><span data-stu-id="b35fc-1099">Method processForm</span></span>

```xpp
public void processForm(int formHandle)
```

### <a name="parameters---processform"></a><span data-ttu-id="b35fc-1100">パラメーター - processForm</span><span class="sxs-lookup"><span data-stu-id="b35fc-1100">Parameters - processForm</span></span>

<span data-ttu-id="b35fc-1101">formHandle</span><span class="sxs-lookup"><span data-stu-id="b35fc-1101">formHandle</span></span>  

## <a name="method-setmargin"></a><span data-ttu-id="b35fc-1102">メソッド setMargin</span><span class="sxs-lookup"><span data-stu-id="b35fc-1102">Method setMargin</span></span>

```xpp
public void setMargin(int Left, int Right, int Top, int Bottom, [NoYes repaint])
```

### <a name="parameters---setmargin"></a><span data-ttu-id="b35fc-1103">パラメーター - setMargin</span><span class="sxs-lookup"><span data-stu-id="b35fc-1103">Parameters - setMargin</span></span>

<span data-ttu-id="b35fc-1104">左</span><span class="sxs-lookup"><span data-stu-id="b35fc-1104">Left</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1105">右</span><span class="sxs-lookup"><span data-stu-id="b35fc-1105">Right</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1106">上</span><span class="sxs-lookup"><span data-stu-id="b35fc-1106">Top</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1107">下</span><span class="sxs-lookup"><span data-stu-id="b35fc-1107">Bottom</span></span>  

<!-- -->

<span data-ttu-id="b35fc-1108">repaint</span><span class="sxs-lookup"><span data-stu-id="b35fc-1108">repaint</span></span>  

