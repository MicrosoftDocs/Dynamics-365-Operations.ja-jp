---
title: FormManagedHostControl クラス
description: このトピックでは、FormManagedHostControl クラスについて説明します。
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
ms.openlocfilehash: 26c3cd66937b7ca4c117943ac2c54d05d651e752
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502930"
---
# <a name="class-formmanagedhostcontrol"></a><span data-ttu-id="0219c-103">クラス FormManagedHostControl</span><span class="sxs-lookup"><span data-stu-id="0219c-103">Class FormManagedHostControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormManagedHostControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="0219c-104">備考</span><span class="sxs-lookup"><span data-stu-id="0219c-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="0219c-105">例</span><span class="sxs-lookup"><span data-stu-id="0219c-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="0219c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="0219c-106">Methods</span></span>

| <span data-ttu-id="0219c-107">方法</span><span class="sxs-lookup"><span data-stu-id="0219c-107">Method</span></span>                                                                                                      | <span data-ttu-id="0219c-108">説明</span><span class="sxs-lookup"><span data-stu-id="0219c-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0219c-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="0219c-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="0219c-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="0219c-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="0219c-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="0219c-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="0219c-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="0219c-115">public str assemblyName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-115">public str assemblyName(\[str value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="0219c-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="0219c-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="0219c-118">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="0219c-118">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="0219c-119">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-119">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="0219c-120">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="0219c-120">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="0219c-121">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-121">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="0219c-122">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-122">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="0219c-123">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-123">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="0219c-124">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="0219c-124">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="0219c-125">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-125">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="0219c-126">public CLRObject control()</span><span class="sxs-lookup"><span data-stu-id="0219c-126">public CLRObject control()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="0219c-127">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-127">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="0219c-128">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-128">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="0219c-129">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-129">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="0219c-130">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-130">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="0219c-131">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-131">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="0219c-132">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-132">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="0219c-133">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-133">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="0219c-134">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-134">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="0219c-135">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="0219c-135">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="0219c-136">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-136">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="0219c-137">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="0219c-137">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="0219c-138">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-138">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="0219c-139">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="0219c-139">public str dragText()</span></span>                                                                                       | <span data-ttu-id="0219c-140">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-140">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="0219c-141">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-141">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="0219c-142">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-142">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="0219c-143">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="0219c-143">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="0219c-144">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-144">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="0219c-145">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="0219c-145">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="0219c-146">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-146">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="0219c-147">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0219c-147">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="0219c-148">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-148">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="0219c-149">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-149">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="0219c-150">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-150">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="0219c-151">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-151">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="0219c-152">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-152">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="0219c-153">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="0219c-153">public str helpField()</span></span>                                                                                      | <span data-ttu-id="0219c-154">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-154">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="0219c-155">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-155">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="0219c-156">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-156">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="0219c-157">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-157">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="0219c-158">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-158">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="0219c-159">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-159">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="0219c-160">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="0219c-160">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="0219c-161">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-161">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="0219c-162">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="0219c-162">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="0219c-163">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="0219c-163">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="0219c-164">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-164">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="0219c-165">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="0219c-165">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="0219c-166">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-166">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="0219c-167">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="0219c-167">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="0219c-168">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-168">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="0219c-169">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="0219c-169">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="0219c-170">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0219c-170">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="0219c-171">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-171">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="0219c-172">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-172">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="0219c-173">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-173">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="0219c-174">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-174">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="0219c-175">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-175">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="0219c-176">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-176">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="0219c-177">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="0219c-177">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="0219c-178">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="0219c-178">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="0219c-179">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-179">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="0219c-180">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="0219c-180">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="0219c-181">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-181">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="0219c-182">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="0219c-182">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="0219c-183">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-183">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="0219c-184">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="0219c-184">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="0219c-185">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-185">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="0219c-186">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-186">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="0219c-187">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-187">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="0219c-188">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-188">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="0219c-189">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="0219c-189">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="0219c-190">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="0219c-190">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="0219c-191">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-191">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="0219c-192">public boolean rTLCapable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-192">public boolean rTLCapable(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="0219c-193">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-193">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="0219c-194">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-194">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="0219c-195">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="0219c-195">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="0219c-196">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-196">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="0219c-197">public int sizing(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-197">public int sizing(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="0219c-198">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-198">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="0219c-199">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-199">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="0219c-200">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="0219c-200">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="0219c-201">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-201">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="0219c-202">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0219c-202">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="0219c-203">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-203">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="0219c-204">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-204">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="0219c-205">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-205">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="0219c-206">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-206">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="0219c-207">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-207">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="0219c-208">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-208">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="0219c-209">public str typeName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-209">public str typeName(\[str value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="0219c-210">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="0219c-210">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="0219c-211">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-211">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="0219c-212">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-212">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="0219c-213">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-213">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="0219c-214">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-214">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="0219c-215">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-215">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="0219c-216">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-216">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="0219c-217">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-217">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="0219c-218">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-218">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="0219c-219">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-219">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="0219c-220">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-220">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="0219c-221">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-221">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="0219c-222">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-222">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="0219c-223">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-223">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="0219c-224">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-224">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="0219c-225">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-225">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="0219c-226">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-226">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="0219c-227">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-227">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="0219c-228">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-228">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="0219c-229">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-229">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="0219c-230">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-230">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="0219c-231">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-231">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="0219c-232">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-232">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="0219c-233">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-233">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="0219c-234">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-234">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="0219c-235">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0219c-235">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="0219c-236">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-236">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="0219c-237">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0219c-237">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="0219c-238">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-238">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="0219c-239">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-239">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="0219c-240">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-240">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="0219c-241">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-241">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="0219c-242">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-242">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="0219c-243">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0219c-243">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="0219c-244">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-244">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="0219c-245">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-245">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="0219c-246">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-246">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="0219c-247">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0219c-247">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="0219c-248">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-248">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="0219c-249">public void enter()</span><span class="sxs-lookup"><span data-stu-id="0219c-249">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="0219c-250">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="0219c-250">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="0219c-251">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="0219c-251">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="0219c-252">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-252">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="0219c-253">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="0219c-253">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="0219c-254">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-254">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="0219c-255">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="0219c-255">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="0219c-256">public void paste()</span><span class="sxs-lookup"><span data-stu-id="0219c-256">public void paste()</span></span>                                                                                         | <span data-ttu-id="0219c-257">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="0219c-257">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="0219c-258">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="0219c-258">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="0219c-259">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-259">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="0219c-260">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="0219c-260">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="0219c-261">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-261">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="0219c-262">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="0219c-262">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="0219c-263">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="0219c-263">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="0219c-264">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="0219c-264">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="0219c-265">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-265">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="0219c-266">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="0219c-266">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="0219c-267">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="0219c-267">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="0219c-268">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-268">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="0219c-269">public void copy()</span><span class="sxs-lookup"><span data-stu-id="0219c-269">public void copy()</span></span>                                                                                          | <span data-ttu-id="0219c-270">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0219c-270">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="0219c-271">public void cut()</span><span class="sxs-lookup"><span data-stu-id="0219c-271">public void cut()</span></span>                                                                                           | <span data-ttu-id="0219c-272">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="0219c-272">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="0219c-273">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="0219c-273">public void displayControl()</span></span>                                                                                | <span data-ttu-id="0219c-274">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-274">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="0219c-275">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="0219c-275">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="0219c-276">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-276">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="0219c-277">public void context()</span><span class="sxs-lookup"><span data-stu-id="0219c-277">public void context()</span></span>                                                                                       | <span data-ttu-id="0219c-278">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-278">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="0219c-279">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="0219c-279">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="0219c-280">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="0219c-280">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="0219c-281">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="0219c-281">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="0219c-282">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="0219c-282">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="0219c-283">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="0219c-283">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="0219c-284">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-284">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="0219c-285">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="0219c-285">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="0219c-286">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-286">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="0219c-287">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="0219c-287">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="0219c-288">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-288">Sets the focus on the control.</span></span>                                                                                                                                          |

## <a name="method-aligncontrol"></a><span data-ttu-id="0219c-289">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="0219c-289">Method alignControl</span></span>

<span data-ttu-id="0219c-290">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-290">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="0219c-291">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="0219c-291">Parameters - alignControl</span></span>

<span data-ttu-id="0219c-292">値</span><span class="sxs-lookup"><span data-stu-id="0219c-292">value</span></span>  
<span data-ttu-id="0219c-293">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-293">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="0219c-294">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="0219c-294">Return Value - alignControl</span></span>

<span data-ttu-id="0219c-295">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="0219c-295">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="0219c-296">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="0219c-296">Remarks - alignControl</span></span>

<span data-ttu-id="0219c-297">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-297">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="0219c-298">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="0219c-298">Method allowEdit</span></span>

<span data-ttu-id="0219c-299">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-299">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="0219c-300">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0219c-300">Parameters - allowEdit</span></span>

<span data-ttu-id="0219c-301">値</span><span class="sxs-lookup"><span data-stu-id="0219c-301">value</span></span>  
<span data-ttu-id="0219c-302">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="0219c-302">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="0219c-303">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0219c-303">Return Value - allowEdit</span></span>

<span data-ttu-id="0219c-304">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-304">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="0219c-305">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0219c-305">Remarks - allowEdit</span></span>

<span data-ttu-id="0219c-306">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="0219c-306">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="0219c-307">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="0219c-307">Method allowSysSetup</span></span>

<span data-ttu-id="0219c-308">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-308">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="0219c-309">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="0219c-309">Return Value - allowSysSetup</span></span>

<span data-ttu-id="0219c-310">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-310">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-assemblyname"></a><span data-ttu-id="0219c-311">メソッド assemblyName</span><span class="sxs-lookup"><span data-stu-id="0219c-311">Method assemblyName</span></span>

```xpp
public str assemblyName([str value])
```

### <a name="parameters---assemblyname"></a><span data-ttu-id="0219c-312">パラメーター - assemblyName</span><span class="sxs-lookup"><span data-stu-id="0219c-312">Parameters - assemblyName</span></span>

<span data-ttu-id="0219c-313">値</span><span class="sxs-lookup"><span data-stu-id="0219c-313">value</span></span>  

### <a name="return-value---assemblyname"></a><span data-ttu-id="0219c-314">戻り値 - assemblyName</span><span class="sxs-lookup"><span data-stu-id="0219c-314">Return Value - assemblyName</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="0219c-315">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0219c-315">Method autoDeclaration</span></span>

<span data-ttu-id="0219c-316">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-316">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="0219c-317">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0219c-317">Parameters - autoDeclaration</span></span>

<span data-ttu-id="0219c-318">値</span><span class="sxs-lookup"><span data-stu-id="0219c-318">value</span></span>  
<span data-ttu-id="0219c-319">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-319">The new value for the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="0219c-320">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0219c-320">Return Value - autoDeclaration</span></span>

<span data-ttu-id="0219c-321">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-321">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="0219c-322">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0219c-322">Remarks - autoDeclaration</span></span>

<span data-ttu-id="0219c-323">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="0219c-323">Controls cannot have identical names.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="0219c-324">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="0219c-324">Method beginDrag</span></span>

<span data-ttu-id="0219c-325">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-325">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="0219c-326">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="0219c-326">Parameters - beginDrag</span></span>

<span data-ttu-id="0219c-327">x</span><span class="sxs-lookup"><span data-stu-id="0219c-327">x</span></span>  
<span data-ttu-id="0219c-328">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-328">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="0219c-329">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="0219c-329">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="0219c-330">y</span><span class="sxs-lookup"><span data-stu-id="0219c-330">y</span></span>  
<span data-ttu-id="0219c-331">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-331">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="0219c-332">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="0219c-332">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="0219c-333">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="0219c-333">Return Value - beginDrag</span></span>

<span data-ttu-id="0219c-334">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0219c-334">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="0219c-335">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="0219c-335">Remarks - beginDrag</span></span>

<span data-ttu-id="0219c-336">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="0219c-336">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="0219c-337">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="0219c-337">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="0219c-338">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="0219c-338">Method calcControlSize</span></span>

<span data-ttu-id="0219c-339">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-339">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="0219c-340">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="0219c-340">Parameters - calcControlSize</span></span>

<span data-ttu-id="0219c-341">chars</span><span class="sxs-lookup"><span data-stu-id="0219c-341">chars</span></span>  
<span data-ttu-id="0219c-342">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="0219c-342">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="0219c-343">明細行</span><span class="sxs-lookup"><span data-stu-id="0219c-343">lines</span></span>  
<span data-ttu-id="0219c-344">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="0219c-344">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="0219c-345">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="0219c-345">Return Value - calcControlSize</span></span>

<span data-ttu-id="0219c-346">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="0219c-346">The container that holds the width and height.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="0219c-347">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="0219c-347">Method configurationKey</span></span>

<span data-ttu-id="0219c-348">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-348">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="0219c-349">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0219c-349">Parameters - configurationKey</span></span>

<span data-ttu-id="0219c-350">値</span><span class="sxs-lookup"><span data-stu-id="0219c-350">value</span></span>  
<span data-ttu-id="0219c-351">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-351">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="0219c-352">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0219c-352">Return Value - configurationKey</span></span>

<span data-ttu-id="0219c-353">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="0219c-353">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="0219c-354">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0219c-354">Remarks - configurationKey</span></span>

<span data-ttu-id="0219c-355">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-355">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="0219c-356">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="0219c-356">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="0219c-357">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="0219c-357">Method configurationKeyEx</span></span>

<span data-ttu-id="0219c-358">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-358">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="0219c-359">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="0219c-359">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="0219c-360">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="0219c-360">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="0219c-361">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="0219c-361">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="0219c-362">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="0219c-362">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="0219c-363">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="0219c-363">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="0219c-364">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0219c-364">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-control"></a><span data-ttu-id="0219c-365">メソッド control</span><span class="sxs-lookup"><span data-stu-id="0219c-365">Method control</span></span>

```xpp
public CLRObject control()
```

### <a name="return-value---control"></a><span data-ttu-id="0219c-366">戻り値 - control</span><span class="sxs-lookup"><span data-stu-id="0219c-366">Return Value - control</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="0219c-367">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0219c-367">Method countryRegionCodes</span></span>

<span data-ttu-id="0219c-368">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-368">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="0219c-369">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0219c-369">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="0219c-370">値</span><span class="sxs-lookup"><span data-stu-id="0219c-370">value</span></span>  
<span data-ttu-id="0219c-371">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-371">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="0219c-372">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0219c-372">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="0219c-373">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="0219c-373">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="0219c-374">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0219c-374">Method dataRelationPath</span></span>

<span data-ttu-id="0219c-375">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-375">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="0219c-376">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0219c-376">Parameters - dataRelationPath</span></span>

<span data-ttu-id="0219c-377">値</span><span class="sxs-lookup"><span data-stu-id="0219c-377">value</span></span>  
<span data-ttu-id="0219c-378">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-378">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="0219c-379">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0219c-379">Return Value - dataRelationPath</span></span>

<span data-ttu-id="0219c-380">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="0219c-380">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="0219c-381">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0219c-381">Remarks - dataRelationPath</span></span>

<span data-ttu-id="0219c-382">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="0219c-382">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="0219c-383">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="0219c-383">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="0219c-384">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="0219c-384">Method displayTarget</span></span>

<span data-ttu-id="0219c-385">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-385">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="0219c-386">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="0219c-386">Parameters - displayTarget</span></span>

<span data-ttu-id="0219c-387">値</span><span class="sxs-lookup"><span data-stu-id="0219c-387">value</span></span>  
<span data-ttu-id="0219c-388">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-388">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="0219c-389">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="0219c-389">Return Value - displayTarget</span></span>

<span data-ttu-id="0219c-390">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="0219c-390">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="0219c-391">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="0219c-391">Method dragDrop</span></span>

<span data-ttu-id="0219c-392">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-392">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="0219c-393">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0219c-393">Parameters - dragDrop</span></span>

<span data-ttu-id="0219c-394">値</span><span class="sxs-lookup"><span data-stu-id="0219c-394">value</span></span>  
<span data-ttu-id="0219c-395">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-395">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="0219c-396">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0219c-396">Return Value - dragDrop</span></span>

<span data-ttu-id="0219c-397">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="0219c-397">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="0219c-398">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0219c-398">Remarks - dragDrop</span></span>

<span data-ttu-id="0219c-399">FormControl.dragLeave、FormControl.dragOver、および FormControl.dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-399">Use the FormControl.dragLeave, FormControl.dragOver, and the FormControl.dragOverEx methods to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="0219c-400">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="0219c-400">Method dragOver</span></span>

<span data-ttu-id="0219c-401">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-401">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="0219c-402">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="0219c-402">Parameters - dragOver</span></span>

<span data-ttu-id="0219c-403">dragSource</span><span class="sxs-lookup"><span data-stu-id="0219c-403">dragSource</span></span>  
<span data-ttu-id="0219c-404">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-404">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-405">dragMode</span><span class="sxs-lookup"><span data-stu-id="0219c-405">dragMode</span></span>  
<span data-ttu-id="0219c-406">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-406">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-407">x</span><span class="sxs-lookup"><span data-stu-id="0219c-407">x</span></span>  
<span data-ttu-id="0219c-408">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-408">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-409">y</span><span class="sxs-lookup"><span data-stu-id="0219c-409">y</span></span>  
<span data-ttu-id="0219c-410">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-410">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="0219c-411">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="0219c-411">Return Value - dragOver</span></span>

<span data-ttu-id="0219c-412">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="0219c-412">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="0219c-413">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="0219c-413">Method dragOverEx</span></span>

<span data-ttu-id="0219c-414">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-414">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="0219c-415">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="0219c-415">Parameters - dragOverEx</span></span>

<span data-ttu-id="0219c-416">dragSource</span><span class="sxs-lookup"><span data-stu-id="0219c-416">dragSource</span></span>  
<span data-ttu-id="0219c-417">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-417">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-418">dragMode</span><span class="sxs-lookup"><span data-stu-id="0219c-418">dragMode</span></span>  
<span data-ttu-id="0219c-419">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-419">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-420">x</span><span class="sxs-lookup"><span data-stu-id="0219c-420">x</span></span>  
<span data-ttu-id="0219c-421">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-421">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-422">y</span><span class="sxs-lookup"><span data-stu-id="0219c-422">y</span></span>  
<span data-ttu-id="0219c-423">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-423">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="0219c-424">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="0219c-424">Return Value - dragOverEx</span></span>

<span data-ttu-id="0219c-425">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="0219c-425">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="0219c-426">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="0219c-426">Method dragText</span></span>

<span data-ttu-id="0219c-427">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-427">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="0219c-428">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="0219c-428">Return Value - dragText</span></span>

<span data-ttu-id="0219c-429">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="0219c-429">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="0219c-430">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="0219c-430">Method enabled</span></span>

<span data-ttu-id="0219c-431">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-431">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="0219c-432">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="0219c-432">Parameters - enabled</span></span>

<span data-ttu-id="0219c-433">値</span><span class="sxs-lookup"><span data-stu-id="0219c-433">value</span></span>  
<span data-ttu-id="0219c-434">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-434">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="0219c-435">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="0219c-435">Return Value - enabled</span></span>

<span data-ttu-id="0219c-436">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-436">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="0219c-437">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="0219c-437">Remarks - enabled</span></span>

<span data-ttu-id="0219c-438">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="0219c-438">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="0219c-439">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="0219c-439">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="0219c-440">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0219c-440">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="0219c-441">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="0219c-441">Method hasChanged</span></span>

<span data-ttu-id="0219c-442">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-442">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="0219c-443">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="0219c-443">Parameters - hasChanged</span></span>

<span data-ttu-id="0219c-444">val</span><span class="sxs-lookup"><span data-stu-id="0219c-444">val</span></span>  
<span data-ttu-id="0219c-445">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-445">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="0219c-446">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="0219c-446">Return Value - hasChanged</span></span>

<span data-ttu-id="0219c-447">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-447">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="0219c-448">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="0219c-448">Method hasUserSetting</span></span>

<span data-ttu-id="0219c-449">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-449">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="0219c-450">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="0219c-450">Return Value - hasUserSetting</span></span>

<span data-ttu-id="0219c-451">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-451">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="0219c-452">メソッド height</span><span class="sxs-lookup"><span data-stu-id="0219c-452">Method height</span></span>

<span data-ttu-id="0219c-453">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-453">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="0219c-454">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="0219c-454">Parameters - height</span></span>

<span data-ttu-id="0219c-455">値</span><span class="sxs-lookup"><span data-stu-id="0219c-455">value</span></span>  
<span data-ttu-id="0219c-456">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-456">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="0219c-457">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-457">mode</span></span>  
<span data-ttu-id="0219c-458">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-458">An Integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="0219c-459">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="0219c-459">Return Value - height</span></span>

<span data-ttu-id="0219c-460">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="0219c-460">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="0219c-461">備考 - height</span><span class="sxs-lookup"><span data-stu-id="0219c-461">Remarks - height</span></span>

<span data-ttu-id="0219c-462">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-462">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="0219c-463">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="0219c-463">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="0219c-464">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-464">Mode</span></span>            | <span data-ttu-id="0219c-465">高さの計算</span><span class="sxs-lookup"><span data-stu-id="0219c-465">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0219c-466">-1 正確</span><span class="sxs-lookup"><span data-stu-id="0219c-466">-1 Exact</span></span>        | <span data-ttu-id="0219c-467">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-467">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0219c-468">0 自動</span><span class="sxs-lookup"><span data-stu-id="0219c-468">0 Auto</span></span>          | <span data-ttu-id="0219c-469">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-469">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0219c-470">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="0219c-470">1 Column height</span></span> | <span data-ttu-id="0219c-471">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="0219c-471">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="0219c-472">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0219c-472">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="0219c-473">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="0219c-473">Method heightMode</span></span>

<span data-ttu-id="0219c-474">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-474">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="0219c-475">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="0219c-475">Parameters - heightMode</span></span>

<span data-ttu-id="0219c-476">値</span><span class="sxs-lookup"><span data-stu-id="0219c-476">value</span></span>  
<span data-ttu-id="0219c-477">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-477">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="0219c-478">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="0219c-478">Return Value - heightMode</span></span>

<span data-ttu-id="0219c-479">計算モード。</span><span class="sxs-lookup"><span data-stu-id="0219c-479">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="0219c-480">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="0219c-480">Remarks - heightMode</span></span>

<span data-ttu-id="0219c-481">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="0219c-481">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="0219c-482">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-482">Mode</span></span>          | <span data-ttu-id="0219c-483">高さの計算</span><span class="sxs-lookup"><span data-stu-id="0219c-483">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0219c-484">正確</span><span class="sxs-lookup"><span data-stu-id="0219c-484">Exact</span></span>         | <span data-ttu-id="0219c-485">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-485">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0219c-486">自動</span><span class="sxs-lookup"><span data-stu-id="0219c-486">Auto</span></span>          | <span data-ttu-id="0219c-487">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-487">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0219c-488">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="0219c-488">Column height</span></span> | <span data-ttu-id="0219c-489">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="0219c-489">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="0219c-490">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0219c-490">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="0219c-491">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="0219c-491">Method heightValue</span></span>

<span data-ttu-id="0219c-492">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-492">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="0219c-493">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="0219c-493">Parameters - heightValue</span></span>

<span data-ttu-id="0219c-494">値</span><span class="sxs-lookup"><span data-stu-id="0219c-494">value</span></span>  
<span data-ttu-id="0219c-495">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-495">An Integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="0219c-496">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="0219c-496">Return Value - heightValue</span></span>

<span data-ttu-id="0219c-497">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="0219c-497">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="0219c-498">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="0219c-498">Remarks - heightValue</span></span>

<span data-ttu-id="0219c-499">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="0219c-499">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="0219c-500">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="0219c-500">Method helpField</span></span>

<span data-ttu-id="0219c-501">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-501">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="0219c-502">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="0219c-502">Return Value - helpField</span></span>

<span data-ttu-id="0219c-503">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="0219c-503">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="0219c-504">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="0219c-504">Remarks - helpField</span></span>

<span data-ttu-id="0219c-505">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="0219c-505">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="0219c-506">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0219c-506">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="0219c-507">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="0219c-507">Method helpText</span></span>

<span data-ttu-id="0219c-508">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-508">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="0219c-509">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="0219c-509">Parameters - helpText</span></span>

<span data-ttu-id="0219c-510">値</span><span class="sxs-lookup"><span data-stu-id="0219c-510">value</span></span>  
<span data-ttu-id="0219c-511">コントロールのヘルプ テキストとして設定する値。</span><span class="sxs-lookup"><span data-stu-id="0219c-511">The value to set as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="0219c-512">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="0219c-512">Return Value - helpText</span></span>

<span data-ttu-id="0219c-513">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="0219c-513">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="0219c-514">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="0219c-514">Remarks - helpText</span></span>

<span data-ttu-id="0219c-515">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-515">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="0219c-516">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="0219c-516">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="0219c-517">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0219c-517">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="0219c-518">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0219c-518">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="0219c-519">値</span><span class="sxs-lookup"><span data-stu-id="0219c-519">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="0219c-520">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0219c-520">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="0219c-521">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0219c-521">Method hierarchyParent</span></span>

<span data-ttu-id="0219c-522">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-522">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="0219c-523">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0219c-523">Parameters - hierarchyParent</span></span>

<span data-ttu-id="0219c-524">値</span><span class="sxs-lookup"><span data-stu-id="0219c-524">value</span></span>  
<span data-ttu-id="0219c-525">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="0219c-525">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="0219c-526">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0219c-526">Return Value - hierarchyParent</span></span>

<span data-ttu-id="0219c-527">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="0219c-527">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="0219c-528">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="0219c-528">Method hWnd</span></span>

<span data-ttu-id="0219c-529">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-529">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="0219c-530">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="0219c-530">Return Value - hWnd</span></span>

<span data-ttu-id="0219c-531">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="0219c-531">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="0219c-532">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="0219c-532">Remarks - hWnd</span></span>

<span data-ttu-id="0219c-533">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0219c-533">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="0219c-534">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="0219c-534">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="0219c-535">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="0219c-535">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="0219c-536">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="0219c-536">Method isDisplayed</span></span>

<span data-ttu-id="0219c-537">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-537">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="0219c-538">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="0219c-538">Return Value - isDisplayed</span></span>

<span data-ttu-id="0219c-539">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="0219c-539">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="0219c-540">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="0219c-540">Remarks - isDisplayed</span></span>

<span data-ttu-id="0219c-541">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0219c-541">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="0219c-542">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="0219c-542">Method isRestricted</span></span>

<span data-ttu-id="0219c-543">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-543">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="0219c-544">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="0219c-544">Return Value - isRestricted</span></span>

<span data-ttu-id="0219c-545">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="0219c-545">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="0219c-546">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="0219c-546">Method isUserSetupEnabled</span></span>

<span data-ttu-id="0219c-547">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-547">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="0219c-548">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="0219c-548">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="0219c-549">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="0219c-549">neededSetupRights</span></span>  
<span data-ttu-id="0219c-550">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="0219c-550">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="0219c-551">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="0219c-551">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="0219c-552">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-552">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="0219c-553">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="0219c-553">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="0219c-554">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="0219c-554">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0219c-555">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="0219c-555">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="0219c-556">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="0219c-556">No changes can be made to the control.</span></span> <span data-ttu-id="0219c-557">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-557">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="0219c-558">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="0219c-558">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="0219c-559">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="0219c-559">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="0219c-560">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="0219c-560">The user cannot move the control.</span></span>   |
| <span data-ttu-id="0219c-561">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="0219c-561">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="0219c-562">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="0219c-562">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="0219c-563">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="0219c-563">The user can also move the control.</span></span> |

<span data-ttu-id="0219c-564">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="0219c-564">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-leave"></a><span data-ttu-id="0219c-565">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="0219c-565">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="0219c-566">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="0219c-566">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="0219c-567">メソッド left</span><span class="sxs-lookup"><span data-stu-id="0219c-567">Method left</span></span>

<span data-ttu-id="0219c-568">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-568">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="0219c-569">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="0219c-569">Parameters - left</span></span>

<span data-ttu-id="0219c-570">値</span><span class="sxs-lookup"><span data-stu-id="0219c-570">value</span></span>  
<span data-ttu-id="0219c-571">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-571">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="0219c-572">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-572">mode</span></span>  
<span data-ttu-id="0219c-573">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-573">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="0219c-574">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="0219c-574">Return Value - left</span></span>

<span data-ttu-id="0219c-575">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="0219c-575">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="0219c-576">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="0219c-576">Method leftMode</span></span>

<span data-ttu-id="0219c-577">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-577">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="0219c-578">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="0219c-578">Parameters - leftMode</span></span>

<span data-ttu-id="0219c-579">値</span><span class="sxs-lookup"><span data-stu-id="0219c-579">value</span></span>  
<span data-ttu-id="0219c-580">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-580">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="0219c-581">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="0219c-581">Return Value - leftMode</span></span>

<span data-ttu-id="0219c-582">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="0219c-582">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="0219c-583">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="0219c-583">Method leftValue</span></span>

<span data-ttu-id="0219c-584">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-584">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="0219c-585">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="0219c-585">Parameters - leftValue</span></span>

<span data-ttu-id="0219c-586">値</span><span class="sxs-lookup"><span data-stu-id="0219c-586">value</span></span>  
<span data-ttu-id="0219c-587">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-587">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="0219c-588">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="0219c-588">Return Value - leftValue</span></span>

<span data-ttu-id="0219c-589">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="0219c-589">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="0219c-590">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="0219c-590">Method markAsUserAdd</span></span>

<span data-ttu-id="0219c-591">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="0219c-591">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="0219c-592">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="0219c-592">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="0219c-593">値</span><span class="sxs-lookup"><span data-stu-id="0219c-593">value</span></span>  
<span data-ttu-id="0219c-594">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-594">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="0219c-595">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="0219c-595">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="0219c-596">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-596">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="0219c-597">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="0219c-597">Method mouseDblClick</span></span>

<span data-ttu-id="0219c-598">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-598">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="0219c-599">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="0219c-599">Parameters - mouseDblClick</span></span>

<span data-ttu-id="0219c-600">x</span><span class="sxs-lookup"><span data-stu-id="0219c-600">x</span></span>  
<span data-ttu-id="0219c-601">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-601">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-602">y</span><span class="sxs-lookup"><span data-stu-id="0219c-602">y</span></span>  
<span data-ttu-id="0219c-603">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-603">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-604">ボタン</span><span class="sxs-lookup"><span data-stu-id="0219c-604">button</span></span>  
<span data-ttu-id="0219c-605">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-605">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-606">Ctrl</span><span class="sxs-lookup"><span data-stu-id="0219c-606">Ctrl</span></span>  
<span data-ttu-id="0219c-607">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-607">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-608">シフト</span><span class="sxs-lookup"><span data-stu-id="0219c-608">Shift</span></span>  
<span data-ttu-id="0219c-609">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-609">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="0219c-610">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="0219c-610">Return Value - mouseDblClick</span></span>

<span data-ttu-id="0219c-611">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0219c-611">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="0219c-612">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="0219c-612">Remarks - mouseDblClick</span></span>

<span data-ttu-id="0219c-613">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-613">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="0219c-614">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="0219c-614">Method mouseDown</span></span>

<span data-ttu-id="0219c-615">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-615">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="0219c-616">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="0219c-616">Parameters - mouseDown</span></span>

<span data-ttu-id="0219c-617">x</span><span class="sxs-lookup"><span data-stu-id="0219c-617">x</span></span>  
<span data-ttu-id="0219c-618">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-618">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-619">y</span><span class="sxs-lookup"><span data-stu-id="0219c-619">y</span></span>  
<span data-ttu-id="0219c-620">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-620">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-621">ボタン</span><span class="sxs-lookup"><span data-stu-id="0219c-621">button</span></span>  
<span data-ttu-id="0219c-622">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-622">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-623">Ctrl</span><span class="sxs-lookup"><span data-stu-id="0219c-623">Ctrl</span></span>  
<span data-ttu-id="0219c-624">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-624">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-625">シフト</span><span class="sxs-lookup"><span data-stu-id="0219c-625">Shift</span></span>  
<span data-ttu-id="0219c-626">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-626">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="0219c-627">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="0219c-627">Return Value - mouseDown</span></span>

<span data-ttu-id="0219c-628">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0219c-628">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="0219c-629">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="0219c-629">Remarks - mouseDown</span></span>

<span data-ttu-id="0219c-630">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-630">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="0219c-631">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-631">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="0219c-632">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="0219c-632">Method mouseMove</span></span>

<span data-ttu-id="0219c-633">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-633">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="0219c-634">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="0219c-634">Parameters - mouseMove</span></span>

<span data-ttu-id="0219c-635">x</span><span class="sxs-lookup"><span data-stu-id="0219c-635">x</span></span>  
<span data-ttu-id="0219c-636">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-636">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-637">y</span><span class="sxs-lookup"><span data-stu-id="0219c-637">y</span></span>  
<span data-ttu-id="0219c-638">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-638">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-639">ボタン</span><span class="sxs-lookup"><span data-stu-id="0219c-639">button</span></span>  
<span data-ttu-id="0219c-640">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-640">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-641">Ctrl</span><span class="sxs-lookup"><span data-stu-id="0219c-641">Ctrl</span></span>  
<span data-ttu-id="0219c-642">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-642">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-643">シフト</span><span class="sxs-lookup"><span data-stu-id="0219c-643">Shift</span></span>  
<span data-ttu-id="0219c-644">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-644">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="0219c-645">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="0219c-645">Return Value - mouseMove</span></span>

<span data-ttu-id="0219c-646">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0219c-646">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="0219c-647">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="0219c-647">Remarks - mouseMove</span></span>

<span data-ttu-id="0219c-648">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-648">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="0219c-649">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="0219c-649">Method mouseUp</span></span>

<span data-ttu-id="0219c-650">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-650">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="0219c-651">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="0219c-651">Parameters - mouseUp</span></span>

<span data-ttu-id="0219c-652">x</span><span class="sxs-lookup"><span data-stu-id="0219c-652">x</span></span>  
<span data-ttu-id="0219c-653">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-653">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-654">y</span><span class="sxs-lookup"><span data-stu-id="0219c-654">y</span></span>  
<span data-ttu-id="0219c-655">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-655">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-656">ボタン</span><span class="sxs-lookup"><span data-stu-id="0219c-656">button</span></span>  
<span data-ttu-id="0219c-657">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-657">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-658">Ctrl</span><span class="sxs-lookup"><span data-stu-id="0219c-658">Ctrl</span></span>  
<span data-ttu-id="0219c-659">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-659">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-660">シフト</span><span class="sxs-lookup"><span data-stu-id="0219c-660">Shift</span></span>  
<span data-ttu-id="0219c-661">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-661">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="0219c-662">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="0219c-662">Return Value - mouseUp</span></span>

<span data-ttu-id="0219c-663">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0219c-663">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="0219c-664">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="0219c-664">Remarks - mouseUp</span></span>

<span data-ttu-id="0219c-665">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-665">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="0219c-666">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-666">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="0219c-667">メソッド名</span><span class="sxs-lookup"><span data-stu-id="0219c-667">Method name</span></span>

<span data-ttu-id="0219c-668">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-668">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="0219c-669">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="0219c-669">Parameters - name</span></span>

<span data-ttu-id="0219c-670">値</span><span class="sxs-lookup"><span data-stu-id="0219c-670">value</span></span>  
<span data-ttu-id="0219c-671">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="0219c-671">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="0219c-672">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="0219c-672">Return Value - name</span></span>

<span data-ttu-id="0219c-673">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="0219c-673">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="0219c-674">備考 - name</span><span class="sxs-lookup"><span data-stu-id="0219c-674">Remarks - name</span></span>

<span data-ttu-id="0219c-675">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0219c-675">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="0219c-676">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="0219c-676">It must start with a letter.</span></span>
-   <span data-ttu-id="0219c-677">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="0219c-677">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="0219c-678">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0219c-678">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="0219c-679">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="0219c-679">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="0219c-680">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="0219c-680">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="0219c-681">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="0219c-681">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="0219c-682">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="0219c-682">Parameters - neededPermission</span></span>

<span data-ttu-id="0219c-683">値</span><span class="sxs-lookup"><span data-stu-id="0219c-683">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="0219c-684">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="0219c-684">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="0219c-685">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="0219c-685">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="0219c-686">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="0219c-686">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="0219c-687">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="0219c-687">Method parentControl</span></span>

<span data-ttu-id="0219c-688">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-688">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="0219c-689">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="0219c-689">Return Value - parentControl</span></span>

<span data-ttu-id="0219c-690">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="0219c-690">The parent control for the control.</span></span>

## <a name="method-rtlcapable"></a><span data-ttu-id="0219c-691">メソッド rTLCapable</span><span class="sxs-lookup"><span data-stu-id="0219c-691">Method rTLCapable</span></span>

```xpp
public boolean rTLCapable([boolean value])
```

### <a name="parameters---rtlcapable"></a><span data-ttu-id="0219c-692">パラメーター - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="0219c-692">Parameters - rTLCapable</span></span>

<span data-ttu-id="0219c-693">値</span><span class="sxs-lookup"><span data-stu-id="0219c-693">value</span></span>  

### <a name="return-value---rtlcapable"></a><span data-ttu-id="0219c-694">戻り値 - rTLCapable</span><span class="sxs-lookup"><span data-stu-id="0219c-694">Return Value - rTLCapable</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="0219c-695">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="0219c-695">Method securityKey</span></span>

<span data-ttu-id="0219c-696">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-696">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="0219c-697">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="0219c-697">Parameters - securityKey</span></span>

<span data-ttu-id="0219c-698">値</span><span class="sxs-lookup"><span data-stu-id="0219c-698">value</span></span>  
<span data-ttu-id="0219c-699">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-699">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="0219c-700">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="0219c-700">Return Value - securityKey</span></span>

<span data-ttu-id="0219c-701">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="0219c-701">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="0219c-702">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="0219c-702">Method showContextMenu</span></span>

<span data-ttu-id="0219c-703">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-703">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="0219c-704">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="0219c-704">Parameters - showContextMenu</span></span>

<span data-ttu-id="0219c-705">menuHandle</span><span class="sxs-lookup"><span data-stu-id="0219c-705">menuHandle</span></span>  
<span data-ttu-id="0219c-706">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="0219c-706">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="0219c-707">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="0219c-707">Return Value - showContextMenu</span></span>

<span data-ttu-id="0219c-708">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-708">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-sizing"></a><span data-ttu-id="0219c-709">メソッド sizing</span><span class="sxs-lookup"><span data-stu-id="0219c-709">Method sizing</span></span>

```xpp
public int sizing([int value])
```

### <a name="parameters---sizing"></a><span data-ttu-id="0219c-710">パラメーター - sizing</span><span class="sxs-lookup"><span data-stu-id="0219c-710">Parameters - sizing</span></span>

<span data-ttu-id="0219c-711">値</span><span class="sxs-lookup"><span data-stu-id="0219c-711">value</span></span>  

### <a name="return-value---sizing"></a><span data-ttu-id="0219c-712">戻り値 - sizing</span><span class="sxs-lookup"><span data-stu-id="0219c-712">Return Value - sizing</span></span>

## <a name="method-skip"></a><span data-ttu-id="0219c-713">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="0219c-713">Method skip</span></span>

<span data-ttu-id="0219c-714">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-714">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="0219c-715">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="0219c-715">Parameters - skip</span></span>

<span data-ttu-id="0219c-716">値</span><span class="sxs-lookup"><span data-stu-id="0219c-716">value</span></span>  
<span data-ttu-id="0219c-717">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-717">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="0219c-718">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="0219c-718">Return Value - skip</span></span>

<span data-ttu-id="0219c-719">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0219c-719">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="0219c-720">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="0219c-720">Remarks - skip</span></span>

<span data-ttu-id="0219c-721">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="0219c-721">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="0219c-722">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="0219c-722">Method toolTip</span></span>

<span data-ttu-id="0219c-723">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0219c-723">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="0219c-724">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="0219c-724">Return Value - toolTip</span></span>

<span data-ttu-id="0219c-725">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="0219c-725">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="0219c-726">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="0219c-726">Remarks - toolTip</span></span>

<span data-ttu-id="0219c-727">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="0219c-727">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="0219c-728">メソッド top</span><span class="sxs-lookup"><span data-stu-id="0219c-728">Method top</span></span>

<span data-ttu-id="0219c-729">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-729">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="0219c-730">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="0219c-730">Parameters - top</span></span>

<span data-ttu-id="0219c-731">値</span><span class="sxs-lookup"><span data-stu-id="0219c-731">value</span></span>  
<span data-ttu-id="0219c-732">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-732">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="0219c-733">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-733">mode</span></span>  
<span data-ttu-id="0219c-734">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-734">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="0219c-735">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="0219c-735">Return Value - top</span></span>

<span data-ttu-id="0219c-736">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="0219c-736">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="0219c-737">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="0219c-737">Method topMode</span></span>

<span data-ttu-id="0219c-738">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-738">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="0219c-739">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="0219c-739">Parameters - topMode</span></span>

<span data-ttu-id="0219c-740">値</span><span class="sxs-lookup"><span data-stu-id="0219c-740">value</span></span>  
<span data-ttu-id="0219c-741">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-741">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="0219c-742">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="0219c-742">Return Value - topMode</span></span>

<span data-ttu-id="0219c-743">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="0219c-743">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="0219c-744">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="0219c-744">Method topValue</span></span>

<span data-ttu-id="0219c-745">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-745">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="0219c-746">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="0219c-746">Parameters - topValue</span></span>

<span data-ttu-id="0219c-747">値</span><span class="sxs-lookup"><span data-stu-id="0219c-747">value</span></span>  
<span data-ttu-id="0219c-748">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-748">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="0219c-749">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="0219c-749">Return Value - topValue</span></span>

<span data-ttu-id="0219c-750">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="0219c-750">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="0219c-751">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="0219c-751">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="0219c-752">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="0219c-752">Parameters - type</span></span>

<span data-ttu-id="0219c-753">値</span><span class="sxs-lookup"><span data-stu-id="0219c-753">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="0219c-754">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="0219c-754">Return Value - type</span></span>

## <a name="method-typename"></a><span data-ttu-id="0219c-755">メソッド typeName</span><span class="sxs-lookup"><span data-stu-id="0219c-755">Method typeName</span></span>

```xpp
public str typeName([str value])
```

### <a name="parameters---typename"></a><span data-ttu-id="0219c-756">パラメーター - typeName</span><span class="sxs-lookup"><span data-stu-id="0219c-756">Parameters - typeName</span></span>

<span data-ttu-id="0219c-757">値</span><span class="sxs-lookup"><span data-stu-id="0219c-757">value</span></span>  

### <a name="return-value---typename"></a><span data-ttu-id="0219c-758">戻り値 - typeName</span><span class="sxs-lookup"><span data-stu-id="0219c-758">Return Value - typeName</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="0219c-759">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="0219c-759">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="0219c-760">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="0219c-760">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="0219c-761">データ</span><span class="sxs-lookup"><span data-stu-id="0219c-761">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="0219c-762">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="0219c-762">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="0219c-763">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="0219c-763">Method userData</span></span>

<span data-ttu-id="0219c-764">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-764">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="0219c-765">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="0219c-765">Parameters - userData</span></span>

<span data-ttu-id="0219c-766">値</span><span class="sxs-lookup"><span data-stu-id="0219c-766">value</span></span>  
<span data-ttu-id="0219c-767">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-767">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="0219c-768">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="0219c-768">Return Value - userData</span></span>

<span data-ttu-id="0219c-769">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="0219c-769">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="0219c-770">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="0219c-770">Method userDataItem</span></span>

<span data-ttu-id="0219c-771">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-771">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="0219c-772">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="0219c-772">Parameters - userDataItem</span></span>

<span data-ttu-id="0219c-773">値</span><span class="sxs-lookup"><span data-stu-id="0219c-773">value</span></span>  
<span data-ttu-id="0219c-774">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-774">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="0219c-775">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="0219c-775">Return Value - userDataItem</span></span>

<span data-ttu-id="0219c-776">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="0219c-776">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="0219c-777">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="0219c-777">Method userDataItems</span></span>

<span data-ttu-id="0219c-778">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-778">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="0219c-779">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="0219c-779">Parameters - userDataItems</span></span>

<span data-ttu-id="0219c-780">値</span><span class="sxs-lookup"><span data-stu-id="0219c-780">value</span></span>  
<span data-ttu-id="0219c-781">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-781">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="0219c-782">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="0219c-782">Return Value - userDataItems</span></span>

<span data-ttu-id="0219c-783">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="0219c-783">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="0219c-784">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="0219c-784">Method userDisable</span></span>

<span data-ttu-id="0219c-785">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-785">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="0219c-786">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="0219c-786">Parameters - userDisable</span></span>

<span data-ttu-id="0219c-787">値</span><span class="sxs-lookup"><span data-stu-id="0219c-787">value</span></span>  
<span data-ttu-id="0219c-788">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-788">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="0219c-789">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="0219c-789">Return Value - userDisable</span></span>

<span data-ttu-id="0219c-790">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="0219c-790">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="0219c-791">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="0219c-791">Method userHeight</span></span>

<span data-ttu-id="0219c-792">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-792">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="0219c-793">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="0219c-793">Parameters - userHeight</span></span>

<span data-ttu-id="0219c-794">値</span><span class="sxs-lookup"><span data-stu-id="0219c-794">value</span></span>  
<span data-ttu-id="0219c-795">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-795">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="0219c-796">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="0219c-796">Return Value - userHeight</span></span>

<span data-ttu-id="0219c-797">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="0219c-797">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="0219c-798">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="0219c-798">Method userHide</span></span>

<span data-ttu-id="0219c-799">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-799">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="0219c-800">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="0219c-800">Parameters - userHide</span></span>

<span data-ttu-id="0219c-801">値</span><span class="sxs-lookup"><span data-stu-id="0219c-801">value</span></span>  
<span data-ttu-id="0219c-802">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-802">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="0219c-803">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="0219c-803">Return Value - userHide</span></span>

<span data-ttu-id="0219c-804">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="0219c-804">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="0219c-805">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="0219c-805">Remarks - userHide</span></span>

<span data-ttu-id="0219c-806">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-806">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="0219c-807">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="0219c-807">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="0219c-808">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="0219c-808">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="0219c-809">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="0219c-809">Method userOrgContainer</span></span>

<span data-ttu-id="0219c-810">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-810">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="0219c-811">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="0219c-811">Parameters - userOrgContainer</span></span>

<span data-ttu-id="0219c-812">値</span><span class="sxs-lookup"><span data-stu-id="0219c-812">value</span></span>  
<span data-ttu-id="0219c-813">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-813">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="0219c-814">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="0219c-814">Return Value - userOrgContainer</span></span>

<span data-ttu-id="0219c-815">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="0219c-815">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="0219c-816">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="0219c-816">Method userOrgSibling</span></span>

<span data-ttu-id="0219c-817">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-817">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="0219c-818">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="0219c-818">Parameters - userOrgSibling</span></span>

<span data-ttu-id="0219c-819">値</span><span class="sxs-lookup"><span data-stu-id="0219c-819">value</span></span>  
<span data-ttu-id="0219c-820">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-820">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="0219c-821">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="0219c-821">Return Value - userOrgSibling</span></span>

<span data-ttu-id="0219c-822">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="0219c-822">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="0219c-823">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="0219c-823">Method userPromptText</span></span>

<span data-ttu-id="0219c-824">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-824">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="0219c-825">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="0219c-825">Parameters - userPromptText</span></span>

<span data-ttu-id="0219c-826">値</span><span class="sxs-lookup"><span data-stu-id="0219c-826">value</span></span>  
<span data-ttu-id="0219c-827">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-827">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="0219c-828">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="0219c-828">Return Value - userPromptText</span></span>

<span data-ttu-id="0219c-829">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="0219c-829">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="0219c-830">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="0219c-830">Method userSecurityLevel</span></span>

<span data-ttu-id="0219c-831">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-831">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="0219c-832">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="0219c-832">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="0219c-833">値</span><span class="sxs-lookup"><span data-stu-id="0219c-833">value</span></span>  
<span data-ttu-id="0219c-834">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-834">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="0219c-835">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="0219c-835">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="0219c-836">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="0219c-836">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="0219c-837">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="0219c-837">Method userSkip</span></span>

<span data-ttu-id="0219c-838">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-838">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="0219c-839">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="0219c-839">Parameters - userSkip</span></span>

<span data-ttu-id="0219c-840">値</span><span class="sxs-lookup"><span data-stu-id="0219c-840">value</span></span>  
<span data-ttu-id="0219c-841">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-841">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="0219c-842">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="0219c-842">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="0219c-843">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="0219c-843">Return Value - userSkip</span></span>

<span data-ttu-id="0219c-844">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="0219c-844">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="0219c-845">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="0219c-845">Method userWidth</span></span>

<span data-ttu-id="0219c-846">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-846">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="0219c-847">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="0219c-847">Parameters - userWidth</span></span>

<span data-ttu-id="0219c-848">値</span><span class="sxs-lookup"><span data-stu-id="0219c-848">value</span></span>  
<span data-ttu-id="0219c-849">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-849">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="0219c-850">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="0219c-850">Return Value - userWidth</span></span>

<span data-ttu-id="0219c-851">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="0219c-851">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="0219c-852">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="0219c-852">Remarks - userWidth</span></span>

<span data-ttu-id="0219c-853">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-853">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="0219c-854">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="0219c-854">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="0219c-855">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="0219c-855">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="0219c-856">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0219c-856">Method verticalSpacing</span></span>

<span data-ttu-id="0219c-857">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-857">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="0219c-858">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0219c-858">Parameters - verticalSpacing</span></span>

<span data-ttu-id="0219c-859">値</span><span class="sxs-lookup"><span data-stu-id="0219c-859">value</span></span>  
<span data-ttu-id="0219c-860">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-860">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="0219c-861">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-861">mode</span></span>  
<span data-ttu-id="0219c-862">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-862">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="0219c-863">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0219c-863">Return Value - verticalSpacing</span></span>

<span data-ttu-id="0219c-864">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="0219c-864">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="0219c-865">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0219c-865">Method verticalSpacingMode</span></span>

<span data-ttu-id="0219c-866">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-866">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="0219c-867">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0219c-867">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="0219c-868">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-868">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="0219c-869">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0219c-869">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="0219c-870">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="0219c-870">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="0219c-871">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0219c-871">Method verticalSpacingValue</span></span>

<span data-ttu-id="0219c-872">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-872">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="0219c-873">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0219c-873">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="0219c-874">値</span><span class="sxs-lookup"><span data-stu-id="0219c-874">value</span></span>  
<span data-ttu-id="0219c-875">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-875">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="0219c-876">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0219c-876">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="0219c-877">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="0219c-877">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="0219c-878">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="0219c-878">Method visible</span></span>

<span data-ttu-id="0219c-879">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0219c-879">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="0219c-880">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="0219c-880">Parameters - visible</span></span>

<span data-ttu-id="0219c-881">値</span><span class="sxs-lookup"><span data-stu-id="0219c-881">value</span></span>  
<span data-ttu-id="0219c-882">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-882">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="0219c-883">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="0219c-883">Return Value - visible</span></span>

<span data-ttu-id="0219c-884">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="0219c-884">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="0219c-885">メソッド width</span><span class="sxs-lookup"><span data-stu-id="0219c-885">Method width</span></span>

<span data-ttu-id="0219c-886">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-886">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="0219c-887">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="0219c-887">Parameters - width</span></span>

<span data-ttu-id="0219c-888">値</span><span class="sxs-lookup"><span data-stu-id="0219c-888">value</span></span>  
<span data-ttu-id="0219c-889">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-889">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="0219c-890">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-890">mode</span></span>  
<span data-ttu-id="0219c-891">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-891">An Integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="0219c-892">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="0219c-892">Return Value - width</span></span>

<span data-ttu-id="0219c-893">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="0219c-893">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="0219c-894">備考 - width</span><span class="sxs-lookup"><span data-stu-id="0219c-894">Remarks - width</span></span>

<span data-ttu-id="0219c-895">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-895">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="0219c-896">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="0219c-896">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="0219c-897">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-897">Mode</span></span>           | <span data-ttu-id="0219c-898">幅計算</span><span class="sxs-lookup"><span data-stu-id="0219c-898">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0219c-899">-1 正確</span><span class="sxs-lookup"><span data-stu-id="0219c-899">-1 Exact</span></span>       | <span data-ttu-id="0219c-900">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-900">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0219c-901">0 自動</span><span class="sxs-lookup"><span data-stu-id="0219c-901">0 Auto</span></span>         | <span data-ttu-id="0219c-902">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-902">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0219c-903">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="0219c-903">1 Column width</span></span> | <span data-ttu-id="0219c-904">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="0219c-904">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="0219c-905">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0219c-905">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="0219c-906">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="0219c-906">Method widthMode</span></span>

<span data-ttu-id="0219c-907">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-907">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="0219c-908">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="0219c-908">Parameters - widthMode</span></span>

<span data-ttu-id="0219c-909">値</span><span class="sxs-lookup"><span data-stu-id="0219c-909">value</span></span>  
<span data-ttu-id="0219c-910">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="0219c-910">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="0219c-911">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="0219c-911">Return Value - widthMode</span></span>

<span data-ttu-id="0219c-912">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-912">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="0219c-913">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="0219c-913">Remarks - widthMode</span></span>

<span data-ttu-id="0219c-914">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="0219c-914">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="0219c-915">モード</span><span class="sxs-lookup"><span data-stu-id="0219c-915">Mode</span></span>         | <span data-ttu-id="0219c-916">幅計算</span><span class="sxs-lookup"><span data-stu-id="0219c-916">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0219c-917">正確</span><span class="sxs-lookup"><span data-stu-id="0219c-917">Exact</span></span>        | <span data-ttu-id="0219c-918">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-918">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0219c-919">自動</span><span class="sxs-lookup"><span data-stu-id="0219c-919">Auto</span></span>         | <span data-ttu-id="0219c-920">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-920">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0219c-921">列の幅</span><span class="sxs-lookup"><span data-stu-id="0219c-921">Column width</span></span> | <span data-ttu-id="0219c-922">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="0219c-922">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="0219c-923">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0219c-923">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="0219c-924">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="0219c-924">Method widthValue</span></span>

<span data-ttu-id="0219c-925">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-925">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="0219c-926">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="0219c-926">Parameters - widthValue</span></span>

<span data-ttu-id="0219c-927">値</span><span class="sxs-lookup"><span data-stu-id="0219c-927">value</span></span>  
<span data-ttu-id="0219c-928">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-928">An Integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="0219c-929">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="0219c-929">Return Value - widthValue</span></span>

<span data-ttu-id="0219c-930">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="0219c-930">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="0219c-931">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="0219c-931">Remarks - widthValue</span></span>

<span data-ttu-id="0219c-932">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="0219c-932">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-enter"></a><span data-ttu-id="0219c-933">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="0219c-933">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="0219c-934">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="0219c-934">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="0219c-935">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="0219c-935">Parameters - OnGotFocus</span></span>

<span data-ttu-id="0219c-936">sender</span><span class="sxs-lookup"><span data-stu-id="0219c-936">sender</span></span>  

<!-- -->

<span data-ttu-id="0219c-937">e</span><span class="sxs-lookup"><span data-stu-id="0219c-937">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="0219c-938">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="0219c-938">Method dropEx</span></span>

<span data-ttu-id="0219c-939">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-939">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="0219c-940">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="0219c-940">Parameters - dropEx</span></span>

<span data-ttu-id="0219c-941">dragSource</span><span class="sxs-lookup"><span data-stu-id="0219c-941">dragSource</span></span>  
<span data-ttu-id="0219c-942">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-942">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-943">dragMode</span><span class="sxs-lookup"><span data-stu-id="0219c-943">dragMode</span></span>  
<span data-ttu-id="0219c-944">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-944">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-945">x</span><span class="sxs-lookup"><span data-stu-id="0219c-945">x</span></span>  
<span data-ttu-id="0219c-946">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-946">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-947">y</span><span class="sxs-lookup"><span data-stu-id="0219c-947">y</span></span>  
<span data-ttu-id="0219c-948">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-948">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="0219c-949">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="0219c-949">Method lostFocus</span></span>

<span data-ttu-id="0219c-950">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-950">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="0219c-951">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="0219c-951">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="0219c-952">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="0219c-952">Parameters - OnLostFocus</span></span>

<span data-ttu-id="0219c-953">sender</span><span class="sxs-lookup"><span data-stu-id="0219c-953">sender</span></span>  

<!-- -->

<span data-ttu-id="0219c-954">e</span><span class="sxs-lookup"><span data-stu-id="0219c-954">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="0219c-955">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="0219c-955">Method paste</span></span>

<span data-ttu-id="0219c-956">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="0219c-956">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-mouseleave"></a><span data-ttu-id="0219c-957">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="0219c-957">Method mouseLeave</span></span>

<span data-ttu-id="0219c-958">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-958">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-drop"></a><span data-ttu-id="0219c-959">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="0219c-959">Method drop</span></span>

<span data-ttu-id="0219c-960">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-960">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="0219c-961">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="0219c-961">Parameters - drop</span></span>

<span data-ttu-id="0219c-962">dragSource</span><span class="sxs-lookup"><span data-stu-id="0219c-962">dragSource</span></span>  
<span data-ttu-id="0219c-963">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-963">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-964">dragMode</span><span class="sxs-lookup"><span data-stu-id="0219c-964">dragMode</span></span>  
<span data-ttu-id="0219c-965">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-965">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-966">x</span><span class="sxs-lookup"><span data-stu-id="0219c-966">x</span></span>  
<span data-ttu-id="0219c-967">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-967">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="0219c-968">y</span><span class="sxs-lookup"><span data-stu-id="0219c-968">y</span></span>  
<span data-ttu-id="0219c-969">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0219c-969">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onleaving"></a><span data-ttu-id="0219c-970">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="0219c-970">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="0219c-971">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="0219c-971">Parameters - OnLeaving</span></span>

<span data-ttu-id="0219c-972">sender</span><span class="sxs-lookup"><span data-stu-id="0219c-972">sender</span></span>  

<!-- -->

<span data-ttu-id="0219c-973">e</span><span class="sxs-lookup"><span data-stu-id="0219c-973">e</span></span>  

## <a name="method-onenter"></a><span data-ttu-id="0219c-974">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="0219c-974">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="0219c-975">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="0219c-975">Parameters - OnEnter</span></span>

<span data-ttu-id="0219c-976">sender</span><span class="sxs-lookup"><span data-stu-id="0219c-976">sender</span></span>  

<!-- -->

<span data-ttu-id="0219c-977">e</span><span class="sxs-lookup"><span data-stu-id="0219c-977">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="0219c-978">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="0219c-978">Method dragLeave</span></span>

<span data-ttu-id="0219c-979">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0219c-979">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="0219c-980">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="0219c-980">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="0219c-981">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="0219c-981">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="0219c-982">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="0219c-982">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="0219c-983">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="0219c-983">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="0219c-984">overrideObject</span><span class="sxs-lookup"><span data-stu-id="0219c-984">overrideObject</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="0219c-985">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="0219c-985">Method endDrag</span></span>

<span data-ttu-id="0219c-986">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-986">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="0219c-987">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="0219c-987">Remarks - endDrag</span></span>

<span data-ttu-id="0219c-988">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="0219c-988">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="0219c-989">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="0219c-989">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-copy"></a><span data-ttu-id="0219c-990">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="0219c-990">Method copy</span></span>

<span data-ttu-id="0219c-991">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0219c-991">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-cut"></a><span data-ttu-id="0219c-992">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="0219c-992">Method cut</span></span>

<span data-ttu-id="0219c-993">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="0219c-993">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="0219c-994">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="0219c-994">Method displayControl</span></span>

<span data-ttu-id="0219c-995">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-995">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="0219c-996">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="0219c-996">Method prefColumnSize</span></span>

<span data-ttu-id="0219c-997">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-997">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="0219c-998">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="0219c-998">Parameters - prefColumnSize</span></span>

<span data-ttu-id="0219c-999">width</span><span class="sxs-lookup"><span data-stu-id="0219c-999">width</span></span>  
<span data-ttu-id="0219c-1000">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="0219c-1000">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="0219c-1001">height</span><span class="sxs-lookup"><span data-stu-id="0219c-1001">height</span></span>  
<span data-ttu-id="0219c-1002">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="0219c-1002">The preferred height of the control.</span></span>

## <a name="method-context"></a><span data-ttu-id="0219c-1003">メソッド context</span><span class="sxs-lookup"><span data-stu-id="0219c-1003">Method context</span></span>

<span data-ttu-id="0219c-1004">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-1004">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="0219c-1005">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="0219c-1005">Method resetUserSetting</span></span>

<span data-ttu-id="0219c-1006">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="0219c-1006">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-inputsearch"></a><span data-ttu-id="0219c-1007">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="0219c-1007">Method inputSearch</span></span>

<span data-ttu-id="0219c-1008">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="0219c-1008">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="0219c-1009">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="0219c-1009">Parameters - inputSearch</span></span>

<span data-ttu-id="0219c-1010">searchStr</span><span class="sxs-lookup"><span data-stu-id="0219c-1010">searchStr</span></span>  
<span data-ttu-id="0219c-1011">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0219c-1011">The string value to use to filter data; optional.</span></span>

## <a name="method-gotfocus"></a><span data-ttu-id="0219c-1012">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="0219c-1012">Method gotFocus</span></span>

<span data-ttu-id="0219c-1013">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="0219c-1013">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="0219c-1014">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="0219c-1014">Method mouseEnter</span></span>

<span data-ttu-id="0219c-1015">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0219c-1015">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="0219c-1016">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="0219c-1016">Parameters - mouseEnter</span></span>

<span data-ttu-id="0219c-1017">x</span><span class="sxs-lookup"><span data-stu-id="0219c-1017">x</span></span>  
<span data-ttu-id="0219c-1018">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-1018">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-1019">y</span><span class="sxs-lookup"><span data-stu-id="0219c-1019">y</span></span>  
<span data-ttu-id="0219c-1020">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-1020">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-1021">ボタン</span><span class="sxs-lookup"><span data-stu-id="0219c-1021">button</span></span>  
<span data-ttu-id="0219c-1022">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-1022">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-1023">Ctrl</span><span class="sxs-lookup"><span data-stu-id="0219c-1023">Ctrl</span></span>  
<span data-ttu-id="0219c-1024">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-1024">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="0219c-1025">シフト</span><span class="sxs-lookup"><span data-stu-id="0219c-1025">Shift</span></span>  
<span data-ttu-id="0219c-1026">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0219c-1026">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="0219c-1027">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="0219c-1027">Method setFocus</span></span>

<span data-ttu-id="0219c-1028">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="0219c-1028">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

