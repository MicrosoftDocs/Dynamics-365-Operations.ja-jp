---
title: FormActiveXControl クラス
description: このトピックでは、FormActiveXControl クラスについて説明します。
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
ms.openlocfilehash: 9d6925f82706d03ceb31eef4ec0489b7acfdcbcd
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502663"
---
# <a name="class-formactivexcontrol"></a><span data-ttu-id="48258-103">クラス FormActiveXControl</span><span class="sxs-lookup"><span data-stu-id="48258-103">Class FormActiveXControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormActiveXControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="48258-104">備考</span><span class="sxs-lookup"><span data-stu-id="48258-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="48258-105">例</span><span class="sxs-lookup"><span data-stu-id="48258-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="48258-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="48258-106">Methods</span></span>

| <span data-ttu-id="48258-107">方法</span><span class="sxs-lookup"><span data-stu-id="48258-107">Method</span></span>                                                                                                      | <span data-ttu-id="48258-108">説明</span><span class="sxs-lookup"><span data-stu-id="48258-108">Description</span></span>                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48258-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48258-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="48258-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-110">Determines whether to align the control.</span></span>                                                                                                             |
| <span data-ttu-id="48258-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48258-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="48258-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-112">Determines whether the user can change the contents of the control.</span></span>                                                                                  |
| <span data-ttu-id="48258-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="48258-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="48258-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                  |
| <span data-ttu-id="48258-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48258-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="48258-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                   |
| <span data-ttu-id="48258-117">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48258-117">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="48258-118">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-118">Is called when the user starts to drag a form control.</span></span>                                                                                               |
| <span data-ttu-id="48258-119">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="48258-119">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="48258-120">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-120">Retrieves the size of the control.</span></span>                                                                                                                   |
| <span data-ttu-id="48258-121">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-121">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="48258-122">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-122">Gets or set the caption of the control.</span></span>                                                                                                              |
| <span data-ttu-id="48258-123">public str className(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-123">public str className(\[str value\])</span></span>                                                                         |                                                                                                                                                      |
| <span data-ttu-id="48258-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="48258-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="48258-125">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-125">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                  |
| <span data-ttu-id="48258-126">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="48258-126">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="48258-127">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-127">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                     |
| <span data-ttu-id="48258-128">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-128">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="48258-129">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-129">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                       |
| <span data-ttu-id="48258-130">public str custom(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-130">public str custom(\[str value\])</span></span>                                                                            |                                                                                                                                                      |
| <span data-ttu-id="48258-131">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-131">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="48258-132">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-132">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                        |
| <span data-ttu-id="48258-133">public AnyType dispatch(VarArg )</span><span class="sxs-lookup"><span data-stu-id="48258-133">public AnyType dispatch(VarArg )</span></span>                                                                            |                                                                                                                                                      |
| <span data-ttu-id="48258-134">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-134">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="48258-135">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-135">Gets or sets the value that indicates whether the control is displayed in the client, or in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="48258-136">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-136">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="48258-137">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-137">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                    |
| <span data-ttu-id="48258-138">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48258-138">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="48258-139">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-139">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                       |
| <span data-ttu-id="48258-140">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48258-140">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="48258-141">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-141">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                     |
| <span data-ttu-id="48258-142">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="48258-142">public str dragText()</span></span>                                                                                       | <span data-ttu-id="48258-143">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-143">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                               |
| <span data-ttu-id="48258-144">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48258-144">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="48258-145">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-145">Determines whether to enable or disable the object.</span></span>                                                                                                  |
| <span data-ttu-id="48258-146">public COMError error()</span><span class="sxs-lookup"><span data-stu-id="48258-146">public COMError error()</span></span>                                                                                     |                                                                                                                                                      |
| <span data-ttu-id="48258-147">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="48258-147">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="48258-148">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-148">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                             |
| <span data-ttu-id="48258-149">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="48258-149">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="48258-150">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48258-150">Indicates whether the control has custom user settings.</span></span>                                                                                              |
| <span data-ttu-id="48258-151">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48258-151">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="48258-152">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-152">Gets or sets the height of the control.</span></span>                                                                                                              |
| <span data-ttu-id="48258-153">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-153">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="48258-154">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-154">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                       |
| <span data-ttu-id="48258-155">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-155">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="48258-156">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-156">Gets or sets the height of the control.</span></span>                                                                                                              |
| <span data-ttu-id="48258-157">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="48258-157">public str helpField()</span></span>                                                                                      | <span data-ttu-id="48258-158">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-158">Retrieves the Help text for the control.</span></span>                                                                                                             |
| <span data-ttu-id="48258-159">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-159">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="48258-160">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-160">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                             |
| <span data-ttu-id="48258-161">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-161">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="48258-162">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-162">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                      |
| <span data-ttu-id="48258-163">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="48258-163">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="48258-164">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-164">Retrieves the Windows handle for the control.</span></span>                                                                                                        |
| <span data-ttu-id="48258-165">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="48258-165">public ComInterface interface()</span></span>                                                                             |                                                                                                                                                      |
| <span data-ttu-id="48258-166">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="48258-166">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                      |
| <span data-ttu-id="48258-167">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="48258-167">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="48258-168">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-168">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                   |
| <span data-ttu-id="48258-169">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="48258-169">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="48258-170">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-170">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                  |
| <span data-ttu-id="48258-171">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="48258-171">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="48258-172">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="48258-172">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                  |
| <span data-ttu-id="48258-173">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="48258-173">public boolean leave()</span></span>                                                                                      |                                                                                                                                                      |
| <span data-ttu-id="48258-174">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48258-174">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="48258-175">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-175">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                     |
| <span data-ttu-id="48258-176">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-176">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="48258-177">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-177">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="48258-178">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-178">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="48258-179">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-179">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                     |
| <span data-ttu-id="48258-180">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48258-180">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="48258-181">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="48258-181">Marks or unmarks the control as a user-added control.</span></span>                                                                                                |
| <span data-ttu-id="48258-182">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48258-182">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="48258-183">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-183">Is called when the control is double-clicked by the user.</span></span>                                                                                            |
| <span data-ttu-id="48258-184">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48258-184">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="48258-185">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-185">Is called when the user clicks the mouse button over the control.</span></span>                                                                                    |
| <span data-ttu-id="48258-186">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48258-186">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="48258-187">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-187">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                    |
| <span data-ttu-id="48258-188">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48258-188">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="48258-189">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-189">Is called when the user releases the mouse button over the control area.</span></span>                                                                             |
| <span data-ttu-id="48258-190">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-190">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="48258-191">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-191">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>              |
| <span data-ttu-id="48258-192">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-192">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                      |
| <span data-ttu-id="48258-193">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="48258-193">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                      |
| <span data-ttu-id="48258-194">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="48258-194">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="48258-195">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-195">Retrieves the parent control for the control.</span></span>                                                                                                        |
| <span data-ttu-id="48258-196">public boolean rTLCapable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48258-196">public boolean rTLCapable(\[boolean value\])</span></span>                                                                |                                                                                                                                                      |
| <span data-ttu-id="48258-197">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="48258-197">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="48258-198">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-198">Sets or returns the ID of the security key for the control.</span></span>                                                                                          |
| <span data-ttu-id="48258-199">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="48258-199">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="48258-200">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="48258-200">Shows the shortcut menu for the control.</span></span>                                                                                                             |
| <span data-ttu-id="48258-201">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48258-201">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="48258-202">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-202">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                      |
| <span data-ttu-id="48258-203">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="48258-203">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="48258-204">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-204">Retrieves the tooltip text for the control.</span></span>                                                                                                          |
| <span data-ttu-id="48258-205">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48258-205">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="48258-206">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-206">Gets or sets the vertical position of the control in the form.</span></span>                                                                                       |
| <span data-ttu-id="48258-207">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-207">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="48258-208">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-208">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                          |
| <span data-ttu-id="48258-209">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-209">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="48258-210">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-210">Gets or sets the vertical position of the control in the form.</span></span>                                                                                       |
| <span data-ttu-id="48258-211">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-211">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                      |
| <span data-ttu-id="48258-212">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="48258-212">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                      |
| <span data-ttu-id="48258-213">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-213">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="48258-214">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-214">Gets or sets the user data for the control.</span></span>                                                                                                          |
| <span data-ttu-id="48258-215">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-215">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="48258-216">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-216">Gets or sets the user data item for the control.</span></span>                                                                                                     |
| <span data-ttu-id="48258-217">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-217">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="48258-218">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-218">Gets or sets the number of user data items for the control.</span></span>                                                                                          |
| <span data-ttu-id="48258-219">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-219">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="48258-220">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-220">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                  |
| <span data-ttu-id="48258-221">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-221">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="48258-222">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-222">Gets or sets the custom user height for the control.</span></span>                                                                                                 |
| <span data-ttu-id="48258-223">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-223">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="48258-224">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-224">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                   |
| <span data-ttu-id="48258-225">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-225">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="48258-226">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-226">Gets or sets the organization container for the control.</span></span>                                                                                             |
| <span data-ttu-id="48258-227">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-227">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="48258-228">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-228">Gets or sets the organization sibling for the control.</span></span>                                                                                               |
| <span data-ttu-id="48258-229">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48258-229">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="48258-230">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-230">Gets or sets the user label text for the control.</span></span>                                                                                                    |
| <span data-ttu-id="48258-231">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-231">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="48258-232">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-232">Gets or sets the user security level for the control.</span></span>                                                                                                |
| <span data-ttu-id="48258-233">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-233">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="48258-234">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-234">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls on the form.</span></span> |
| <span data-ttu-id="48258-235">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-235">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="48258-236">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-236">Sets or returns the width of the control in pixels.</span></span>                                                                                                  |
| <span data-ttu-id="48258-237">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="48258-237">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="48258-238">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-238">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="48258-239">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="48258-239">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="48258-240">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-240">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                          |
| <span data-ttu-id="48258-241">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-241">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="48258-242">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-242">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="48258-243">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48258-243">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="48258-244">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-244">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                               |
| <span data-ttu-id="48258-245">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48258-245">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="48258-246">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-246">Gets or sets the width of the control.</span></span>                                                                                                               |
| <span data-ttu-id="48258-247">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-247">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="48258-248">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-248">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                       |
| <span data-ttu-id="48258-249">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48258-249">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="48258-250">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-250">Gets or sets the width of the control.</span></span>                                                                                                               |
| <span data-ttu-id="48258-251">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="48258-251">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="48258-252">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="48258-252">Performs data filtering for the control, based on the specified string.</span></span>                                                                              |
| <span data-ttu-id="48258-253">public void copy()</span><span class="sxs-lookup"><span data-stu-id="48258-253">public void copy()</span></span>                                                                                          | <span data-ttu-id="48258-254">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="48258-254">Copies the contents of the control to the clipboard.</span></span>                                                                                                 |
| <span data-ttu-id="48258-255">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="48258-255">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="48258-256">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-256">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                     |
| <span data-ttu-id="48258-257">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48258-257">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="48258-258">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-258">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                   |
| <span data-ttu-id="48258-259">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48258-259">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="48258-260">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-260">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                               |
| <span data-ttu-id="48258-261">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="48258-261">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                      |
| <span data-ttu-id="48258-262">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="48258-262">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="48258-263">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="48258-263">Resets the user settings for the control.</span></span>                                                                                                            |
| <span data-ttu-id="48258-264">public void context()</span><span class="sxs-lookup"><span data-stu-id="48258-264">public void context()</span></span>                                                                                       | <span data-ttu-id="48258-265">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="48258-265">Shows the shortcut menu for the control.</span></span>                                                                                                             |
| <span data-ttu-id="48258-266">public void enter()</span><span class="sxs-lookup"><span data-stu-id="48258-266">public void enter()</span></span>                                                                                         |                                                                                                                                                      |
| <span data-ttu-id="48258-267">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48258-267">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                      |
| <span data-ttu-id="48258-268">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="48258-268">public void displayControl()</span></span>                                                                                | <span data-ttu-id="48258-269">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="48258-269">Displays the control.</span></span>                                                                                                                                |
| <span data-ttu-id="48258-270">public void updateSize()</span><span class="sxs-lookup"><span data-stu-id="48258-270">public void updateSize()</span></span>                                                                                    |                                                                                                                                                      |
| <span data-ttu-id="48258-271">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="48258-271">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="48258-272">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="48258-272">Indicates that the control has received focus.</span></span>                                                                                                       |
| <span data-ttu-id="48258-273">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="48258-273">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="48258-274">ユーザーがマウス ポインターをコントロール エリアから移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-274">Is called when the user moves the mouse pointer out of the control area.</span></span>                                                                             |
| <span data-ttu-id="48258-275">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48258-275">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="48258-276">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-276">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                 |
| <span data-ttu-id="48258-277">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="48258-277">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="48258-278">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-278">Is called when the user has finished dragging a form control.</span></span>                                                                                        |
| <span data-ttu-id="48258-279">public void cut()</span><span class="sxs-lookup"><span data-stu-id="48258-279">public void cut()</span></span>                                                                                           | <span data-ttu-id="48258-280">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="48258-280">Cuts the contents of the control.</span></span>                                                                                                                    |
| <span data-ttu-id="48258-281">public void paste()</span><span class="sxs-lookup"><span data-stu-id="48258-281">public void paste()</span></span>                                                                                         | <span data-ttu-id="48258-282">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="48258-282">Pastes the contents of the clipboard into the control.</span></span>                                                                                               |
| <span data-ttu-id="48258-283">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48258-283">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                      |
| <span data-ttu-id="48258-284">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="48258-284">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="48258-285">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="48258-285">Specifies the preferred column width and height for the form control.</span></span>                                                                                |
| <span data-ttu-id="48258-286">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48258-286">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                      |
| <span data-ttu-id="48258-287">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48258-287">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                      |
| <span data-ttu-id="48258-288">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="48258-288">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="48258-289">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-289">Sets the focus on the control.</span></span>                                                                                                                       |
| <span data-ttu-id="48258-290">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="48258-290">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="48258-291">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="48258-291">Indicates that the control has lost focus.</span></span>                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="48258-292">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="48258-292">Method alignControl</span></span>

<span data-ttu-id="48258-293">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-293">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="48258-294">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="48258-294">Parameters - alignControl</span></span>

<span data-ttu-id="48258-295">値</span><span class="sxs-lookup"><span data-stu-id="48258-295">value</span></span>  
<span data-ttu-id="48258-296">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-296">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="48258-297">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="48258-297">Return Value - alignControl</span></span>

<span data-ttu-id="48258-298">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="48258-298">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="48258-299">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="48258-299">Remarks - alignControl</span></span>

<span data-ttu-id="48258-300">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="48258-300">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="48258-301">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="48258-301">Method allowEdit</span></span>

<span data-ttu-id="48258-302">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-302">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="48258-303">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="48258-303">Parameters - allowEdit</span></span>

<span data-ttu-id="48258-304">値</span><span class="sxs-lookup"><span data-stu-id="48258-304">value</span></span>  
<span data-ttu-id="48258-305">allowEdit プロパティに割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="48258-305">The value to be assigned to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="48258-306">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="48258-306">Return Value - allowEdit</span></span>

<span data-ttu-id="48258-307">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-307">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="48258-308">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="48258-308">Remarks - allowEdit</span></span>

<span data-ttu-id="48258-309">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="48258-309">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="48258-310">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="48258-310">Method allowSysSetup</span></span>

<span data-ttu-id="48258-311">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-311">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="48258-312">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="48258-312">Return Value - allowSysSetup</span></span>

<span data-ttu-id="48258-313">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-313">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="48258-314">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="48258-314">Method autoDeclaration</span></span>

<span data-ttu-id="48258-315">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-315">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="48258-316">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="48258-316">Parameters - autoDeclaration</span></span>

<span data-ttu-id="48258-317">値</span><span class="sxs-lookup"><span data-stu-id="48258-317">value</span></span>  
<span data-ttu-id="48258-318">指定されている場合、プロパティはこの値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="48258-318">The property is set to this value, if supplied.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="48258-319">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="48258-319">Return Value - autoDeclaration</span></span>

<span data-ttu-id="48258-320">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-320">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="48258-321">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="48258-321">Remarks - autoDeclaration</span></span>

<span data-ttu-id="48258-322">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="48258-322">Controls cannot have identical names.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="48258-323">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="48258-323">Method beginDrag</span></span>

<span data-ttu-id="48258-324">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-324">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="48258-325">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="48258-325">Parameters - beginDrag</span></span>

<span data-ttu-id="48258-326">x</span><span class="sxs-lookup"><span data-stu-id="48258-326">x</span></span>  
<span data-ttu-id="48258-327">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-327">An integer value that indicates the y-coordinate of the mouse pointer.</span></span>

<!-- -->

<span data-ttu-id="48258-328">y</span><span class="sxs-lookup"><span data-stu-id="48258-328">y</span></span>  
<span data-ttu-id="48258-329">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-329">An integer value that indicates the y-coordinate of the mouse pointer.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="48258-330">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="48258-330">Return Value - beginDrag</span></span>

<span data-ttu-id="48258-331">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48258-331">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="48258-332">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="48258-332">Remarks - beginDrag</span></span>

<span data-ttu-id="48258-333">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="48258-333">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="48258-334">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="48258-334">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="48258-335">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="48258-335">Method calcControlSize</span></span>

<span data-ttu-id="48258-336">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-336">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="48258-337">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="48258-337">Parameters - calcControlSize</span></span>

<span data-ttu-id="48258-338">chars</span><span class="sxs-lookup"><span data-stu-id="48258-338">chars</span></span>  
<span data-ttu-id="48258-339">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="48258-339">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="48258-340">明細行</span><span class="sxs-lookup"><span data-stu-id="48258-340">lines</span></span>  
<span data-ttu-id="48258-341">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="48258-341">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="48258-342">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="48258-342">Return Value - calcControlSize</span></span>

<span data-ttu-id="48258-343">幅と高さのあるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="48258-343">The container that has the width and height.</span></span>

## <a name="method-caption"></a><span data-ttu-id="48258-344">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="48258-344">Method caption</span></span>

<span data-ttu-id="48258-345">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-345">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="48258-346">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="48258-346">Parameters - caption</span></span>

<span data-ttu-id="48258-347">値</span><span class="sxs-lookup"><span data-stu-id="48258-347">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="48258-348">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="48258-348">Return Value - caption</span></span>

<span data-ttu-id="48258-349">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="48258-349">The string that is used as the caption of the control.</span></span>

## <a name="method-classname"></a><span data-ttu-id="48258-350">メソッド className</span><span class="sxs-lookup"><span data-stu-id="48258-350">Method className</span></span>

```xpp
public str className([str value])
```

### <a name="parameters---classname"></a><span data-ttu-id="48258-351">パラメーター - className</span><span class="sxs-lookup"><span data-stu-id="48258-351">Parameters - className</span></span>

<span data-ttu-id="48258-352">値</span><span class="sxs-lookup"><span data-stu-id="48258-352">value</span></span>  

### <a name="return-value---classname"></a><span data-ttu-id="48258-353">戻り値 - className</span><span class="sxs-lookup"><span data-stu-id="48258-353">Return Value - className</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="48258-354">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="48258-354">Method configurationKey</span></span>

<span data-ttu-id="48258-355">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-355">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="48258-356">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="48258-356">Parameters - configurationKey</span></span>

<span data-ttu-id="48258-357">値</span><span class="sxs-lookup"><span data-stu-id="48258-357">value</span></span>  
<span data-ttu-id="48258-358">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-358">The ID of the configuration key that is being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="48258-359">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="48258-359">Return Value - configurationKey</span></span>

<span data-ttu-id="48258-360">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="48258-360">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="48258-361">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="48258-361">Remarks - configurationKey</span></span>

<span data-ttu-id="48258-362">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="48258-362">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="48258-363">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="48258-363">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="48258-364">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="48258-364">Method configurationKeyEx</span></span>

<span data-ttu-id="48258-365">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-365">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="48258-366">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="48258-366">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="48258-367">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="48258-367">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="48258-368">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="48258-368">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="48258-369">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="48258-369">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="48258-370">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="48258-370">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="48258-371">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="48258-371">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="48258-372">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="48258-372">Method countryRegionCodes</span></span>

<span data-ttu-id="48258-373">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-373">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="48258-374">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="48258-374">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="48258-375">値</span><span class="sxs-lookup"><span data-stu-id="48258-375">value</span></span>  
<span data-ttu-id="48258-376">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-376">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="48258-377">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="48258-377">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="48258-378">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="48258-378">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-custom"></a><span data-ttu-id="48258-379">メソッド custom</span><span class="sxs-lookup"><span data-stu-id="48258-379">Method custom</span></span>

```xpp
public str custom([str value])
```

### <a name="parameters---custom"></a><span data-ttu-id="48258-380">パラメーター - custom</span><span class="sxs-lookup"><span data-stu-id="48258-380">Parameters - custom</span></span>

<span data-ttu-id="48258-381">値</span><span class="sxs-lookup"><span data-stu-id="48258-381">value</span></span>  

### <a name="return-value---custom"></a><span data-ttu-id="48258-382">戻り値 - custom</span><span class="sxs-lookup"><span data-stu-id="48258-382">Return Value - custom</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="48258-383">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="48258-383">Method dataRelationPath</span></span>

<span data-ttu-id="48258-384">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-384">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="48258-385">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="48258-385">Parameters - dataRelationPath</span></span>

<span data-ttu-id="48258-386">値</span><span class="sxs-lookup"><span data-stu-id="48258-386">value</span></span>  
<span data-ttu-id="48258-387">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-387">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="48258-388">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="48258-388">Return Value - dataRelationPath</span></span>

<span data-ttu-id="48258-389">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="48258-389">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="48258-390">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="48258-390">Remarks - dataRelationPath</span></span>

<span data-ttu-id="48258-391">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="48258-391">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="48258-392">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="48258-392">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-dispatch"></a><span data-ttu-id="48258-393">メソッド dispatch</span><span class="sxs-lookup"><span data-stu-id="48258-393">Method dispatch</span></span>

```xpp
public AnyType dispatch(VarArg )
```

### <a name="parameters---dispatch"></a><span data-ttu-id="48258-394">パラメーター - dispatch</span><span class="sxs-lookup"><span data-stu-id="48258-394">Parameters - dispatch</span></span>


### <a name="return-value---dispatch"></a><span data-ttu-id="48258-395">戻り値 - dispatch</span><span class="sxs-lookup"><span data-stu-id="48258-395">Return Value - dispatch</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="48258-396">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="48258-396">Method displayTarget</span></span>

<span data-ttu-id="48258-397">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-397">Gets or sets the value that indicates whether the control is displayed in the client, or in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="48258-398">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="48258-398">Parameters - displayTarget</span></span>

<span data-ttu-id="48258-399">値</span><span class="sxs-lookup"><span data-stu-id="48258-399">value</span></span>  
<span data-ttu-id="48258-400">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-400">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="48258-401">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="48258-401">Return Value - displayTarget</span></span>

<span data-ttu-id="48258-402">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="48258-402">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="48258-403">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="48258-403">Method dragDrop</span></span>

<span data-ttu-id="48258-404">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-404">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="48258-405">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="48258-405">Parameters - dragDrop</span></span>

<span data-ttu-id="48258-406">値</span><span class="sxs-lookup"><span data-stu-id="48258-406">value</span></span>  
<span data-ttu-id="48258-407">ドラッグ アンド ドロップの動作が有効かどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-407">An Integer data type that indicates whether the drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="48258-408">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="48258-408">Return Value - dragDrop</span></span>

<span data-ttu-id="48258-409">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="48258-409">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="48258-410">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="48258-410">Remarks - dragDrop</span></span>

<span data-ttu-id="48258-411">FormControl::dragLeave、FormControl::dragOver、および FormControl::dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="48258-411">Use the FormControl::dragLeave, FormControl::dragOver, and FormControl::dragOverEx methods to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="48258-412">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="48258-412">Method dragOver</span></span>

<span data-ttu-id="48258-413">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-413">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="48258-414">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="48258-414">Parameters - dragOver</span></span>

<span data-ttu-id="48258-415">dragSource</span><span class="sxs-lookup"><span data-stu-id="48258-415">dragSource</span></span>  
<span data-ttu-id="48258-416">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-416">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-417">dragMode</span><span class="sxs-lookup"><span data-stu-id="48258-417">dragMode</span></span>  
<span data-ttu-id="48258-418">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-418">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-419">x</span><span class="sxs-lookup"><span data-stu-id="48258-419">x</span></span>  
<span data-ttu-id="48258-420">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-420">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-421">y</span><span class="sxs-lookup"><span data-stu-id="48258-421">y</span></span>  
<span data-ttu-id="48258-422">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-422">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="48258-423">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="48258-423">Return Value - dragOver</span></span>

<span data-ttu-id="48258-424">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="48258-424">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="48258-425">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="48258-425">Method dragOverEx</span></span>

<span data-ttu-id="48258-426">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-426">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="48258-427">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="48258-427">Parameters - dragOverEx</span></span>

<span data-ttu-id="48258-428">dragSource</span><span class="sxs-lookup"><span data-stu-id="48258-428">dragSource</span></span>  
<span data-ttu-id="48258-429">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-429">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-430">dragMode</span><span class="sxs-lookup"><span data-stu-id="48258-430">dragMode</span></span>  
<span data-ttu-id="48258-431">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-431">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-432">x</span><span class="sxs-lookup"><span data-stu-id="48258-432">x</span></span>  
<span data-ttu-id="48258-433">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-433">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-434">y</span><span class="sxs-lookup"><span data-stu-id="48258-434">y</span></span>  
<span data-ttu-id="48258-435">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-435">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="48258-436">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="48258-436">Return Value - dragOverEx</span></span>

<span data-ttu-id="48258-437">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="48258-437">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="48258-438">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="48258-438">Method dragText</span></span>

<span data-ttu-id="48258-439">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-439">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="48258-440">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="48258-440">Return Value - dragText</span></span>

<span data-ttu-id="48258-441">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="48258-441">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="48258-442">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="48258-442">Method enabled</span></span>

<span data-ttu-id="48258-443">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48258-443">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="48258-444">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="48258-444">Parameters - enabled</span></span>

<span data-ttu-id="48258-445">値</span><span class="sxs-lookup"><span data-stu-id="48258-445">value</span></span>  
<span data-ttu-id="48258-446">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-446">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="48258-447">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="48258-447">Return Value - enabled</span></span>

<span data-ttu-id="48258-448">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-448">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="48258-449">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="48258-449">Remarks - enabled</span></span>

<span data-ttu-id="48258-450">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="48258-450">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="48258-451">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="48258-451">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="48258-452">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="48258-452">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-error"></a><span data-ttu-id="48258-453">メソッド error</span><span class="sxs-lookup"><span data-stu-id="48258-453">Method error</span></span>

```xpp
public COMError error()
```

### <a name="return-value---error"></a><span data-ttu-id="48258-454">戻り値 - error</span><span class="sxs-lookup"><span data-stu-id="48258-454">Return Value - error</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="48258-455">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="48258-455">Method hasChanged</span></span>

<span data-ttu-id="48258-456">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-456">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="48258-457">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="48258-457">Parameters - hasChanged</span></span>

<span data-ttu-id="48258-458">val</span><span class="sxs-lookup"><span data-stu-id="48258-458">val</span></span>  
<span data-ttu-id="48258-459">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-459">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="48258-460">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="48258-460">Return Value - hasChanged</span></span>

<span data-ttu-id="48258-461">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-461">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="48258-462">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="48258-462">Method hasUserSetting</span></span>

<span data-ttu-id="48258-463">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48258-463">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="48258-464">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="48258-464">Return Value - hasUserSetting</span></span>

<span data-ttu-id="48258-465">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-465">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="48258-466">メソッド height</span><span class="sxs-lookup"><span data-stu-id="48258-466">Method height</span></span>

<span data-ttu-id="48258-467">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-467">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="48258-468">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="48258-468">Parameters - height</span></span>

<span data-ttu-id="48258-469">値</span><span class="sxs-lookup"><span data-stu-id="48258-469">value</span></span>  
<span data-ttu-id="48258-470">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="48258-470">An Integer data type that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="48258-471">モード</span><span class="sxs-lookup"><span data-stu-id="48258-471">mode</span></span>  
<span data-ttu-id="48258-472">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="48258-472">An Integer data type that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="48258-473">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="48258-473">Return Value - height</span></span>

<span data-ttu-id="48258-474">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="48258-474">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="48258-475">備考 - height</span><span class="sxs-lookup"><span data-stu-id="48258-475">Remarks - height</span></span>

<span data-ttu-id="48258-476">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48258-476">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="48258-477">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="48258-477">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="48258-478">モード。</span><span class="sxs-lookup"><span data-stu-id="48258-478">Mode.</span></span>            | <span data-ttu-id="48258-479">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="48258-479">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="48258-480">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="48258-480">-1 Exact.</span></span>        | <span data-ttu-id="48258-481">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48258-481">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="48258-482">0 自動。</span><span class="sxs-lookup"><span data-stu-id="48258-482">0 Auto.</span></span>          | <span data-ttu-id="48258-483">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="48258-483">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="48258-484">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="48258-484">1 Column height.</span></span> | <span data-ttu-id="48258-485">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="48258-485">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="48258-486">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="48258-486">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="48258-487">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="48258-487">Method heightMode</span></span>

<span data-ttu-id="48258-488">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-488">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="48258-489">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="48258-489">Parameters - heightMode</span></span>

<span data-ttu-id="48258-490">値</span><span class="sxs-lookup"><span data-stu-id="48258-490">value</span></span>  
<span data-ttu-id="48258-491">コントロールの高さの計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-491">An Integer data type value that indicates how the control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="48258-492">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="48258-492">Return Value - heightMode</span></span>

<span data-ttu-id="48258-493">計算モード。</span><span class="sxs-lookup"><span data-stu-id="48258-493">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="48258-494">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="48258-494">Remarks - heightMode</span></span>

<span data-ttu-id="48258-495">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="48258-495">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="48258-496">モード。</span><span class="sxs-lookup"><span data-stu-id="48258-496">Mode.</span></span>          | <span data-ttu-id="48258-497">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="48258-497">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="48258-498">正確。</span><span class="sxs-lookup"><span data-stu-id="48258-498">Exact.</span></span>         | <span data-ttu-id="48258-499">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48258-499">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="48258-500">自動。</span><span class="sxs-lookup"><span data-stu-id="48258-500">Auto.</span></span>          | <span data-ttu-id="48258-501">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="48258-501">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="48258-502">列の高さ</span><span class="sxs-lookup"><span data-stu-id="48258-502">Column height.</span></span> | <span data-ttu-id="48258-503">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="48258-503">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="48258-504">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="48258-504">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="48258-505">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="48258-505">Method heightValue</span></span>

<span data-ttu-id="48258-506">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-506">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="48258-507">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="48258-507">Parameters - heightValue</span></span>

<span data-ttu-id="48258-508">値</span><span class="sxs-lookup"><span data-stu-id="48258-508">value</span></span>  
<span data-ttu-id="48258-509">高さをピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-509">An Integer data type that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="48258-510">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="48258-510">Return Value - heightValue</span></span>

<span data-ttu-id="48258-511">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="48258-511">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="48258-512">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="48258-512">Remarks - heightValue</span></span>

<span data-ttu-id="48258-513">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="48258-513">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="48258-514">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="48258-514">Method helpField</span></span>

<span data-ttu-id="48258-515">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-515">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="48258-516">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="48258-516">Return Value - helpField</span></span>

<span data-ttu-id="48258-517">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="48258-517">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="48258-518">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="48258-518">Remarks - helpField</span></span>

<span data-ttu-id="48258-519">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="48258-519">The helpField method cannot be used to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="48258-520">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="48258-520">Method helpText</span></span>

<span data-ttu-id="48258-521">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-521">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="48258-522">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="48258-522">Parameters - helpText</span></span>

<span data-ttu-id="48258-523">値</span><span class="sxs-lookup"><span data-stu-id="48258-523">value</span></span>  
<span data-ttu-id="48258-524">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="48258-524">The value that is assigned as the help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="48258-525">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="48258-525">Return Value - helpText</span></span>

<span data-ttu-id="48258-526">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="48258-526">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="48258-527">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="48258-527">Remarks - helpText</span></span>

<span data-ttu-id="48258-528">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-528">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="48258-529">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="48258-529">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="48258-530">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="48258-530">Method hierarchyParent</span></span>

<span data-ttu-id="48258-531">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-531">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="48258-532">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="48258-532">Parameters - hierarchyParent</span></span>

<span data-ttu-id="48258-533">値</span><span class="sxs-lookup"><span data-stu-id="48258-533">value</span></span>  
<span data-ttu-id="48258-534">コントロールの HierarchyParent 値として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="48258-534">The value to assign as the HierarchyParent value of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="48258-535">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="48258-535">Return Value - hierarchyParent</span></span>

<span data-ttu-id="48258-536">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="48258-536">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="48258-537">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="48258-537">Method hWnd</span></span>

<span data-ttu-id="48258-538">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-538">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="48258-539">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="48258-539">Return Value - hWnd</span></span>

<span data-ttu-id="48258-540">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="48258-540">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="48258-541">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="48258-541">Remarks - hWnd</span></span>

<span data-ttu-id="48258-542">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="48258-542">The handle can be used with the Windows API.</span></span>

## <a name="method-interface"></a><span data-ttu-id="48258-543">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="48258-543">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="48258-544">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="48258-544">Return Value - interface</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="48258-545">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="48258-545">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="48258-546">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="48258-546">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="48258-547">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="48258-547">Method isDisplayed</span></span>

<span data-ttu-id="48258-548">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-548">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="48258-549">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="48258-549">Return Value - isDisplayed</span></span>

<span data-ttu-id="48258-550">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="48258-550">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="48258-551">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="48258-551">Remarks - isDisplayed</span></span>

<span data-ttu-id="48258-552">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="48258-552">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="48258-553">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="48258-553">Method isRestricted</span></span>

<span data-ttu-id="48258-554">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-554">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="48258-555">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="48258-555">Return Value - isRestricted</span></span>

<span data-ttu-id="48258-556">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="48258-556">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="48258-557">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="48258-557">Method isUserSetupEnabled</span></span>

<span data-ttu-id="48258-558">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="48258-558">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="48258-559">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="48258-559">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="48258-560">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="48258-560">neededSetupRights</span></span>  
<span data-ttu-id="48258-561">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="48258-561">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span> <span data-ttu-id="48258-562">詳細については、「備考」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="48258-562">For more information, see the �Remarks� section.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="48258-563">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="48258-563">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="48258-564">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-564">true if the control, design, and parent container allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="48258-565">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="48258-565">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="48258-566">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="48258-566">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                 |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48258-567">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="48258-567">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="48258-568">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="48258-568">No changes can be made to the control.</span></span> <span data-ttu-id="48258-569">neededSetupRights にこの値を使用すると、常に、true が返ってきます。</span><span class="sxs-lookup"><span data-stu-id="48258-569">Using this value for neededSetupRights always returns true.</span></span>                              |
| <span data-ttu-id="48258-570">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="48258-570">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="48258-571">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="48258-571">The user can change the editable, visible, skip, label and width properties of the control.</span></span> <span data-ttu-id="48258-572">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="48258-572">The user cannot move the control.</span></span>   |
| <span data-ttu-id="48258-573">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="48258-573">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="48258-574">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="48258-574">The user can change the editable, visible, skip, label and width properties of the control.</span></span> <span data-ttu-id="48258-575">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="48258-575">The user can also move the control.</span></span> |

<span data-ttu-id="48258-576">このメソッドは、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメーターで指定されたレベル以上の場合にのみ true を返します。</span><span class="sxs-lookup"><span data-stu-id="48258-576">This method returns true only if the AllowUserSetup property for the design and all parent containers is at least as high as the level that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-leave"></a><span data-ttu-id="48258-577">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="48258-577">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="48258-578">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="48258-578">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="48258-579">メソッド left</span><span class="sxs-lookup"><span data-stu-id="48258-579">Method left</span></span>

<span data-ttu-id="48258-580">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-580">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="48258-581">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="48258-581">Parameters - left</span></span>

<span data-ttu-id="48258-582">値</span><span class="sxs-lookup"><span data-stu-id="48258-582">value</span></span>  
<span data-ttu-id="48258-583">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-583">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="48258-584">モード</span><span class="sxs-lookup"><span data-stu-id="48258-584">mode</span></span>  
<span data-ttu-id="48258-585">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-585">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="48258-586">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="48258-586">Return Value - left</span></span>

<span data-ttu-id="48258-587">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="48258-587">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="48258-588">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="48258-588">Method leftMode</span></span>

<span data-ttu-id="48258-589">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-589">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="48258-590">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="48258-590">Parameters - leftMode</span></span>

<span data-ttu-id="48258-591">値</span><span class="sxs-lookup"><span data-stu-id="48258-591">value</span></span>  
<span data-ttu-id="48258-592">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-592">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="48258-593">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="48258-593">Return Value - leftMode</span></span>

<span data-ttu-id="48258-594">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="48258-594">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="48258-595">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="48258-595">Method leftValue</span></span>

<span data-ttu-id="48258-596">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-596">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="48258-597">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="48258-597">Parameters - leftValue</span></span>

<span data-ttu-id="48258-598">値</span><span class="sxs-lookup"><span data-stu-id="48258-598">value</span></span>  
<span data-ttu-id="48258-599">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-599">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="48258-600">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="48258-600">Return Value - leftValue</span></span>

<span data-ttu-id="48258-601">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="48258-601">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="48258-602">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="48258-602">Method markAsUserAdd</span></span>

<span data-ttu-id="48258-603">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="48258-603">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="48258-604">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="48258-604">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="48258-605">値</span><span class="sxs-lookup"><span data-stu-id="48258-605">value</span></span>  
<span data-ttu-id="48258-606">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-606">A Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="48258-607">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="48258-607">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="48258-608">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-608">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="48258-609">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48258-609">Method mouseDblClick</span></span>

<span data-ttu-id="48258-610">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-610">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="48258-611">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48258-611">Parameters - mouseDblClick</span></span>

<span data-ttu-id="48258-612">x</span><span class="sxs-lookup"><span data-stu-id="48258-612">x</span></span>  
<span data-ttu-id="48258-613">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-613">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-614">y</span><span class="sxs-lookup"><span data-stu-id="48258-614">y</span></span>  
<span data-ttu-id="48258-615">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-615">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-616">ボタン</span><span class="sxs-lookup"><span data-stu-id="48258-616">button</span></span>  
<span data-ttu-id="48258-617">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-617">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-618">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48258-618">Ctrl</span></span>  
<span data-ttu-id="48258-619">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-619">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-620">シフト</span><span class="sxs-lookup"><span data-stu-id="48258-620">Shift</span></span>  
<span data-ttu-id="48258-621">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-621">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="48258-622">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48258-622">Return Value - mouseDblClick</span></span>

<span data-ttu-id="48258-623">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48258-623">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="48258-624">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48258-624">Remarks - mouseDblClick</span></span>

<span data-ttu-id="48258-625">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="48258-625">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="48258-626">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="48258-626">Method mouseDown</span></span>

<span data-ttu-id="48258-627">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-627">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="48258-628">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="48258-628">Parameters - mouseDown</span></span>

<span data-ttu-id="48258-629">x</span><span class="sxs-lookup"><span data-stu-id="48258-629">x</span></span>  
<span data-ttu-id="48258-630">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-630">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-631">y</span><span class="sxs-lookup"><span data-stu-id="48258-631">y</span></span>  
<span data-ttu-id="48258-632">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-632">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-633">ボタン</span><span class="sxs-lookup"><span data-stu-id="48258-633">button</span></span>  
<span data-ttu-id="48258-634">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-634">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-635">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48258-635">Ctrl</span></span>  
<span data-ttu-id="48258-636">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-636">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-637">シフト</span><span class="sxs-lookup"><span data-stu-id="48258-637">Shift</span></span>  
<span data-ttu-id="48258-638">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-638">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="48258-639">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="48258-639">Return Value - mouseDown</span></span>

<span data-ttu-id="48258-640">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48258-640">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="48258-641">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="48258-641">Remarks - mouseDown</span></span>

<span data-ttu-id="48258-642">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="48258-642">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="48258-643">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-643">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="48258-644">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="48258-644">Method mouseMove</span></span>

<span data-ttu-id="48258-645">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-645">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="48258-646">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="48258-646">Parameters - mouseMove</span></span>

<span data-ttu-id="48258-647">x</span><span class="sxs-lookup"><span data-stu-id="48258-647">x</span></span>  
<span data-ttu-id="48258-648">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-648">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-649">y</span><span class="sxs-lookup"><span data-stu-id="48258-649">y</span></span>  
<span data-ttu-id="48258-650">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-650">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-651">ボタン</span><span class="sxs-lookup"><span data-stu-id="48258-651">button</span></span>  
<span data-ttu-id="48258-652">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-652">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-653">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48258-653">Ctrl</span></span>  
<span data-ttu-id="48258-654">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-654">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-655">シフト</span><span class="sxs-lookup"><span data-stu-id="48258-655">Shift</span></span>  
<span data-ttu-id="48258-656">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-656">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="48258-657">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="48258-657">Return Value - mouseMove</span></span>

<span data-ttu-id="48258-658">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48258-658">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="48258-659">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="48258-659">Remarks - mouseMove</span></span>

<span data-ttu-id="48258-660">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="48258-660">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="48258-661">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="48258-661">Method mouseUp</span></span>

<span data-ttu-id="48258-662">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-662">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="48258-663">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="48258-663">Parameters - mouseUp</span></span>

<span data-ttu-id="48258-664">x</span><span class="sxs-lookup"><span data-stu-id="48258-664">x</span></span>  
<span data-ttu-id="48258-665">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-665">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-666">y</span><span class="sxs-lookup"><span data-stu-id="48258-666">y</span></span>  
<span data-ttu-id="48258-667">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-667">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-668">ボタン</span><span class="sxs-lookup"><span data-stu-id="48258-668">button</span></span>  
<span data-ttu-id="48258-669">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-669">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-670">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48258-670">Ctrl</span></span>  
<span data-ttu-id="48258-671">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-671">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-672">シフト</span><span class="sxs-lookup"><span data-stu-id="48258-672">Shift</span></span>  
<span data-ttu-id="48258-673">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-673">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="48258-674">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="48258-674">Return Value - mouseUp</span></span>

<span data-ttu-id="48258-675">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48258-675">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="48258-676">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="48258-676">Remarks - mouseUp</span></span>

<span data-ttu-id="48258-677">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="48258-677">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="48258-678">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-678">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="48258-679">メソッド名</span><span class="sxs-lookup"><span data-stu-id="48258-679">Method name</span></span>

<span data-ttu-id="48258-680">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-680">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="48258-681">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="48258-681">Parameters - name</span></span>

<span data-ttu-id="48258-682">値</span><span class="sxs-lookup"><span data-stu-id="48258-682">value</span></span>  
<span data-ttu-id="48258-683">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-683">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="48258-684">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="48258-684">Return Value - name</span></span>

<span data-ttu-id="48258-685">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="48258-685">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="48258-686">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="48258-686">Remarks - name</span></span>

<span data-ttu-id="48258-687">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="48258-687">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="48258-688">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="48258-688">It must begin with a letter.</span></span>
-   <span data-ttu-id="48258-689">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="48258-689">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="48258-690">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="48258-690">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="48258-691">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="48258-691">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="48258-692">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="48258-692">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="48258-693">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="48258-693">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="48258-694">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="48258-694">Parameters - neededPermission</span></span>

<span data-ttu-id="48258-695">値</span><span class="sxs-lookup"><span data-stu-id="48258-695">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="48258-696">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="48258-696">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="48258-697">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48258-697">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="48258-698">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48258-698">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="48258-699">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="48258-699">Method parentControl</span></span>

<span data-ttu-id="48258-700">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-700">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="48258-701">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="48258-701">Return Value - parentControl</span></span>

<span data-ttu-id="48258-702">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="48258-702">The parent control for the control.</span></span>

## <a name="method-rtlcapable"></a><span data-ttu-id="48258-703">メソッド rTLCapable</span><span class="sxs-lookup"><span data-stu-id="48258-703">Method rTLCapable</span></span>

```xpp
public boolean rTLCapable([boolean value])
```

### <a name="parameters---rtlcapable"></a><span data-ttu-id="48258-704">パラメーター - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="48258-704">Parameters - rTLCapable</span></span>

<span data-ttu-id="48258-705">値</span><span class="sxs-lookup"><span data-stu-id="48258-705">value</span></span>  

### <a name="return-value---rtlcapable"></a><span data-ttu-id="48258-706">戻り値 - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="48258-706">Return Value - rTLCapable</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="48258-707">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="48258-707">Method securityKey</span></span>

<span data-ttu-id="48258-708">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-708">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="48258-709">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="48258-709">Parameters - securityKey</span></span>

<span data-ttu-id="48258-710">値</span><span class="sxs-lookup"><span data-stu-id="48258-710">value</span></span>  
<span data-ttu-id="48258-711">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-711">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="48258-712">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="48258-712">Return Value - securityKey</span></span>

<span data-ttu-id="48258-713">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="48258-713">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="48258-714">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="48258-714">Method showContextMenu</span></span>

<span data-ttu-id="48258-715">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="48258-715">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="48258-716">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="48258-716">Parameters - showContextMenu</span></span>

<span data-ttu-id="48258-717">menuHandle</span><span class="sxs-lookup"><span data-stu-id="48258-717">menuHandle</span></span>  
<span data-ttu-id="48258-718">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="48258-718">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="48258-719">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="48258-719">Return Value - showContextMenu</span></span>

<span data-ttu-id="48258-720">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-720">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="48258-721">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="48258-721">Method skip</span></span>

<span data-ttu-id="48258-722">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-722">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="48258-723">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="48258-723">Parameters - skip</span></span>

<span data-ttu-id="48258-724">値</span><span class="sxs-lookup"><span data-stu-id="48258-724">value</span></span>  
<span data-ttu-id="48258-725">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="48258-725">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="48258-726">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="48258-726">Return Value - skip</span></span>

<span data-ttu-id="48258-727">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48258-727">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="48258-728">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="48258-728">Method toolTip</span></span>

<span data-ttu-id="48258-729">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48258-729">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="48258-730">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="48258-730">Return Value - toolTip</span></span>

<span data-ttu-id="48258-731">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="48258-731">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="48258-732">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="48258-732">Remarks - toolTip</span></span>

<span data-ttu-id="48258-733">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="48258-733">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="48258-734">メソッド top</span><span class="sxs-lookup"><span data-stu-id="48258-734">Method top</span></span>

<span data-ttu-id="48258-735">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-735">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="48258-736">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="48258-736">Parameters - top</span></span>

<span data-ttu-id="48258-737">値</span><span class="sxs-lookup"><span data-stu-id="48258-737">value</span></span>  
<span data-ttu-id="48258-738">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-738">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="48258-739">モード</span><span class="sxs-lookup"><span data-stu-id="48258-739">mode</span></span>  
<span data-ttu-id="48258-740">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-740">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="48258-741">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="48258-741">Return Value - top</span></span>

<span data-ttu-id="48258-742">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="48258-742">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="48258-743">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="48258-743">Method topMode</span></span>

<span data-ttu-id="48258-744">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-744">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="48258-745">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="48258-745">Parameters - topMode</span></span>

<span data-ttu-id="48258-746">値</span><span class="sxs-lookup"><span data-stu-id="48258-746">value</span></span>  
<span data-ttu-id="48258-747">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-747">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="48258-748">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="48258-748">Return Value - topMode</span></span>

<span data-ttu-id="48258-749">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="48258-749">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="48258-750">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="48258-750">Method topValue</span></span>

<span data-ttu-id="48258-751">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-751">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="48258-752">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="48258-752">Parameters - topValue</span></span>

<span data-ttu-id="48258-753">値</span><span class="sxs-lookup"><span data-stu-id="48258-753">value</span></span>  
<span data-ttu-id="48258-754">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-754">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="48258-755">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="48258-755">Return Value - topValue</span></span>

<span data-ttu-id="48258-756">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="48258-756">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="48258-757">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="48258-757">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="48258-758">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="48258-758">Parameters - type</span></span>

<span data-ttu-id="48258-759">値</span><span class="sxs-lookup"><span data-stu-id="48258-759">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="48258-760">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="48258-760">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="48258-761">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48258-761">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="48258-762">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48258-762">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="48258-763">データ</span><span class="sxs-lookup"><span data-stu-id="48258-763">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="48258-764">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48258-764">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="48258-765">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="48258-765">Method userData</span></span>

<span data-ttu-id="48258-766">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-766">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="48258-767">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="48258-767">Parameters - userData</span></span>

<span data-ttu-id="48258-768">値</span><span class="sxs-lookup"><span data-stu-id="48258-768">value</span></span>  
<span data-ttu-id="48258-769">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-769">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="48258-770">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="48258-770">Return Value - userData</span></span>

<span data-ttu-id="48258-771">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="48258-771">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="48258-772">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="48258-772">Method userDataItem</span></span>

<span data-ttu-id="48258-773">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-773">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="48258-774">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="48258-774">Parameters - userDataItem</span></span>

<span data-ttu-id="48258-775">値</span><span class="sxs-lookup"><span data-stu-id="48258-775">value</span></span>  
<span data-ttu-id="48258-776">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-776">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="48258-777">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="48258-777">Return Value - userDataItem</span></span>

<span data-ttu-id="48258-778">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="48258-778">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="48258-779">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="48258-779">Method userDataItems</span></span>

<span data-ttu-id="48258-780">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-780">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="48258-781">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="48258-781">Parameters - userDataItems</span></span>

<span data-ttu-id="48258-782">値</span><span class="sxs-lookup"><span data-stu-id="48258-782">value</span></span>  
<span data-ttu-id="48258-783">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-783">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="48258-784">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="48258-784">Return Value - userDataItems</span></span>

<span data-ttu-id="48258-785">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="48258-785">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="48258-786">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="48258-786">Method userDisable</span></span>

<span data-ttu-id="48258-787">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-787">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="48258-788">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="48258-788">Parameters - userDisable</span></span>

<span data-ttu-id="48258-789">値</span><span class="sxs-lookup"><span data-stu-id="48258-789">value</span></span>  
<span data-ttu-id="48258-790">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-790">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="48258-791">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="48258-791">Return Value - userDisable</span></span>

<span data-ttu-id="48258-792">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="48258-792">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="48258-793">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="48258-793">Method userHeight</span></span>

<span data-ttu-id="48258-794">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-794">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="48258-795">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="48258-795">Parameters - userHeight</span></span>

<span data-ttu-id="48258-796">値</span><span class="sxs-lookup"><span data-stu-id="48258-796">value</span></span>  
<span data-ttu-id="48258-797">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-797">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="48258-798">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="48258-798">Return Value - userHeight</span></span>

<span data-ttu-id="48258-799">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="48258-799">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="48258-800">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="48258-800">Method userHide</span></span>

<span data-ttu-id="48258-801">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-801">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="48258-802">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="48258-802">Parameters - userHide</span></span>

<span data-ttu-id="48258-803">値</span><span class="sxs-lookup"><span data-stu-id="48258-803">value</span></span>  
<span data-ttu-id="48258-804">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-804">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="48258-805">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="48258-805">Return Value - userHide</span></span>

<span data-ttu-id="48258-806">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="48258-806">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="48258-807">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="48258-807">Remarks - userHide</span></span>

<span data-ttu-id="48258-808">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="48258-808">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="48258-809">右クリックすると、コントロールを非表示または表示できるメニューが起動します。</span><span class="sxs-lookup"><span data-stu-id="48258-809">Right-clicking invokes a menu that enables the control to be hidden or displayed.</span></span> <span data-ttu-id="48258-810">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="48258-810">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="48258-811">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="48258-811">Method userOrgContainer</span></span>

<span data-ttu-id="48258-812">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-812">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="48258-813">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="48258-813">Parameters - userOrgContainer</span></span>

<span data-ttu-id="48258-814">値</span><span class="sxs-lookup"><span data-stu-id="48258-814">value</span></span>  
<span data-ttu-id="48258-815">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-815">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="48258-816">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="48258-816">Return Value - userOrgContainer</span></span>

<span data-ttu-id="48258-817">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="48258-817">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="48258-818">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="48258-818">Method userOrgSibling</span></span>

<span data-ttu-id="48258-819">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-819">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="48258-820">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="48258-820">Parameters - userOrgSibling</span></span>

<span data-ttu-id="48258-821">値</span><span class="sxs-lookup"><span data-stu-id="48258-821">value</span></span>  
<span data-ttu-id="48258-822">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-822">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="48258-823">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="48258-823">Return Value - userOrgSibling</span></span>

<span data-ttu-id="48258-824">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="48258-824">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="48258-825">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="48258-825">Method userPromptText</span></span>

<span data-ttu-id="48258-826">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-826">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="48258-827">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="48258-827">Parameters - userPromptText</span></span>

<span data-ttu-id="48258-828">値</span><span class="sxs-lookup"><span data-stu-id="48258-828">value</span></span>  
<span data-ttu-id="48258-829">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-829">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="48258-830">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="48258-830">Return Value - userPromptText</span></span>

<span data-ttu-id="48258-831">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="48258-831">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="48258-832">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="48258-832">Method userSecurityLevel</span></span>

<span data-ttu-id="48258-833">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-833">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="48258-834">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="48258-834">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="48258-835">値</span><span class="sxs-lookup"><span data-stu-id="48258-835">value</span></span>  
<span data-ttu-id="48258-836">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-836">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="48258-837">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="48258-837">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="48258-838">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="48258-838">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="48258-839">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="48258-839">Method userSkip</span></span>

<span data-ttu-id="48258-840">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-840">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls on the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="48258-841">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="48258-841">Parameters - userSkip</span></span>

<span data-ttu-id="48258-842">値</span><span class="sxs-lookup"><span data-stu-id="48258-842">value</span></span>  
<span data-ttu-id="48258-843">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-843">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="48258-844">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="48258-844">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="48258-845">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="48258-845">Return Value - userSkip</span></span>

<span data-ttu-id="48258-846">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="48258-846">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="48258-847">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="48258-847">Method userWidth</span></span>

<span data-ttu-id="48258-848">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-848">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="48258-849">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="48258-849">Parameters - userWidth</span></span>

<span data-ttu-id="48258-850">値</span><span class="sxs-lookup"><span data-stu-id="48258-850">value</span></span>  
<span data-ttu-id="48258-851">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-851">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="48258-852">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="48258-852">Return Value - userWidth</span></span>

<span data-ttu-id="48258-853">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="48258-853">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="48258-854">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="48258-854">Remarks - userWidth</span></span>

<span data-ttu-id="48258-855">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="48258-855">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="48258-856">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻りは 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="48258-856">For example, if the user has specified 30 characters as the width for the control, the return is 6 \* 30 = 180.</span></span> <span data-ttu-id="48258-857">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="48258-857">To specify the width of the control in characters, users can right-click the control to invoke the setup form in which the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="48258-858">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="48258-858">Method verticalSpacing</span></span>

<span data-ttu-id="48258-859">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-859">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="48258-860">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="48258-860">Parameters - verticalSpacing</span></span>

<span data-ttu-id="48258-861">値</span><span class="sxs-lookup"><span data-stu-id="48258-861">value</span></span>  
<span data-ttu-id="48258-862">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-862">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="48258-863">モード</span><span class="sxs-lookup"><span data-stu-id="48258-863">mode</span></span>  
<span data-ttu-id="48258-864">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-864">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="48258-865">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="48258-865">Return Value - verticalSpacing</span></span>

<span data-ttu-id="48258-866">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="48258-866">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="48258-867">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="48258-867">Method verticalSpacingMode</span></span>

<span data-ttu-id="48258-868">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-868">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="48258-869">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="48258-869">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="48258-870">モード</span><span class="sxs-lookup"><span data-stu-id="48258-870">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="48258-871">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="48258-871">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="48258-872">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="48258-872">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="48258-873">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="48258-873">Method verticalSpacingValue</span></span>

<span data-ttu-id="48258-874">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-874">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="48258-875">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="48258-875">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="48258-876">値</span><span class="sxs-lookup"><span data-stu-id="48258-876">value</span></span>  
<span data-ttu-id="48258-877">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48258-877">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="48258-878">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="48258-878">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="48258-879">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="48258-879">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="48258-880">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="48258-880">Method visible</span></span>

<span data-ttu-id="48258-881">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48258-881">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="48258-882">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="48258-882">Parameters - visible</span></span>

<span data-ttu-id="48258-883">値</span><span class="sxs-lookup"><span data-stu-id="48258-883">value</span></span>  
<span data-ttu-id="48258-884">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-884">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="48258-885">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="48258-885">Return Value - visible</span></span>

<span data-ttu-id="48258-886">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="48258-886">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="48258-887">メソッド width</span><span class="sxs-lookup"><span data-stu-id="48258-887">Method width</span></span>

<span data-ttu-id="48258-888">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-888">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="48258-889">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="48258-889">Parameters - width</span></span>

<span data-ttu-id="48258-890">値</span><span class="sxs-lookup"><span data-stu-id="48258-890">value</span></span>  
<span data-ttu-id="48258-891">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="48258-891">An Integer data type that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="48258-892">モード</span><span class="sxs-lookup"><span data-stu-id="48258-892">mode</span></span>  
<span data-ttu-id="48258-893">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="48258-893">An Integer data type that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="48258-894">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="48258-894">Return Value - width</span></span>

<span data-ttu-id="48258-895">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="48258-895">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="48258-896">備考 - width</span><span class="sxs-lookup"><span data-stu-id="48258-896">Remarks - width</span></span>

<span data-ttu-id="48258-897">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48258-897">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="48258-898">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="48258-898">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="48258-899">モード。</span><span class="sxs-lookup"><span data-stu-id="48258-899">Mode.</span></span>           | <span data-ttu-id="48258-900">幅計算。</span><span class="sxs-lookup"><span data-stu-id="48258-900">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48258-901">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="48258-901">-1 Exact.</span></span>       | <span data-ttu-id="48258-902">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="48258-902">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="48258-903">0 自動。</span><span class="sxs-lookup"><span data-stu-id="48258-903">0 Auto.</span></span>         | <span data-ttu-id="48258-904">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="48258-904">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="48258-905">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="48258-905">1 Column width.</span></span> | <span data-ttu-id="48258-906">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="48258-906">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="48258-907">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="48258-907">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="48258-908">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="48258-908">Method widthMode</span></span>

<span data-ttu-id="48258-909">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-909">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="48258-910">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="48258-910">Parameters - widthMode</span></span>

<span data-ttu-id="48258-911">値</span><span class="sxs-lookup"><span data-stu-id="48258-911">value</span></span>  
<span data-ttu-id="48258-912">コントロールの幅の計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-912">An Integer data type value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="48258-913">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="48258-913">Return Value - widthMode</span></span>

<span data-ttu-id="48258-914">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-914">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="48258-915">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="48258-915">Remarks - widthMode</span></span>

<span data-ttu-id="48258-916">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="48258-916">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="48258-917">モード。</span><span class="sxs-lookup"><span data-stu-id="48258-917">Mode.</span></span>         | <span data-ttu-id="48258-918">幅計算。</span><span class="sxs-lookup"><span data-stu-id="48258-918">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48258-919">正確。</span><span class="sxs-lookup"><span data-stu-id="48258-919">Exact.</span></span>        | <span data-ttu-id="48258-920">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="48258-920">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="48258-921">自動。</span><span class="sxs-lookup"><span data-stu-id="48258-921">Auto.</span></span>         | <span data-ttu-id="48258-922">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="48258-922">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="48258-923">列の幅。</span><span class="sxs-lookup"><span data-stu-id="48258-923">Column width.</span></span> | <span data-ttu-id="48258-924">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="48258-924">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="48258-925">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="48258-925">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="48258-926">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="48258-926">Method widthValue</span></span>

<span data-ttu-id="48258-927">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-927">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="48258-928">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="48258-928">Parameters - widthValue</span></span>

<span data-ttu-id="48258-929">値</span><span class="sxs-lookup"><span data-stu-id="48258-929">value</span></span>  
<span data-ttu-id="48258-930">幅をピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-930">An Integer data type that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="48258-931">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="48258-931">Return Value - widthValue</span></span>

<span data-ttu-id="48258-932">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="48258-932">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="48258-933">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="48258-933">Remarks - widthValue</span></span>

<span data-ttu-id="48258-934">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="48258-934">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-inputsearch"></a><span data-ttu-id="48258-935">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="48258-935">Method inputSearch</span></span>

<span data-ttu-id="48258-936">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="48258-936">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="48258-937">パラメーター - inputSerach</span><span class="sxs-lookup"><span data-stu-id="48258-937">Parameters - inputSearch</span></span>

<span data-ttu-id="48258-938">searchStr</span><span class="sxs-lookup"><span data-stu-id="48258-938">searchStr</span></span>  
<span data-ttu-id="48258-939">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48258-939">The string value to use to filter data; optional.</span></span>

## <a name="method-copy"></a><span data-ttu-id="48258-940">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="48258-940">Method copy</span></span>

<span data-ttu-id="48258-941">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="48258-941">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-dragleave"></a><span data-ttu-id="48258-942">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="48258-942">Method dragLeave</span></span>

<span data-ttu-id="48258-943">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-943">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-drop"></a><span data-ttu-id="48258-944">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="48258-944">Method drop</span></span>

<span data-ttu-id="48258-945">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-945">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="48258-946">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="48258-946">Parameters - drop</span></span>

<span data-ttu-id="48258-947">dragSource</span><span class="sxs-lookup"><span data-stu-id="48258-947">dragSource</span></span>  
<span data-ttu-id="48258-948">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-948">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-949">dragMode</span><span class="sxs-lookup"><span data-stu-id="48258-949">dragMode</span></span>  
<span data-ttu-id="48258-950">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-950">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-951">x</span><span class="sxs-lookup"><span data-stu-id="48258-951">x</span></span>  
<span data-ttu-id="48258-952">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-952">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-953">y</span><span class="sxs-lookup"><span data-stu-id="48258-953">y</span></span>  
<span data-ttu-id="48258-954">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-954">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="48258-955">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="48258-955">Method mouseEnter</span></span>

<span data-ttu-id="48258-956">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-956">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="48258-957">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="48258-957">Parameters - mouseEnter</span></span>

<span data-ttu-id="48258-958">x</span><span class="sxs-lookup"><span data-stu-id="48258-958">x</span></span>  
<span data-ttu-id="48258-959">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-959">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-960">y</span><span class="sxs-lookup"><span data-stu-id="48258-960">y</span></span>  
<span data-ttu-id="48258-961">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-961">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-962">ボタン</span><span class="sxs-lookup"><span data-stu-id="48258-962">button</span></span>  
<span data-ttu-id="48258-963">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-963">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-964">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48258-964">Ctrl</span></span>  
<span data-ttu-id="48258-965">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-965">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48258-966">シフト</span><span class="sxs-lookup"><span data-stu-id="48258-966">Shift</span></span>  
<span data-ttu-id="48258-967">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48258-967">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="48258-968">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="48258-968">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="48258-969">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="48258-969">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="48258-970">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="48258-970">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="48258-971">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="48258-971">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="48258-972">overrideObject</span><span class="sxs-lookup"><span data-stu-id="48258-972">overrideObject</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="48258-973">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="48258-973">Method resetUserSetting</span></span>

<span data-ttu-id="48258-974">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="48258-974">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-context"></a><span data-ttu-id="48258-975">メソッド context</span><span class="sxs-lookup"><span data-stu-id="48258-975">Method context</span></span>

<span data-ttu-id="48258-976">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="48258-976">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enter"></a><span data-ttu-id="48258-977">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="48258-977">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="48258-978">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="48258-978">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="48258-979">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="48258-979">Parameters - OnGotFocus</span></span>

<span data-ttu-id="48258-980">sender</span><span class="sxs-lookup"><span data-stu-id="48258-980">sender</span></span>  

<!-- -->

<span data-ttu-id="48258-981">e</span><span class="sxs-lookup"><span data-stu-id="48258-981">e</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="48258-982">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="48258-982">Method displayControl</span></span>

<span data-ttu-id="48258-983">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="48258-983">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-updatesize"></a><span data-ttu-id="48258-984">メソッド updateSize</span><span class="sxs-lookup"><span data-stu-id="48258-984">Method updateSize</span></span>

```xpp
public void updateSize()
```

## <a name="method-gotfocus"></a><span data-ttu-id="48258-985">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="48258-985">Method gotFocus</span></span>

<span data-ttu-id="48258-986">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="48258-986">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-mouseleave"></a><span data-ttu-id="48258-987">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="48258-987">Method mouseLeave</span></span>

<span data-ttu-id="48258-988">ユーザーがマウス ポインターをコントロール エリアから移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-988">Is called when the user moves the mouse pointer out of the control area.</span></span>

```xpp
public void mouseLeave()
```

### <a name="examples---mouseleave"></a><span data-ttu-id="48258-989">例 - mouseLeave</span><span class="sxs-lookup"><span data-stu-id="48258-989">Examples - mouseLeave</span></span>

<span data-ttu-id="48258-990">次の例では、マウス ポインタがコントロールを離れるときに情報ログに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="48258-990">The following example writes to the information log when the mouse pointer leaves the control.</span></span>

```xpp
public void mouseLeave() 
{ 
    info (strfmt("The mouse pointer has left the %1 control.", 
                 this.name()) ); 
    super(); 
}
```

## <a name="method-dropex"></a><span data-ttu-id="48258-991">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="48258-991">Method dropEx</span></span>

<span data-ttu-id="48258-992">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48258-992">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="48258-993">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="48258-993">Parameters - dropEx</span></span>

<span data-ttu-id="48258-994">dragSource</span><span class="sxs-lookup"><span data-stu-id="48258-994">dragSource</span></span>  
<span data-ttu-id="48258-995">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-995">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-996">dragMode</span><span class="sxs-lookup"><span data-stu-id="48258-996">dragMode</span></span>  
<span data-ttu-id="48258-997">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-997">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-998">x</span><span class="sxs-lookup"><span data-stu-id="48258-998">x</span></span>  
<span data-ttu-id="48258-999">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-999">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48258-1000">y</span><span class="sxs-lookup"><span data-stu-id="48258-1000">y</span></span>  
<span data-ttu-id="48258-1001">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48258-1001">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="48258-1002">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="48258-1002">Method endDrag</span></span>

<span data-ttu-id="48258-1003">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48258-1003">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="48258-1004">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="48258-1004">Remarks - endDrag</span></span>

<span data-ttu-id="48258-1005">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="48258-1005">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="48258-1006">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="48258-1006">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-cut"></a><span data-ttu-id="48258-1007">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="48258-1007">Method cut</span></span>

<span data-ttu-id="48258-1008">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="48258-1008">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-paste"></a><span data-ttu-id="48258-1009">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="48258-1009">Method paste</span></span>

<span data-ttu-id="48258-1010">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="48258-1010">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-onleaving"></a><span data-ttu-id="48258-1011">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="48258-1011">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="48258-1012">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="48258-1012">Parameters - OnLeaving</span></span>

<span data-ttu-id="48258-1013">sender</span><span class="sxs-lookup"><span data-stu-id="48258-1013">sender</span></span>  

<!-- -->

<span data-ttu-id="48258-1014">e</span><span class="sxs-lookup"><span data-stu-id="48258-1014">e</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="48258-1015">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="48258-1015">Method prefColumnSize</span></span>

<span data-ttu-id="48258-1016">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="48258-1016">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="48258-1017">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="48258-1017">Parameters - prefColumnSize</span></span>

<span data-ttu-id="48258-1018">width</span><span class="sxs-lookup"><span data-stu-id="48258-1018">width</span></span>  
<span data-ttu-id="48258-1019">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="48258-1019">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="48258-1020">height</span><span class="sxs-lookup"><span data-stu-id="48258-1020">height</span></span>  
<span data-ttu-id="48258-1021">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="48258-1021">The preferred height of the control.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="48258-1022">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="48258-1022">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="48258-1023">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="48258-1023">Parameters - OnLostFocus</span></span>

<span data-ttu-id="48258-1024">sender</span><span class="sxs-lookup"><span data-stu-id="48258-1024">sender</span></span>  

<!-- -->

<span data-ttu-id="48258-1025">e</span><span class="sxs-lookup"><span data-stu-id="48258-1025">e</span></span>  

## <a name="method-onenter"></a><span data-ttu-id="48258-1026">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="48258-1026">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="48258-1027">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="48258-1027">Parameters - OnEnter</span></span>

<span data-ttu-id="48258-1028">sender</span><span class="sxs-lookup"><span data-stu-id="48258-1028">sender</span></span>  

<!-- -->

<span data-ttu-id="48258-1029">e</span><span class="sxs-lookup"><span data-stu-id="48258-1029">e</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="48258-1030">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="48258-1030">Method setFocus</span></span>

<span data-ttu-id="48258-1031">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="48258-1031">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-lostfocus"></a><span data-ttu-id="48258-1032">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="48258-1032">Method lostFocus</span></span>

<span data-ttu-id="48258-1033">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="48258-1033">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

