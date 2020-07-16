---
title: FormTableControl クラス
description: このトピックでは、FormTabControl クラスについて説明します。
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
ms.openlocfilehash: 223919c47aee5b8a1857915bdc03d9ab0e145ef0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502615"
---
# <a name="class-formtablecontrol"></a><span data-ttu-id="29385-103">クラス FormTableControl</span><span class="sxs-lookup"><span data-stu-id="29385-103">Class FormTableControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormTableControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="29385-104">備考</span><span class="sxs-lookup"><span data-stu-id="29385-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="29385-105">例</span><span class="sxs-lookup"><span data-stu-id="29385-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="29385-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="29385-106">Methods</span></span>

| <span data-ttu-id="29385-107">方法</span><span class="sxs-lookup"><span data-stu-id="29385-107">Method</span></span>                                                                                                              | <span data-ttu-id="29385-108">説明</span><span class="sxs-lookup"><span data-stu-id="29385-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29385-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="29385-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="29385-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="29385-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="29385-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="29385-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="29385-112">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-112">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="29385-113">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-113">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="29385-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="29385-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-115">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="29385-116">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="29385-116">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="29385-117">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-117">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="29385-118">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-118">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="29385-119">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-119">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="29385-120">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-120">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="29385-121">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-121">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="29385-122">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="29385-122">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="29385-123">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-123">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="29385-124">public int bottomMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-124">public int bottomMargin(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="29385-125">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="29385-125">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="29385-126">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-126">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="29385-127">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="29385-127">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="29385-128">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="29385-128">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="29385-129">public FormTableCell cell(\[int column\], \[int row\])</span><span class="sxs-lookup"><span data-stu-id="29385-129">public FormTableCell cell(\[int column\], \[int row\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="29385-130">public str colLabel(int column)</span><span class="sxs-lookup"><span data-stu-id="29385-130">public str colLabel(int column)</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="29385-131">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-131">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="29385-132">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-132">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="29385-133">public int column(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-133">public int column(\[int value\])</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="29385-134">public int columns(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-134">public int columns(\[int value\])</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="29385-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="29385-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="29385-136">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-136">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="29385-137">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="29385-137">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="29385-138">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-138">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="29385-139">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="29385-139">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="29385-140">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="29385-140">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="29385-141">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="29385-141">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="29385-142">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29385-142">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="29385-143">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-143">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="29385-144">public AnyType data(int column, int row)</span><span class="sxs-lookup"><span data-stu-id="29385-144">public AnyType data(int column, int row)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="29385-145">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29385-145">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="29385-146">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-146">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="29385-147">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-147">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="29385-148">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-148">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="29385-149">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-149">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="29385-150">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-150">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="29385-151">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="29385-151">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="29385-152">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-152">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="29385-153">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="29385-153">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="29385-154">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-154">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="29385-155">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="29385-155">public str dragText()</span></span>                                                                                               | <span data-ttu-id="29385-156">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-156">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="29385-157">public FormControl editControl(int Column, int Row)</span><span class="sxs-lookup"><span data-stu-id="29385-157">public FormControl editControl(int Column, int Row)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="29385-158">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-158">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="29385-159">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-159">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="29385-160">public boolean gridLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-160">public boolean gridLines(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="29385-161">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="29385-161">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="29385-162">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-162">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="29385-163">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="29385-163">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="29385-164">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="29385-164">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="29385-165">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="29385-165">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="29385-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-166">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="29385-167">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-167">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="29385-168">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-168">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="29385-169">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-169">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="29385-170">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-170">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="29385-171">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="29385-171">public str helpField()</span></span>                                                                                              | <span data-ttu-id="29385-172">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-172">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="29385-173">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29385-173">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="29385-174">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-174">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="29385-175">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29385-175">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="29385-176">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-176">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="29385-177">public boolean highlightActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-177">public boolean highlightActive(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="29385-178">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="29385-178">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="29385-179">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-179">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="29385-180">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="29385-180">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="29385-181">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="29385-181">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="29385-182">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-182">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="29385-183">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="29385-183">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="29385-184">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-184">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="29385-185">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="29385-185">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="29385-186">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-186">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="29385-187">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="29385-187">public boolean leave()</span></span>                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="29385-188">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="29385-188">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="29385-189">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-189">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="29385-190">public int leftMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-190">public int leftMargin(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="29385-191">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-191">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="29385-192">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-192">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="29385-193">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-193">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="29385-194">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-194">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="29385-195">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-195">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="29385-196">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="29385-196">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="29385-197">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="29385-197">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="29385-198">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-198">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="29385-199">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="29385-199">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="29385-200">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-200">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="29385-201">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="29385-201">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="29385-202">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-202">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="29385-203">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="29385-203">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="29385-204">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-204">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="29385-205">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="29385-205">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="29385-206">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29385-206">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="29385-207">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-207">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                               |
| <span data-ttu-id="29385-208">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-208">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="29385-209">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="29385-209">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="29385-210">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="29385-210">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="29385-211">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-211">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="29385-212">public int rightMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-212">public int rightMargin(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="29385-213">public int row(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-213">public int row(\[int value\])</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="29385-214">public str rowLabel(int row)</span><span class="sxs-lookup"><span data-stu-id="29385-214">public str rowLabel(int row)</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="29385-215">public int rows(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-215">public int rows(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="29385-216">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="29385-216">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="29385-217">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-217">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="29385-218">public boolean showColLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-218">public boolean showColLabels(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="29385-219">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="29385-219">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="29385-220">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="29385-220">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="29385-221">public boolean showRowLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-221">public boolean showRowLabels(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="29385-222">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-222">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="29385-223">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-223">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="29385-224">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="29385-224">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="29385-225">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-225">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="29385-226">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="29385-226">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="29385-227">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-227">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="29385-228">public int topMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-228">public int topMargin(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="29385-229">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-229">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="29385-230">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-230">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="29385-231">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-231">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="29385-232">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-232">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="29385-233">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-233">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="29385-234">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="29385-234">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="29385-235">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-235">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="29385-236">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-236">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="29385-237">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-237">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="29385-238">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-238">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="29385-239">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-239">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="29385-240">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-240">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="29385-241">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-241">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="29385-242">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-242">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="29385-243">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-243">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="29385-244">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-244">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="29385-245">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-245">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="29385-246">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-246">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="29385-247">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-247">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="29385-248">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-248">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="29385-249">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-249">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="29385-250">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-250">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="29385-251">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29385-251">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="29385-252">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-252">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="29385-253">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-253">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="29385-254">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-254">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="29385-255">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-255">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="29385-256">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-256">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="29385-257">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-257">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="29385-258">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-258">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="29385-259">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-259">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="29385-260">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="29385-260">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="29385-261">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-261">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="29385-262">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="29385-262">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="29385-263">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-263">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="29385-264">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-264">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="29385-265">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-265">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="29385-266">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29385-266">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="29385-267">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-267">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="29385-268">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="29385-268">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="29385-269">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-269">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="29385-270">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-270">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="29385-271">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-271">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="29385-272">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29385-272">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="29385-273">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-273">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="29385-274">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="29385-274">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="29385-275">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="29385-275">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="29385-276">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="29385-276">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="29385-277">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-277">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="29385-278">public void setColLabel(int column, str text)</span><span class="sxs-lookup"><span data-stu-id="29385-278">public void setColLabel(int column, str text)</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="29385-279">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="29385-279">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="29385-280">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-280">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="29385-281">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="29385-281">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="29385-282">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="29385-282">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="29385-283">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="29385-283">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="29385-284">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="29385-284">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="29385-285">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="29385-285">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="29385-286">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="29385-286">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="29385-287">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="29385-287">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="29385-288">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-288">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="29385-289">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="29385-289">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="29385-290">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="29385-290">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="29385-291">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="29385-291">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="29385-292">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="29385-292">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="29385-293">public void deleteRows(int deleteAfterRow, int rows)</span><span class="sxs-lookup"><span data-stu-id="29385-293">public void deleteRows(int deleteAfterRow, int rows)</span></span>                                                                | <span data-ttu-id="29385-294">;</span><span class="sxs-lookup"><span data-stu-id="29385-294">;</span></span>                                                                                                                                                                       |
| <span data-ttu-id="29385-295">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="29385-295">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="29385-296">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-296">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="29385-297">public void deleteCols(int deleteAfterColumn, int columns)</span><span class="sxs-lookup"><span data-stu-id="29385-297">public void deleteCols(int deleteAfterColumn, int columns)</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="29385-298">public void clear()</span><span class="sxs-lookup"><span data-stu-id="29385-298">public void clear()</span></span>                                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="29385-299">public void insertRows(int insertAfterRow, int rows)</span><span class="sxs-lookup"><span data-stu-id="29385-299">public void insertRows(int insertAfterRow, int rows)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="29385-300">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="29385-300">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="29385-301">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="29385-301">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="29385-302">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="29385-302">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="29385-303">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="29385-303">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="29385-304">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="29385-304">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="29385-305">public void copy()</span><span class="sxs-lookup"><span data-stu-id="29385-305">public void copy()</span></span>                                                                                                  | <span data-ttu-id="29385-306">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="29385-306">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="29385-307">public void setRowLabel(int row, str text)</span><span class="sxs-lookup"><span data-stu-id="29385-307">public void setRowLabel(int row, str text)</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="29385-308">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="29385-308">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="29385-309">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="29385-309">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="29385-310">public void paste()</span><span class="sxs-lookup"><span data-stu-id="29385-310">public void paste()</span></span>                                                                                                 | <span data-ttu-id="29385-311">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="29385-311">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="29385-312">public void enter()</span><span class="sxs-lookup"><span data-stu-id="29385-312">public void enter()</span></span>                                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="29385-313">public void cut()</span><span class="sxs-lookup"><span data-stu-id="29385-313">public void cut()</span></span>                                                                                                   | <span data-ttu-id="29385-314">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="29385-314">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="29385-315">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="29385-315">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="29385-316">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-316">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="29385-317">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="29385-317">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="29385-318">public void updateCell(int column, int row)</span><span class="sxs-lookup"><span data-stu-id="29385-318">public void updateCell(int column, int row)</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="29385-319">public void insertCols(int insertAferColumn, int columns)</span><span class="sxs-lookup"><span data-stu-id="29385-319">public void insertCols(int insertAferColumn, int columns)</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="29385-320">public void activeCellChanged()</span><span class="sxs-lookup"><span data-stu-id="29385-320">public void activeCellChanged()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="29385-321">public void context()</span><span class="sxs-lookup"><span data-stu-id="29385-321">public void context()</span></span>                                                                                               | <span data-ttu-id="29385-322">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="29385-322">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="29385-323">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="29385-323">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="29385-324">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-324">Sets the focus on the control.</span></span>                                                                                                                                          |

## <a name="method-addcontrol"></a><span data-ttu-id="29385-325">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="29385-325">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="29385-326">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="29385-326">Parameters - addControl</span></span>

<span data-ttu-id="29385-327">controlType</span><span class="sxs-lookup"><span data-stu-id="29385-327">controlType</span></span>  

<!-- -->

<span data-ttu-id="29385-328">controlName</span><span class="sxs-lookup"><span data-stu-id="29385-328">controlName</span></span>  

<!-- -->

<span data-ttu-id="29385-329">insertAfter</span><span class="sxs-lookup"><span data-stu-id="29385-329">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="29385-330">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="29385-330">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="29385-331">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="29385-331">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="29385-332">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="29385-332">Parameters - addControlEx</span></span>

<span data-ttu-id="29385-333">controlClass</span><span class="sxs-lookup"><span data-stu-id="29385-333">controlClass</span></span>  

<!-- -->

<span data-ttu-id="29385-334">controlName</span><span class="sxs-lookup"><span data-stu-id="29385-334">controlName</span></span>  

<!-- -->

<span data-ttu-id="29385-335">insertAfter</span><span class="sxs-lookup"><span data-stu-id="29385-335">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="29385-336">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="29385-336">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="29385-337">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="29385-337">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="29385-338">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="29385-338">Parameters - addDataField</span></span>

<span data-ttu-id="29385-339">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="29385-339">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="29385-340">fieldId</span><span class="sxs-lookup"><span data-stu-id="29385-340">fieldId</span></span>  

<!-- -->

<span data-ttu-id="29385-341">insertAfter</span><span class="sxs-lookup"><span data-stu-id="29385-341">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="29385-342">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="29385-342">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="29385-343">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="29385-343">Return Value - addDataField</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="29385-344">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="29385-344">Method alignControl</span></span>

<span data-ttu-id="29385-345">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-345">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="29385-346">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="29385-346">Parameters - alignControl</span></span>

<span data-ttu-id="29385-347">値</span><span class="sxs-lookup"><span data-stu-id="29385-347">value</span></span>  
<span data-ttu-id="29385-348">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-348">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="29385-349">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="29385-349">Return Value - alignControl</span></span>

<span data-ttu-id="29385-350">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="29385-350">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="29385-351">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="29385-351">Remarks - alignControl</span></span>

<span data-ttu-id="29385-352">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="29385-352">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="29385-353">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="29385-353">Method allowEdit</span></span>

<span data-ttu-id="29385-354">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-354">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="29385-355">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="29385-355">Parameters - allowEdit</span></span>

<span data-ttu-id="29385-356">値</span><span class="sxs-lookup"><span data-stu-id="29385-356">value</span></span>  
<span data-ttu-id="29385-357">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="29385-357">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="29385-358">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="29385-358">Return Value - allowEdit</span></span>

<span data-ttu-id="29385-359">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-359">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="29385-360">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="29385-360">Remarks - allowEdit</span></span>

<span data-ttu-id="29385-361">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="29385-361">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="29385-362">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="29385-362">Method allowSysSetup</span></span>

<span data-ttu-id="29385-363">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-363">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="29385-364">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="29385-364">Return Value - allowSysSetup</span></span>

<span data-ttu-id="29385-365">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-365">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="29385-366">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="29385-366">Method autoDeclaration</span></span>

<span data-ttu-id="29385-367">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-367">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="29385-368">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="29385-368">Parameters - autoDeclaration</span></span>

<span data-ttu-id="29385-369">値</span><span class="sxs-lookup"><span data-stu-id="29385-369">value</span></span>  
<span data-ttu-id="29385-370">指定されている場合、プロパティはこの値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="29385-370">If supplied, the property is set to this value.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="29385-371">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="29385-371">Return Value - autoDeclaration</span></span>

<span data-ttu-id="29385-372">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-372">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="29385-373">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="29385-373">Remarks - autoDeclaration</span></span>

<span data-ttu-id="29385-374">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="29385-374">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="29385-375">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="29385-375">Method backgroundColor</span></span>

<span data-ttu-id="29385-376">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-376">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="29385-377">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="29385-377">Parameters - backgroundColor</span></span>

<span data-ttu-id="29385-378">値</span><span class="sxs-lookup"><span data-stu-id="29385-378">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="29385-379">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="29385-379">Return Value - backgroundColor</span></span>

<span data-ttu-id="29385-380">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="29385-380">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="29385-381">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="29385-381">Remarks - backgroundColor</span></span>

<span data-ttu-id="29385-382">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="29385-382">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="29385-383">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="29385-383">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="29385-384">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="29385-384">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="29385-385">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="29385-385">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="29385-386">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="29385-386">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="29385-387">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="29385-387">The maximum value for a single byte is 255.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="29385-388">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="29385-388">Method beginDrag</span></span>

<span data-ttu-id="29385-389">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-389">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="29385-390">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="29385-390">Parameters - beginDrag</span></span>

<span data-ttu-id="29385-391">x</span><span class="sxs-lookup"><span data-stu-id="29385-391">x</span></span>  
<span data-ttu-id="29385-392">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-392">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="29385-393">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="29385-393">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="29385-394">y</span><span class="sxs-lookup"><span data-stu-id="29385-394">y</span></span>  
<span data-ttu-id="29385-395">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-395">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="29385-396">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="29385-396">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="29385-397">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="29385-397">Return Value - beginDrag</span></span>

<span data-ttu-id="29385-398">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="29385-398">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="29385-399">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="29385-399">Remarks - beginDrag</span></span>

<span data-ttu-id="29385-400">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="29385-400">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="29385-401">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="29385-401">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="29385-402">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="29385-402">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="29385-403">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="29385-403">Parameters - bottomMargin</span></span>

<span data-ttu-id="29385-404">値</span><span class="sxs-lookup"><span data-stu-id="29385-404">value</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="29385-405">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="29385-405">Return Value - bottomMargin</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="29385-406">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="29385-406">Method calcControlSize</span></span>

<span data-ttu-id="29385-407">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-407">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="29385-408">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="29385-408">Parameters - calcControlSize</span></span>

<span data-ttu-id="29385-409">chars</span><span class="sxs-lookup"><span data-stu-id="29385-409">chars</span></span>  
<span data-ttu-id="29385-410">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="29385-410">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="29385-411">明細行</span><span class="sxs-lookup"><span data-stu-id="29385-411">lines</span></span>  
<span data-ttu-id="29385-412">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="29385-412">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="29385-413">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="29385-413">Return Value - calcControlSize</span></span>

<span data-ttu-id="29385-414">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="29385-414">The container that holds the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="29385-415">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="29385-415">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="29385-416">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="29385-416">Parameters - canAddDataField</span></span>

<span data-ttu-id="29385-417">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="29385-417">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="29385-418">fieldId</span><span class="sxs-lookup"><span data-stu-id="29385-418">fieldId</span></span>  

<!-- -->

<span data-ttu-id="29385-419">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="29385-419">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="29385-420">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="29385-420">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="29385-421">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="29385-421">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="29385-422">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="29385-422">Parameters - canContain</span></span>

<span data-ttu-id="29385-423">control</span><span class="sxs-lookup"><span data-stu-id="29385-423">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="29385-424">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="29385-424">Return Value - canContain</span></span>

## <a name="method-cell"></a><span data-ttu-id="29385-425">メソッド cell</span><span class="sxs-lookup"><span data-stu-id="29385-425">Method cell</span></span>

```xpp
public FormTableCell cell([int column], [int row])
```

### <a name="parameters---cell"></a><span data-ttu-id="29385-426">パラメーター - cell</span><span class="sxs-lookup"><span data-stu-id="29385-426">Parameters - cell</span></span>

<span data-ttu-id="29385-427">column</span><span class="sxs-lookup"><span data-stu-id="29385-427">column</span></span>  

<!-- -->

<span data-ttu-id="29385-428"> 行 </span><span class="sxs-lookup"><span data-stu-id="29385-428">row</span></span>  

### <a name="return-value---cell"></a><span data-ttu-id="29385-429">戻り値 - cell</span><span class="sxs-lookup"><span data-stu-id="29385-429">Return Value - cell</span></span>

## <a name="method-collabel"></a><span data-ttu-id="29385-430">メソッド colLabel</span><span class="sxs-lookup"><span data-stu-id="29385-430">Method colLabel</span></span>

```xpp
public str colLabel(int column)
```

### <a name="parameters---collabel"></a><span data-ttu-id="29385-431">パラメーター - colLabel</span><span class="sxs-lookup"><span data-stu-id="29385-431">Parameters - colLabel</span></span>

<span data-ttu-id="29385-432">column</span><span class="sxs-lookup"><span data-stu-id="29385-432">column</span></span>  

### <a name="return-value---collabel"></a><span data-ttu-id="29385-433">戻り値 - colLabel</span><span class="sxs-lookup"><span data-stu-id="29385-433">Return Value - colLabel</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="29385-434">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="29385-434">Method colorScheme</span></span>

<span data-ttu-id="29385-435">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-435">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="29385-436">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="29385-436">Parameters - colorScheme</span></span>

<span data-ttu-id="29385-437">値</span><span class="sxs-lookup"><span data-stu-id="29385-437">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="29385-438">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="29385-438">Return Value - colorScheme</span></span>

<span data-ttu-id="29385-439">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="29385-439">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="29385-440">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="29385-440">Remarks - colorScheme</span></span>

<span data-ttu-id="29385-441">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="29385-441">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="29385-442">金額</span><span class="sxs-lookup"><span data-stu-id="29385-442">Value</span></span> | <span data-ttu-id="29385-443">スタイル</span><span class="sxs-lookup"><span data-stu-id="29385-443">Style</span></span>                        |
|-------|------------------------------|
| <span data-ttu-id="29385-444">0</span><span class="sxs-lookup"><span data-stu-id="29385-444">0</span></span>     | <span data-ttu-id="29385-445">既定</span><span class="sxs-lookup"><span data-stu-id="29385-445">Default</span></span>                      |
| <span data-ttu-id="29385-446">1</span><span class="sxs-lookup"><span data-stu-id="29385-446">1</span></span>     | <span data-ttu-id="29385-447">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="29385-447">The Microsoft Windows palette</span></span> |
| <span data-ttu-id="29385-448">2</span><span class="sxs-lookup"><span data-stu-id="29385-448">2</span></span>     | <span data-ttu-id="29385-449">真の配色</span><span class="sxs-lookup"><span data-stu-id="29385-449">The true-color scheme</span></span>        |

## <a name="method-column"></a><span data-ttu-id="29385-450">メソッド column</span><span class="sxs-lookup"><span data-stu-id="29385-450">Method column</span></span>

```xpp
public int column([int value])
```

### <a name="parameters---column"></a><span data-ttu-id="29385-451">パラメーター - column</span><span class="sxs-lookup"><span data-stu-id="29385-451">Parameters - column</span></span>

<span data-ttu-id="29385-452">値</span><span class="sxs-lookup"><span data-stu-id="29385-452">value</span></span>  

### <a name="return-value---column"></a><span data-ttu-id="29385-453">戻り値 - column</span><span class="sxs-lookup"><span data-stu-id="29385-453">Return Value - column</span></span>

## <a name="method-columns"></a><span data-ttu-id="29385-454">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="29385-454">Method columns</span></span>

```xpp
public int columns([int value])
```

### <a name="parameters---columns"></a><span data-ttu-id="29385-455">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="29385-455">Parameters - columns</span></span>

<span data-ttu-id="29385-456">値</span><span class="sxs-lookup"><span data-stu-id="29385-456">value</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="29385-457">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="29385-457">Return Value - columns</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="29385-458">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="29385-458">Method configurationKey</span></span>

<span data-ttu-id="29385-459">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-459">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="29385-460">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="29385-460">Parameters - configurationKey</span></span>

<span data-ttu-id="29385-461">値</span><span class="sxs-lookup"><span data-stu-id="29385-461">value</span></span>  
<span data-ttu-id="29385-462">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-462">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="29385-463">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="29385-463">Return Value - configurationKey</span></span>

<span data-ttu-id="29385-464">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="29385-464">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="29385-465">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="29385-465">Remarks - configurationKey</span></span>

<span data-ttu-id="29385-466">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="29385-466">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="29385-467">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="29385-467">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="29385-468">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="29385-468">Method configurationKeyEx</span></span>

<span data-ttu-id="29385-469">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-469">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="29385-470">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="29385-470">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="29385-471">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="29385-471">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="29385-472">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="29385-472">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="29385-473">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="29385-473">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="29385-474">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="29385-474">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="29385-475">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="29385-475">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-contains"></a><span data-ttu-id="29385-476">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="29385-476">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="29385-477">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="29385-477">Parameters - contains</span></span>

<span data-ttu-id="29385-478">control</span><span class="sxs-lookup"><span data-stu-id="29385-478">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="29385-479">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="29385-479">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="29385-480">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="29385-480">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="29385-481">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="29385-481">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="29385-482">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="29385-482">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="29385-483">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="29385-483">Parameters - controlNum</span></span>

<span data-ttu-id="29385-484">controlNo</span><span class="sxs-lookup"><span data-stu-id="29385-484">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="29385-485">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="29385-485">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="29385-486">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="29385-486">Method countryRegionCodes</span></span>

<span data-ttu-id="29385-487">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-487">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="29385-488">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="29385-488">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="29385-489">値</span><span class="sxs-lookup"><span data-stu-id="29385-489">value</span></span>  
<span data-ttu-id="29385-490">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-490">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="29385-491">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="29385-491">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="29385-492">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="29385-492">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-data"></a><span data-ttu-id="29385-493">メソッド data</span><span class="sxs-lookup"><span data-stu-id="29385-493">Method data</span></span>

```xpp
public AnyType data(int column, int row)
```

### <a name="parameters---data"></a><span data-ttu-id="29385-494">パラメーター - data</span><span class="sxs-lookup"><span data-stu-id="29385-494">Parameters - data</span></span>

<span data-ttu-id="29385-495">column</span><span class="sxs-lookup"><span data-stu-id="29385-495">column</span></span>  

<!-- -->

<span data-ttu-id="29385-496"> 行 </span><span class="sxs-lookup"><span data-stu-id="29385-496">row</span></span>  

### <a name="return-value---data"></a><span data-ttu-id="29385-497">戻り値 - data</span><span class="sxs-lookup"><span data-stu-id="29385-497">Return Value - data</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="29385-498">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="29385-498">Method dataRelationPath</span></span>

<span data-ttu-id="29385-499">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-499">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="29385-500">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="29385-500">Parameters - dataRelationPath</span></span>

<span data-ttu-id="29385-501">値</span><span class="sxs-lookup"><span data-stu-id="29385-501">value</span></span>  
<span data-ttu-id="29385-502">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-502">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="29385-503">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="29385-503">Return Value - dataRelationPath</span></span>

<span data-ttu-id="29385-504">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="29385-504">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="29385-505">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="29385-505">Remarks - dataRelationPath</span></span>

<span data-ttu-id="29385-506">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="29385-506">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="29385-507">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="29385-507">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="29385-508">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="29385-508">Method displayTarget</span></span>

<span data-ttu-id="29385-509">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-509">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="29385-510">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="29385-510">Parameters - displayTarget</span></span>

<span data-ttu-id="29385-511">値</span><span class="sxs-lookup"><span data-stu-id="29385-511">value</span></span>  
<span data-ttu-id="29385-512">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-512">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="29385-513">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="29385-513">Return Value - displayTarget</span></span>

<span data-ttu-id="29385-514">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="29385-514">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="29385-515">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="29385-515">Method dragDrop</span></span>

<span data-ttu-id="29385-516">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-516">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="29385-517">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="29385-517">Parameters - dragDrop</span></span>

<span data-ttu-id="29385-518">値</span><span class="sxs-lookup"><span data-stu-id="29385-518">value</span></span>  
<span data-ttu-id="29385-519">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-519">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="29385-520">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="29385-520">Return Value - dragDrop</span></span>

<span data-ttu-id="29385-521">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="29385-521">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="29385-522">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="29385-522">Remarks - dragDrop</span></span>

<span data-ttu-id="29385-523">dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="29385-523">Use the dragLeave Method, the dragOver Method, and the dragOverEx Method to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="29385-524">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="29385-524">Method dragOver</span></span>

<span data-ttu-id="29385-525">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-525">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="29385-526">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="29385-526">Parameters - dragOver</span></span>

<span data-ttu-id="29385-527">dragSource</span><span class="sxs-lookup"><span data-stu-id="29385-527">dragSource</span></span>  
<span data-ttu-id="29385-528">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-528">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-529">dragMode</span><span class="sxs-lookup"><span data-stu-id="29385-529">dragMode</span></span>  
<span data-ttu-id="29385-530">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-530">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-531">x</span><span class="sxs-lookup"><span data-stu-id="29385-531">x</span></span>  
<span data-ttu-id="29385-532">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-532">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-533">y</span><span class="sxs-lookup"><span data-stu-id="29385-533">y</span></span>  
<span data-ttu-id="29385-534">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-534">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="29385-535">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="29385-535">Return Value - dragOver</span></span>

<span data-ttu-id="29385-536">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="29385-536">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="29385-537">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="29385-537">Method dragOverEx</span></span>

<span data-ttu-id="29385-538">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-538">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="29385-539">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="29385-539">Parameters - dragOverEx</span></span>

<span data-ttu-id="29385-540">dragSource</span><span class="sxs-lookup"><span data-stu-id="29385-540">dragSource</span></span>  
<span data-ttu-id="29385-541">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-541">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-542">dragMode</span><span class="sxs-lookup"><span data-stu-id="29385-542">dragMode</span></span>  
<span data-ttu-id="29385-543">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-543">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-544">x</span><span class="sxs-lookup"><span data-stu-id="29385-544">x</span></span>  
<span data-ttu-id="29385-545">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-545">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-546">y</span><span class="sxs-lookup"><span data-stu-id="29385-546">y</span></span>  
<span data-ttu-id="29385-547">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-547">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="29385-548">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="29385-548">Return Value - dragOverEx</span></span>

<span data-ttu-id="29385-549">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="29385-549">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="29385-550">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="29385-550">Method dragText</span></span>

<span data-ttu-id="29385-551">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-551">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="29385-552">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="29385-552">Return Value - dragText</span></span>

<span data-ttu-id="29385-553">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="29385-553">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-editcontrol"></a><span data-ttu-id="29385-554">メソッド editControl</span><span class="sxs-lookup"><span data-stu-id="29385-554">Method editControl</span></span>

```xpp
public FormControl editControl(int Column, int Row)
```

### <a name="parameters---editcontrol"></a><span data-ttu-id="29385-555">パラメーター - editControl</span><span class="sxs-lookup"><span data-stu-id="29385-555">Parameters - editControl</span></span>

<span data-ttu-id="29385-556">円柱</span><span class="sxs-lookup"><span data-stu-id="29385-556">Column</span></span>  

<!-- -->

<span data-ttu-id="29385-557">行</span><span class="sxs-lookup"><span data-stu-id="29385-557">Row</span></span>  

### <a name="return-value---editcontrol"></a><span data-ttu-id="29385-558">戻り値 - editControl</span><span class="sxs-lookup"><span data-stu-id="29385-558">Return Value - editControl</span></span>

## <a name="method-enabled"></a><span data-ttu-id="29385-559">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="29385-559">Method enabled</span></span>

<span data-ttu-id="29385-560">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29385-560">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="29385-561">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="29385-561">Parameters - enabled</span></span>

<span data-ttu-id="29385-562">値</span><span class="sxs-lookup"><span data-stu-id="29385-562">value</span></span>  
<span data-ttu-id="29385-563">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-563">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="29385-564">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="29385-564">Return Value - enabled</span></span>

<span data-ttu-id="29385-565">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-565">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="29385-566">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="29385-566">Remarks - enabled</span></span>

<span data-ttu-id="29385-567">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="29385-567">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="29385-568">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="29385-568">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="29385-569">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="29385-569">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-gridlines"></a><span data-ttu-id="29385-570">メソッド gridLines</span><span class="sxs-lookup"><span data-stu-id="29385-570">Method gridLines</span></span>

```xpp
public boolean gridLines([boolean value])
```

### <a name="parameters---gridlines"></a><span data-ttu-id="29385-571">パラメーター - gridLines</span><span class="sxs-lookup"><span data-stu-id="29385-571">Parameters - gridLines</span></span>

<span data-ttu-id="29385-572">値</span><span class="sxs-lookup"><span data-stu-id="29385-572">value</span></span>  

### <a name="return-value---gridlines"></a><span data-ttu-id="29385-573">戻り値 - gridLines</span><span class="sxs-lookup"><span data-stu-id="29385-573">Return Value - gridLines</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="29385-574">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="29385-574">Method hasChanged</span></span>

<span data-ttu-id="29385-575">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-575">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="29385-576">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="29385-576">Parameters - hasChanged</span></span>

<span data-ttu-id="29385-577">val</span><span class="sxs-lookup"><span data-stu-id="29385-577">val</span></span>  
<span data-ttu-id="29385-578">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-578">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="29385-579">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="29385-579">Return Value - hasChanged</span></span>

<span data-ttu-id="29385-580">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-580">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="29385-581">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="29385-581">Method hasUserSetting</span></span>

<span data-ttu-id="29385-582">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="29385-582">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="29385-583">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="29385-583">Return Value - hasUserSetting</span></span>

<span data-ttu-id="29385-584">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-584">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="29385-585">メソッド height</span><span class="sxs-lookup"><span data-stu-id="29385-585">Method height</span></span>

<span data-ttu-id="29385-586">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-586">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="29385-587">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="29385-587">Parameters - height</span></span>

<span data-ttu-id="29385-588">値</span><span class="sxs-lookup"><span data-stu-id="29385-588">value</span></span>  
<span data-ttu-id="29385-589">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-589">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="29385-590">モード</span><span class="sxs-lookup"><span data-stu-id="29385-590">mode</span></span>  
<span data-ttu-id="29385-591">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-591">An integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="29385-592">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="29385-592">Return Value - height</span></span>

<span data-ttu-id="29385-593">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="29385-593">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="29385-594">備考 - height</span><span class="sxs-lookup"><span data-stu-id="29385-594">Remarks - height</span></span>

<span data-ttu-id="29385-595">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29385-595">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="29385-596">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="29385-596">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="29385-597">モード</span><span class="sxs-lookup"><span data-stu-id="29385-597">Mode</span></span>            | <span data-ttu-id="29385-598">高さの計算</span><span class="sxs-lookup"><span data-stu-id="29385-598">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="29385-599">-1 正確</span><span class="sxs-lookup"><span data-stu-id="29385-599">-1 Exact</span></span>        | <span data-ttu-id="29385-600">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29385-600">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="29385-601">0 自動</span><span class="sxs-lookup"><span data-stu-id="29385-601">0 Auto</span></span>          | <span data-ttu-id="29385-602">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="29385-602">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="29385-603">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="29385-603">1 Column height</span></span> | <span data-ttu-id="29385-604">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="29385-604">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="29385-605">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="29385-605">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="29385-606">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="29385-606">Method heightMode</span></span>

<span data-ttu-id="29385-607">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-607">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="29385-608">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="29385-608">Parameters - heightMode</span></span>

<span data-ttu-id="29385-609">値</span><span class="sxs-lookup"><span data-stu-id="29385-609">value</span></span>  
<span data-ttu-id="29385-610">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-610">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="29385-611">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="29385-611">Return Value - heightMode</span></span>

<span data-ttu-id="29385-612">計算モード。</span><span class="sxs-lookup"><span data-stu-id="29385-612">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="29385-613">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="29385-613">Remarks - heightMode</span></span>

<span data-ttu-id="29385-614">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="29385-614">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="29385-615">モード</span><span class="sxs-lookup"><span data-stu-id="29385-615">Mode</span></span>          | <span data-ttu-id="29385-616">高さの計算</span><span class="sxs-lookup"><span data-stu-id="29385-616">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="29385-617">正確</span><span class="sxs-lookup"><span data-stu-id="29385-617">Exact</span></span>         | <span data-ttu-id="29385-618">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29385-618">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="29385-619">自動</span><span class="sxs-lookup"><span data-stu-id="29385-619">Auto</span></span>          | <span data-ttu-id="29385-620">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="29385-620">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="29385-621">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="29385-621">Column height</span></span> | <span data-ttu-id="29385-622">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="29385-622">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="29385-623">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="29385-623">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="29385-624">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="29385-624">Method heightValue</span></span>

<span data-ttu-id="29385-625">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-625">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="29385-626">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="29385-626">Parameters - heightValue</span></span>

<span data-ttu-id="29385-627">値</span><span class="sxs-lookup"><span data-stu-id="29385-627">value</span></span>  
<span data-ttu-id="29385-628">高さをピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-628">An integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="29385-629">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="29385-629">Return Value - heightValue</span></span>

<span data-ttu-id="29385-630">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="29385-630">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="29385-631">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="29385-631">Remarks - heightValue</span></span>

<span data-ttu-id="29385-632">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="29385-632">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="29385-633">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="29385-633">Method helpField</span></span>

<span data-ttu-id="29385-634">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-634">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="29385-635">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="29385-635">Return Value - helpField</span></span>

<span data-ttu-id="29385-636">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="29385-636">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="29385-637">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="29385-637">Remarks - helpField</span></span>

<span data-ttu-id="29385-638">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="29385-638">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="29385-639">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="29385-639">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="29385-640">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="29385-640">Method helpText</span></span>

<span data-ttu-id="29385-641">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-641">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="29385-642">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="29385-642">Parameters - helpText</span></span>

<span data-ttu-id="29385-643">値</span><span class="sxs-lookup"><span data-stu-id="29385-643">value</span></span>  
<span data-ttu-id="29385-644">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="29385-644">The value to assign as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="29385-645">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="29385-645">Return Value - helpText</span></span>

<span data-ttu-id="29385-646">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="29385-646">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="29385-647">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="29385-647">Remarks - helpText</span></span>

<span data-ttu-id="29385-648">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-648">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="29385-649">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="29385-649">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="29385-650">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="29385-650">Method hierarchyParent</span></span>

<span data-ttu-id="29385-651">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-651">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="29385-652">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="29385-652">Parameters - hierarchyParent</span></span>

<span data-ttu-id="29385-653">値</span><span class="sxs-lookup"><span data-stu-id="29385-653">value</span></span>  
<span data-ttu-id="29385-654">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="29385-654">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="29385-655">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="29385-655">Return Value - hierarchyParent</span></span>

<span data-ttu-id="29385-656">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="29385-656">The HierarchyParent property value of the control.</span></span>

## <a name="method-highlightactive"></a><span data-ttu-id="29385-657">メソッド highlightActive</span><span class="sxs-lookup"><span data-stu-id="29385-657">Method highlightActive</span></span>

```xpp
public boolean highlightActive([boolean value])
```

### <a name="parameters---highlightactive"></a><span data-ttu-id="29385-658">パラメーター - highlightActive</span><span class="sxs-lookup"><span data-stu-id="29385-658">Parameters - highlightActive</span></span>

<span data-ttu-id="29385-659">値</span><span class="sxs-lookup"><span data-stu-id="29385-659">value</span></span>  

### <a name="return-value---highlightactive"></a><span data-ttu-id="29385-660">戻り値 - highlightActive</span><span class="sxs-lookup"><span data-stu-id="29385-660">Return Value - highlightActive</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="29385-661">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="29385-661">Method hWnd</span></span>

<span data-ttu-id="29385-662">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-662">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="29385-663">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="29385-663">Return Value - hWnd</span></span>

<span data-ttu-id="29385-664">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="29385-664">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="29385-665">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="29385-665">Remarks - hWnd</span></span>

<span data-ttu-id="29385-666">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="29385-666">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="29385-667">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="29385-667">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="29385-668">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="29385-668">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="29385-669">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="29385-669">Method isDisplayed</span></span>

<span data-ttu-id="29385-670">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-670">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="29385-671">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="29385-671">Return Value - isDisplayed</span></span>

<span data-ttu-id="29385-672">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="29385-672">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="29385-673">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="29385-673">Remarks - isDisplayed</span></span>

<span data-ttu-id="29385-674">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="29385-674">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="29385-675">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="29385-675">Method isRestricted</span></span>

<span data-ttu-id="29385-676">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-676">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="29385-677">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="29385-677">Return Value - isRestricted</span></span>

<span data-ttu-id="29385-678">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="29385-678">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="29385-679">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="29385-679">Method isUserSetupEnabled</span></span>

<span data-ttu-id="29385-680">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-680">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="29385-681">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="29385-681">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="29385-682">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="29385-682">neededSetupRights</span></span>  
<span data-ttu-id="29385-683">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="29385-683">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="29385-684">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="29385-684">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="29385-685">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-685">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="29385-686">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="29385-686">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="29385-687">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="29385-687">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29385-688">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="29385-688">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="29385-689">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="29385-689">No changes can be made to the control.</span></span> <span data-ttu-id="29385-690">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="29385-690">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="29385-691">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="29385-691">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="29385-692">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="29385-692">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="29385-693">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="29385-693">The user cannot move the control.</span></span>   |
| <span data-ttu-id="29385-694">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="29385-694">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="29385-695">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="29385-695">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="29385-696">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="29385-696">The user can also move the control.</span></span> |

<span data-ttu-id="29385-697">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="29385-697">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-leave"></a><span data-ttu-id="29385-698">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="29385-698">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="29385-699">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="29385-699">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="29385-700">メソッド left</span><span class="sxs-lookup"><span data-stu-id="29385-700">Method left</span></span>

<span data-ttu-id="29385-701">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-701">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="29385-702">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="29385-702">Parameters - left</span></span>

<span data-ttu-id="29385-703">値</span><span class="sxs-lookup"><span data-stu-id="29385-703">value</span></span>  
<span data-ttu-id="29385-704">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-704">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="29385-705">モード</span><span class="sxs-lookup"><span data-stu-id="29385-705">mode</span></span>  
<span data-ttu-id="29385-706">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-706">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="29385-707">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="29385-707">Return Value - left</span></span>

<span data-ttu-id="29385-708">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="29385-708">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="29385-709">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="29385-709">Method leftMargin</span></span>

```xpp
public int leftMargin([int value])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="29385-710">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="29385-710">Parameters - leftMargin</span></span>

<span data-ttu-id="29385-711">値</span><span class="sxs-lookup"><span data-stu-id="29385-711">value</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="29385-712">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="29385-712">Return Value - leftMargin</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="29385-713">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="29385-713">Method leftMode</span></span>

<span data-ttu-id="29385-714">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-714">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="29385-715">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="29385-715">Parameters - leftMode</span></span>

<span data-ttu-id="29385-716">値</span><span class="sxs-lookup"><span data-stu-id="29385-716">value</span></span>  
<span data-ttu-id="29385-717">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-717">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="29385-718">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="29385-718">Return Value - leftMode</span></span>

<span data-ttu-id="29385-719">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="29385-719">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="29385-720">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="29385-720">Method leftValue</span></span>

<span data-ttu-id="29385-721">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-721">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="29385-722">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="29385-722">Parameters - leftValue</span></span>

<span data-ttu-id="29385-723">値</span><span class="sxs-lookup"><span data-stu-id="29385-723">value</span></span>  
<span data-ttu-id="29385-724">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-724">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="29385-725">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="29385-725">Return Value - leftValue</span></span>

<span data-ttu-id="29385-726">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="29385-726">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="29385-727">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="29385-727">Method markAsUserAdd</span></span>

<span data-ttu-id="29385-728">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="29385-728">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="29385-729">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="29385-729">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="29385-730">値</span><span class="sxs-lookup"><span data-stu-id="29385-730">value</span></span>  
<span data-ttu-id="29385-731">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-731">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="29385-732">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="29385-732">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="29385-733">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-733">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="29385-734">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="29385-734">Method mouseDblClick</span></span>

<span data-ttu-id="29385-735">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-735">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="29385-736">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="29385-736">Parameters - mouseDblClick</span></span>

<span data-ttu-id="29385-737">x</span><span class="sxs-lookup"><span data-stu-id="29385-737">x</span></span>  
<span data-ttu-id="29385-738">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-738">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-739">y</span><span class="sxs-lookup"><span data-stu-id="29385-739">y</span></span>  
<span data-ttu-id="29385-740">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-740">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-741">ボタン</span><span class="sxs-lookup"><span data-stu-id="29385-741">button</span></span>  
<span data-ttu-id="29385-742">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-742">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-743">Ctrl</span><span class="sxs-lookup"><span data-stu-id="29385-743">Ctrl</span></span>  
<span data-ttu-id="29385-744">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-744">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-745">シフト</span><span class="sxs-lookup"><span data-stu-id="29385-745">Shift</span></span>  
<span data-ttu-id="29385-746">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-746">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="29385-747">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="29385-747">Return Value - mouseDblClick</span></span>

<span data-ttu-id="29385-748">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="29385-748">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="29385-749">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="29385-749">Remarks - mouseDblClick</span></span>

<span data-ttu-id="29385-750">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="29385-750">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="29385-751">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="29385-751">Method mouseDown</span></span>

<span data-ttu-id="29385-752">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-752">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="29385-753">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="29385-753">Parameters - mouseDown</span></span>

<span data-ttu-id="29385-754">x</span><span class="sxs-lookup"><span data-stu-id="29385-754">x</span></span>  
<span data-ttu-id="29385-755">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-755">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-756">y</span><span class="sxs-lookup"><span data-stu-id="29385-756">y</span></span>  
<span data-ttu-id="29385-757">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-757">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-758">ボタン</span><span class="sxs-lookup"><span data-stu-id="29385-758">button</span></span>  
<span data-ttu-id="29385-759">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-759">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-760">Ctrl</span><span class="sxs-lookup"><span data-stu-id="29385-760">Ctrl</span></span>  
<span data-ttu-id="29385-761">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-761">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-762">シフト</span><span class="sxs-lookup"><span data-stu-id="29385-762">Shift</span></span>  
<span data-ttu-id="29385-763">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-763">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="29385-764">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="29385-764">Return Value - mouseDown</span></span>

<span data-ttu-id="29385-765">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="29385-765">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="29385-766">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="29385-766">Remarks - mouseDown</span></span>

<span data-ttu-id="29385-767">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="29385-767">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="29385-768">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-768">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="29385-769">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="29385-769">Method mouseMove</span></span>

<span data-ttu-id="29385-770">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-770">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="29385-771">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="29385-771">Parameters - mouseMove</span></span>

<span data-ttu-id="29385-772">x</span><span class="sxs-lookup"><span data-stu-id="29385-772">x</span></span>  
<span data-ttu-id="29385-773">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-773">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-774">y</span><span class="sxs-lookup"><span data-stu-id="29385-774">y</span></span>  
<span data-ttu-id="29385-775">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-775">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-776">ボタン</span><span class="sxs-lookup"><span data-stu-id="29385-776">button</span></span>  
<span data-ttu-id="29385-777">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-777">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-778">Ctrl</span><span class="sxs-lookup"><span data-stu-id="29385-778">Ctrl</span></span>  
<span data-ttu-id="29385-779">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-779">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-780">シフト</span><span class="sxs-lookup"><span data-stu-id="29385-780">Shift</span></span>  
<span data-ttu-id="29385-781">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-781">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="29385-782">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="29385-782">Return Value - mouseMove</span></span>

<span data-ttu-id="29385-783">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="29385-783">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="29385-784">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="29385-784">Remarks - mouseMove</span></span>

<span data-ttu-id="29385-785">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="29385-785">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="29385-786">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="29385-786">Method mouseUp</span></span>

<span data-ttu-id="29385-787">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-787">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="29385-788">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="29385-788">Parameters - mouseUp</span></span>

<span data-ttu-id="29385-789">x</span><span class="sxs-lookup"><span data-stu-id="29385-789">x</span></span>  
<span data-ttu-id="29385-790">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-790">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-791">y</span><span class="sxs-lookup"><span data-stu-id="29385-791">y</span></span>  
<span data-ttu-id="29385-792">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-792">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-793">ボタン</span><span class="sxs-lookup"><span data-stu-id="29385-793">button</span></span>  
<span data-ttu-id="29385-794">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-794">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-795">Ctrl</span><span class="sxs-lookup"><span data-stu-id="29385-795">Ctrl</span></span>  
<span data-ttu-id="29385-796">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-796">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-797">シフト</span><span class="sxs-lookup"><span data-stu-id="29385-797">Shift</span></span>  
<span data-ttu-id="29385-798">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-798">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="29385-799">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="29385-799">Return Value - mouseUp</span></span>

<span data-ttu-id="29385-800">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="29385-800">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="29385-801">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="29385-801">Remarks - mouseUp</span></span>

<span data-ttu-id="29385-802">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="29385-802">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="29385-803">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-803">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="29385-804">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="29385-804">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="29385-805">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="29385-805">Parameters - moveControl</span></span>

<span data-ttu-id="29385-806">controlId</span><span class="sxs-lookup"><span data-stu-id="29385-806">controlId</span></span>  

<!-- -->

<span data-ttu-id="29385-807">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="29385-807">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="29385-808">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="29385-808">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="29385-809">メソッド名</span><span class="sxs-lookup"><span data-stu-id="29385-809">Method name</span></span>

<span data-ttu-id="29385-810">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-810">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="29385-811">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="29385-811">Parameters - name</span></span>

<span data-ttu-id="29385-812">値</span><span class="sxs-lookup"><span data-stu-id="29385-812">value</span></span>  
<span data-ttu-id="29385-813">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="29385-813">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="29385-814">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="29385-814">Return Value - name</span></span>

<span data-ttu-id="29385-815">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="29385-815">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="29385-816">備考 - name</span><span class="sxs-lookup"><span data-stu-id="29385-816">Remarks - name</span></span>

<span data-ttu-id="29385-817">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="29385-817">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="29385-818">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="29385-818">Begins with a letter.</span></span>
-   <span data-ttu-id="29385-819">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="29385-819">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="29385-820">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="29385-820">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="29385-821">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="29385-821">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="29385-822">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="29385-822">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="29385-823">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="29385-823">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="29385-824">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="29385-824">Parameters - neededPermission</span></span>

<span data-ttu-id="29385-825">値</span><span class="sxs-lookup"><span data-stu-id="29385-825">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="29385-826">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="29385-826">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="29385-827">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="29385-827">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="29385-828">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="29385-828">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="29385-829">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="29385-829">Method parentControl</span></span>

<span data-ttu-id="29385-830">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-830">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="29385-831">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="29385-831">Return Value - parentControl</span></span>

<span data-ttu-id="29385-832">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="29385-832">The parent control for the control.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="29385-833">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="29385-833">Method rightMargin</span></span>

```xpp
public int rightMargin([int value])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="29385-834">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="29385-834">Parameters - rightMargin</span></span>

<span data-ttu-id="29385-835">値</span><span class="sxs-lookup"><span data-stu-id="29385-835">value</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="29385-836">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="29385-836">Return Value - rightMargin</span></span>

## <a name="method-row"></a><span data-ttu-id="29385-837">メソッド row</span><span class="sxs-lookup"><span data-stu-id="29385-837">Method row</span></span>

```xpp
public int row([int value])
```

### <a name="parameters---row"></a><span data-ttu-id="29385-838">パラメーター - row</span><span class="sxs-lookup"><span data-stu-id="29385-838">Parameters - row</span></span>

<span data-ttu-id="29385-839">値</span><span class="sxs-lookup"><span data-stu-id="29385-839">value</span></span>  

### <a name="return-value---row"></a><span data-ttu-id="29385-840">戻り値 - row</span><span class="sxs-lookup"><span data-stu-id="29385-840">Return Value - row</span></span>

## <a name="method-rowlabel"></a><span data-ttu-id="29385-841">メソッド rowLabel</span><span class="sxs-lookup"><span data-stu-id="29385-841">Method rowLabel</span></span>

```xpp
public str rowLabel(int row)
```

### <a name="parameters---rowlabel"></a><span data-ttu-id="29385-842">パラメーター - rowLabel</span><span class="sxs-lookup"><span data-stu-id="29385-842">Parameters - rowLabel</span></span>

<span data-ttu-id="29385-843"> 行 </span><span class="sxs-lookup"><span data-stu-id="29385-843">row</span></span>  

### <a name="return-value---rowlabel"></a><span data-ttu-id="29385-844">戻り値 - rowLabel</span><span class="sxs-lookup"><span data-stu-id="29385-844">Return Value - rowLabel</span></span>

## <a name="method-rows"></a><span data-ttu-id="29385-845">メソッド rows</span><span class="sxs-lookup"><span data-stu-id="29385-845">Method rows</span></span>

```xpp
public int rows([int value])
```

### <a name="parameters---rows"></a><span data-ttu-id="29385-846">パラメーター - rows</span><span class="sxs-lookup"><span data-stu-id="29385-846">Parameters - rows</span></span>

<span data-ttu-id="29385-847">値</span><span class="sxs-lookup"><span data-stu-id="29385-847">value</span></span>  

### <a name="return-value---rows"></a><span data-ttu-id="29385-848">戻り値 - rows</span><span class="sxs-lookup"><span data-stu-id="29385-848">Return Value - rows</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="29385-849">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="29385-849">Method securityKey</span></span>

<span data-ttu-id="29385-850">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-850">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="29385-851">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="29385-851">Parameters - securityKey</span></span>

<span data-ttu-id="29385-852">値</span><span class="sxs-lookup"><span data-stu-id="29385-852">value</span></span>  
<span data-ttu-id="29385-853">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-853">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="29385-854">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="29385-854">Return Value - securityKey</span></span>

<span data-ttu-id="29385-855">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="29385-855">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcollabels"></a><span data-ttu-id="29385-856">メソッド showColLabels</span><span class="sxs-lookup"><span data-stu-id="29385-856">Method showColLabels</span></span>

```xpp
public boolean showColLabels([boolean value])
```

### <a name="parameters---showcollabels"></a><span data-ttu-id="29385-857">パラメーター - showColLabels</span><span class="sxs-lookup"><span data-stu-id="29385-857">Parameters - showColLabels</span></span>

<span data-ttu-id="29385-858">値</span><span class="sxs-lookup"><span data-stu-id="29385-858">value</span></span>  

### <a name="return-value---showcollabels"></a><span data-ttu-id="29385-859">戻り値 - showColLabels</span><span class="sxs-lookup"><span data-stu-id="29385-859">Return Value - showColLabels</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="29385-860">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="29385-860">Method showContextMenu</span></span>

<span data-ttu-id="29385-861">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="29385-861">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="29385-862">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="29385-862">Parameters - showContextMenu</span></span>

<span data-ttu-id="29385-863">menuHandle</span><span class="sxs-lookup"><span data-stu-id="29385-863">menuHandle</span></span>  
<span data-ttu-id="29385-864">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="29385-864">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="29385-865">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="29385-865">Return Value - showContextMenu</span></span>

<span data-ttu-id="29385-866">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-866">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showrowlabels"></a><span data-ttu-id="29385-867">メソッド showRowLabels</span><span class="sxs-lookup"><span data-stu-id="29385-867">Method showRowLabels</span></span>

```xpp
public boolean showRowLabels([boolean value])
```

### <a name="parameters---showrowlabels"></a><span data-ttu-id="29385-868">パラメーター - showRowLabels</span><span class="sxs-lookup"><span data-stu-id="29385-868">Parameters - showRowLabels</span></span>

<span data-ttu-id="29385-869">値</span><span class="sxs-lookup"><span data-stu-id="29385-869">value</span></span>  

### <a name="return-value---showrowlabels"></a><span data-ttu-id="29385-870">戻り値 - showRowLabels</span><span class="sxs-lookup"><span data-stu-id="29385-870">Return Value - showRowLabels</span></span>

## <a name="method-skip"></a><span data-ttu-id="29385-871">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="29385-871">Method skip</span></span>

<span data-ttu-id="29385-872">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-872">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="29385-873">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="29385-873">Parameters - skip</span></span>

<span data-ttu-id="29385-874">値</span><span class="sxs-lookup"><span data-stu-id="29385-874">value</span></span>  
<span data-ttu-id="29385-875">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-875">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="29385-876">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="29385-876">Return Value - skip</span></span>

<span data-ttu-id="29385-877">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29385-877">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="29385-878">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="29385-878">Remarks - skip</span></span>

<span data-ttu-id="29385-879">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="29385-879">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="29385-880">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="29385-880">Method toolTip</span></span>

<span data-ttu-id="29385-881">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="29385-881">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="29385-882">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="29385-882">Return Value - toolTip</span></span>

<span data-ttu-id="29385-883">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="29385-883">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="29385-884">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="29385-884">Remarks - toolTip</span></span>

<span data-ttu-id="29385-885">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="29385-885">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="29385-886">メソッド top</span><span class="sxs-lookup"><span data-stu-id="29385-886">Method top</span></span>

<span data-ttu-id="29385-887">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-887">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="29385-888">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="29385-888">Parameters - top</span></span>

<span data-ttu-id="29385-889">値</span><span class="sxs-lookup"><span data-stu-id="29385-889">value</span></span>  
<span data-ttu-id="29385-890">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-890">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="29385-891">モード</span><span class="sxs-lookup"><span data-stu-id="29385-891">mode</span></span>  
<span data-ttu-id="29385-892">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-892">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="29385-893">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="29385-893">Return Value - top</span></span>

<span data-ttu-id="29385-894">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="29385-894">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="29385-895">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="29385-895">Method topMargin</span></span>

```xpp
public int topMargin([int value])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="29385-896">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="29385-896">Parameters - topMargin</span></span>

<span data-ttu-id="29385-897">値</span><span class="sxs-lookup"><span data-stu-id="29385-897">value</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="29385-898">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="29385-898">Return Value - topMargin</span></span>

## <a name="method-topmode"></a><span data-ttu-id="29385-899">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="29385-899">Method topMode</span></span>

<span data-ttu-id="29385-900">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-900">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="29385-901">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="29385-901">Parameters - topMode</span></span>

<span data-ttu-id="29385-902">値</span><span class="sxs-lookup"><span data-stu-id="29385-902">value</span></span>  
<span data-ttu-id="29385-903">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-903">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="29385-904">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="29385-904">Return Value - topMode</span></span>

<span data-ttu-id="29385-905">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="29385-905">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="29385-906">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="29385-906">Method topValue</span></span>

<span data-ttu-id="29385-907">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-907">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="29385-908">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="29385-908">Parameters - topValue</span></span>

<span data-ttu-id="29385-909">値</span><span class="sxs-lookup"><span data-stu-id="29385-909">value</span></span>  
<span data-ttu-id="29385-910">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-910">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="29385-911">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="29385-911">Return Value - topValue</span></span>

<span data-ttu-id="29385-912">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="29385-912">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="29385-913">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="29385-913">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="29385-914">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="29385-914">Parameters - type</span></span>

<span data-ttu-id="29385-915">値</span><span class="sxs-lookup"><span data-stu-id="29385-915">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="29385-916">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="29385-916">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="29385-917">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="29385-917">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="29385-918">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="29385-918">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="29385-919">データ</span><span class="sxs-lookup"><span data-stu-id="29385-919">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="29385-920">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="29385-920">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="29385-921">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="29385-921">Method userData</span></span>

<span data-ttu-id="29385-922">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-922">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="29385-923">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="29385-923">Parameters - userData</span></span>

<span data-ttu-id="29385-924">値</span><span class="sxs-lookup"><span data-stu-id="29385-924">value</span></span>  
<span data-ttu-id="29385-925">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-925">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="29385-926">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="29385-926">Return Value - userData</span></span>

<span data-ttu-id="29385-927">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="29385-927">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="29385-928">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="29385-928">Method userDataItem</span></span>

<span data-ttu-id="29385-929">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-929">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="29385-930">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="29385-930">Parameters - userDataItem</span></span>

<span data-ttu-id="29385-931">値</span><span class="sxs-lookup"><span data-stu-id="29385-931">value</span></span>  
<span data-ttu-id="29385-932">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-932">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="29385-933">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="29385-933">Return Value - userDataItem</span></span>

<span data-ttu-id="29385-934">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="29385-934">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="29385-935">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="29385-935">Method userDataItems</span></span>

<span data-ttu-id="29385-936">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-936">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="29385-937">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="29385-937">Parameters - userDataItems</span></span>

<span data-ttu-id="29385-938">値</span><span class="sxs-lookup"><span data-stu-id="29385-938">value</span></span>  
<span data-ttu-id="29385-939">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-939">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="29385-940">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="29385-940">Return Value - userDataItems</span></span>

<span data-ttu-id="29385-941">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="29385-941">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="29385-942">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="29385-942">Method userDisable</span></span>

<span data-ttu-id="29385-943">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-943">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="29385-944">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="29385-944">Parameters - userDisable</span></span>

<span data-ttu-id="29385-945">値</span><span class="sxs-lookup"><span data-stu-id="29385-945">value</span></span>  
<span data-ttu-id="29385-946">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-946">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="29385-947">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="29385-947">Return Value - userDisable</span></span>

<span data-ttu-id="29385-948">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="29385-948">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="29385-949">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="29385-949">Method userHeight</span></span>

<span data-ttu-id="29385-950">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-950">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="29385-951">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="29385-951">Parameters - userHeight</span></span>

<span data-ttu-id="29385-952">値</span><span class="sxs-lookup"><span data-stu-id="29385-952">value</span></span>  
<span data-ttu-id="29385-953">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-953">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="29385-954">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="29385-954">Return Value - userHeight</span></span>

<span data-ttu-id="29385-955">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="29385-955">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="29385-956">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="29385-956">Method userHide</span></span>

<span data-ttu-id="29385-957">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-957">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="29385-958">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="29385-958">Parameters - userHide</span></span>

<span data-ttu-id="29385-959">値</span><span class="sxs-lookup"><span data-stu-id="29385-959">value</span></span>  
<span data-ttu-id="29385-960">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-960">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="29385-961">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="29385-961">Return Value - userHide</span></span>

<span data-ttu-id="29385-962">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="29385-962">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="29385-963">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="29385-963">Remarks - userHide</span></span>

<span data-ttu-id="29385-964">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="29385-964">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="29385-965">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="29385-965">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="29385-966">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="29385-966">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="29385-967">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="29385-967">Method userOrgContainer</span></span>

<span data-ttu-id="29385-968">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-968">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="29385-969">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="29385-969">Parameters - userOrgContainer</span></span>

<span data-ttu-id="29385-970">値</span><span class="sxs-lookup"><span data-stu-id="29385-970">value</span></span>  
<span data-ttu-id="29385-971">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-971">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="29385-972">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="29385-972">Return Value - userOrgContainer</span></span>

<span data-ttu-id="29385-973">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="29385-973">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="29385-974">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="29385-974">Method userOrgSibling</span></span>

<span data-ttu-id="29385-975">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-975">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="29385-976">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="29385-976">Parameters - userOrgSibling</span></span>

<span data-ttu-id="29385-977">値</span><span class="sxs-lookup"><span data-stu-id="29385-977">value</span></span>  
<span data-ttu-id="29385-978">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-978">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="29385-979">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="29385-979">Return Value - userOrgSibling</span></span>

<span data-ttu-id="29385-980">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="29385-980">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="29385-981">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="29385-981">Method userPromptText</span></span>

<span data-ttu-id="29385-982">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-982">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="29385-983">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="29385-983">Parameters - userPromptText</span></span>

<span data-ttu-id="29385-984">値</span><span class="sxs-lookup"><span data-stu-id="29385-984">value</span></span>  
<span data-ttu-id="29385-985">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-985">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="29385-986">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="29385-986">Return Value - userPromptText</span></span>

<span data-ttu-id="29385-987">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="29385-987">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="29385-988">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="29385-988">Method userSecurityLevel</span></span>

<span data-ttu-id="29385-989">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-989">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="29385-990">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="29385-990">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="29385-991">値</span><span class="sxs-lookup"><span data-stu-id="29385-991">value</span></span>  
<span data-ttu-id="29385-992">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-992">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="29385-993">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="29385-993">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="29385-994">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="29385-994">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="29385-995">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="29385-995">Method userSkip</span></span>

<span data-ttu-id="29385-996">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-996">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="29385-997">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="29385-997">Parameters - userSkip</span></span>

<span data-ttu-id="29385-998">値</span><span class="sxs-lookup"><span data-stu-id="29385-998">value</span></span>  
<span data-ttu-id="29385-999">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-999">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="29385-1000">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="29385-1000">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="29385-1001">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="29385-1001">Return Value - userSkip</span></span>

<span data-ttu-id="29385-1002">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="29385-1002">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="29385-1003">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="29385-1003">Method userWidth</span></span>

<span data-ttu-id="29385-1004">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-1004">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="29385-1005">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="29385-1005">Parameters - userWidth</span></span>

<span data-ttu-id="29385-1006">値</span><span class="sxs-lookup"><span data-stu-id="29385-1006">value</span></span>  
<span data-ttu-id="29385-1007">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-1007">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="29385-1008">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="29385-1008">Return Value - userWidth</span></span>

<span data-ttu-id="29385-1009">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="29385-1009">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="29385-1010">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="29385-1010">Remarks - userWidth</span></span>

<span data-ttu-id="29385-1011">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="29385-1011">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="29385-1012">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="29385-1012">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="29385-1013">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="29385-1013">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="29385-1014">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="29385-1014">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="29385-1015">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="29385-1015">Parameters - useUserLayout</span></span>

<span data-ttu-id="29385-1016">値</span><span class="sxs-lookup"><span data-stu-id="29385-1016">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="29385-1017">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="29385-1017">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="29385-1018">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="29385-1018">Method verticalSpacing</span></span>

<span data-ttu-id="29385-1019">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-1019">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="29385-1020">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="29385-1020">Parameters - verticalSpacing</span></span>

<span data-ttu-id="29385-1021">値</span><span class="sxs-lookup"><span data-stu-id="29385-1021">value</span></span>  
<span data-ttu-id="29385-1022">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-1022">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="29385-1023">モード</span><span class="sxs-lookup"><span data-stu-id="29385-1023">mode</span></span>  
<span data-ttu-id="29385-1024">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-1024">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="29385-1025">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="29385-1025">Return Value - verticalSpacing</span></span>

<span data-ttu-id="29385-1026">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="29385-1026">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="29385-1027">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="29385-1027">Method verticalSpacingMode</span></span>

<span data-ttu-id="29385-1028">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-1028">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="29385-1029">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="29385-1029">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="29385-1030">モード</span><span class="sxs-lookup"><span data-stu-id="29385-1030">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="29385-1031">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="29385-1031">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="29385-1032">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="29385-1032">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="29385-1033">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="29385-1033">Method verticalSpacingValue</span></span>

<span data-ttu-id="29385-1034">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-1034">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="29385-1035">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="29385-1035">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="29385-1036">値</span><span class="sxs-lookup"><span data-stu-id="29385-1036">value</span></span>  
<span data-ttu-id="29385-1037">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-1037">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="29385-1038">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="29385-1038">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="29385-1039">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="29385-1039">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="29385-1040">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="29385-1040">Method visible</span></span>

<span data-ttu-id="29385-1041">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29385-1041">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="29385-1042">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="29385-1042">Parameters - visible</span></span>

<span data-ttu-id="29385-1043">値</span><span class="sxs-lookup"><span data-stu-id="29385-1043">value</span></span>  
<span data-ttu-id="29385-1044">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-1044">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="29385-1045">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="29385-1045">Return Value - visible</span></span>

<span data-ttu-id="29385-1046">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="29385-1046">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="29385-1047">メソッド width</span><span class="sxs-lookup"><span data-stu-id="29385-1047">Method width</span></span>

<span data-ttu-id="29385-1048">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-1048">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="29385-1049">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="29385-1049">Parameters - width</span></span>

<span data-ttu-id="29385-1050">値</span><span class="sxs-lookup"><span data-stu-id="29385-1050">value</span></span>  
<span data-ttu-id="29385-1051">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-1051">An integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="29385-1052">モード</span><span class="sxs-lookup"><span data-stu-id="29385-1052">mode</span></span>  
<span data-ttu-id="29385-1053">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-1053">An integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="29385-1054">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="29385-1054">Return Value - width</span></span>

<span data-ttu-id="29385-1055">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="29385-1055">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="29385-1056">備考 - width</span><span class="sxs-lookup"><span data-stu-id="29385-1056">Remarks - width</span></span>

<span data-ttu-id="29385-1057">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29385-1057">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="29385-1058">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="29385-1058">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="29385-1059">モード</span><span class="sxs-lookup"><span data-stu-id="29385-1059">Mode</span></span>           | <span data-ttu-id="29385-1060">幅計算</span><span class="sxs-lookup"><span data-stu-id="29385-1060">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29385-1061">-1 正確</span><span class="sxs-lookup"><span data-stu-id="29385-1061">-1 Exact</span></span>       | <span data-ttu-id="29385-1062">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="29385-1062">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="29385-1063">0 自動</span><span class="sxs-lookup"><span data-stu-id="29385-1063">0 Auto</span></span>         | <span data-ttu-id="29385-1064">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="29385-1064">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="29385-1065">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="29385-1065">1 Column width</span></span> | <span data-ttu-id="29385-1066">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="29385-1066">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="29385-1067">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="29385-1067">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="29385-1068">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="29385-1068">Method widthMode</span></span>

<span data-ttu-id="29385-1069">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-1069">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="29385-1070">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="29385-1070">Parameters - widthMode</span></span>

<span data-ttu-id="29385-1071">値</span><span class="sxs-lookup"><span data-stu-id="29385-1071">value</span></span>  
<span data-ttu-id="29385-1072">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-1072">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="29385-1073">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="29385-1073">Return Value - widthMode</span></span>

<span data-ttu-id="29385-1074">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1074">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="29385-1075">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="29385-1075">Remarks - widthMode</span></span>

<span data-ttu-id="29385-1076">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="29385-1076">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="29385-1077">モード</span><span class="sxs-lookup"><span data-stu-id="29385-1077">Mode</span></span>         | <span data-ttu-id="29385-1078">幅計算</span><span class="sxs-lookup"><span data-stu-id="29385-1078">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29385-1079">正確</span><span class="sxs-lookup"><span data-stu-id="29385-1079">Exact</span></span>        | <span data-ttu-id="29385-1080">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="29385-1080">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="29385-1081">自動</span><span class="sxs-lookup"><span data-stu-id="29385-1081">Auto</span></span>         | <span data-ttu-id="29385-1082">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="29385-1082">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="29385-1083">列の幅</span><span class="sxs-lookup"><span data-stu-id="29385-1083">Column width</span></span> | <span data-ttu-id="29385-1084">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="29385-1084">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="29385-1085">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="29385-1085">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="29385-1086">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="29385-1086">Method widthValue</span></span>

<span data-ttu-id="29385-1087">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-1087">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="29385-1088">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="29385-1088">Parameters - widthValue</span></span>

<span data-ttu-id="29385-1089">値</span><span class="sxs-lookup"><span data-stu-id="29385-1089">value</span></span>  
<span data-ttu-id="29385-1090">幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="29385-1090">An integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="29385-1091">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="29385-1091">Return Value - widthValue</span></span>

<span data-ttu-id="29385-1092">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="29385-1092">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="29385-1093">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="29385-1093">Remarks - widthValue</span></span>

<span data-ttu-id="29385-1094">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="29385-1094">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-prefcolumnsize"></a><span data-ttu-id="29385-1095">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="29385-1095">Method prefColumnSize</span></span>

<span data-ttu-id="29385-1096">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="29385-1096">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="29385-1097">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="29385-1097">Parameters - prefColumnSize</span></span>

<span data-ttu-id="29385-1098">width</span><span class="sxs-lookup"><span data-stu-id="29385-1098">width</span></span>  
<span data-ttu-id="29385-1099">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="29385-1099">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="29385-1100">height</span><span class="sxs-lookup"><span data-stu-id="29385-1100">height</span></span>  
<span data-ttu-id="29385-1101">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="29385-1101">The preferred height of the control.</span></span>

## <a name="method-drop"></a><span data-ttu-id="29385-1102">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="29385-1102">Method drop</span></span>

<span data-ttu-id="29385-1103">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-1103">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="29385-1104">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="29385-1104">Parameters - drop</span></span>

<span data-ttu-id="29385-1105">dragSource</span><span class="sxs-lookup"><span data-stu-id="29385-1105">dragSource</span></span>  
<span data-ttu-id="29385-1106">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1106">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-1107">dragMode</span><span class="sxs-lookup"><span data-stu-id="29385-1107">dragMode</span></span>  
<span data-ttu-id="29385-1108">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1108">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-1109">x</span><span class="sxs-lookup"><span data-stu-id="29385-1109">x</span></span>  
<span data-ttu-id="29385-1110">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1110">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-1111">y</span><span class="sxs-lookup"><span data-stu-id="29385-1111">y</span></span>  
<span data-ttu-id="29385-1112">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1112">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-setcollabel"></a><span data-ttu-id="29385-1113">メソッド setColLabel</span><span class="sxs-lookup"><span data-stu-id="29385-1113">Method setColLabel</span></span>

```xpp
public void setColLabel(int column, str text)
```

### <a name="parameters---setcollabel"></a><span data-ttu-id="29385-1114">パラメーター - setColLabel</span><span class="sxs-lookup"><span data-stu-id="29385-1114">Parameters - setColLabel</span></span>

<span data-ttu-id="29385-1115">column</span><span class="sxs-lookup"><span data-stu-id="29385-1115">column</span></span>  

<!-- -->

<span data-ttu-id="29385-1116">テキスト</span><span class="sxs-lookup"><span data-stu-id="29385-1116">text</span></span>  

## <a name="method-mouseenter"></a><span data-ttu-id="29385-1117">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="29385-1117">Method mouseEnter</span></span>

<span data-ttu-id="29385-1118">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-1118">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="29385-1119">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="29385-1119">Parameters - mouseEnter</span></span>

<span data-ttu-id="29385-1120">x</span><span class="sxs-lookup"><span data-stu-id="29385-1120">x</span></span>  
<span data-ttu-id="29385-1121">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-1121">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-1122">y</span><span class="sxs-lookup"><span data-stu-id="29385-1122">y</span></span>  
<span data-ttu-id="29385-1123">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-1123">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-1124">ボタン</span><span class="sxs-lookup"><span data-stu-id="29385-1124">button</span></span>  
<span data-ttu-id="29385-1125">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-1125">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-1126">Ctrl</span><span class="sxs-lookup"><span data-stu-id="29385-1126">Ctrl</span></span>  
<span data-ttu-id="29385-1127">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-1127">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="29385-1128">シフト</span><span class="sxs-lookup"><span data-stu-id="29385-1128">Shift</span></span>  
<span data-ttu-id="29385-1129">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29385-1129">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="29385-1130">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="29385-1130">Method resetUserSetting</span></span>

<span data-ttu-id="29385-1131">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="29385-1131">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-lostfocus"></a><span data-ttu-id="29385-1132">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="29385-1132">Method lostFocus</span></span>

<span data-ttu-id="29385-1133">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="29385-1133">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-inputsearch"></a><span data-ttu-id="29385-1134">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="29385-1134">Method inputSearch</span></span>

<span data-ttu-id="29385-1135">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="29385-1135">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="29385-1136">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="29385-1136">Parameters - inputSearch</span></span>

<span data-ttu-id="29385-1137">searchStr</span><span class="sxs-lookup"><span data-stu-id="29385-1137">searchStr</span></span>  
<span data-ttu-id="29385-1138">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="29385-1138">The string value to use to filter data; optional.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="29385-1139">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="29385-1139">Method dragLeave</span></span>

<span data-ttu-id="29385-1140">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-1140">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="29385-1141">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="29385-1141">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="29385-1142">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="29385-1142">Parameters - OnGotFocus</span></span>

<span data-ttu-id="29385-1143">sender</span><span class="sxs-lookup"><span data-stu-id="29385-1143">sender</span></span>  

<!-- -->

<span data-ttu-id="29385-1144">e</span><span class="sxs-lookup"><span data-stu-id="29385-1144">e</span></span>  

## <a name="method-registeroverridemethod"></a><span data-ttu-id="29385-1145">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="29385-1145">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="29385-1146">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="29385-1146">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="29385-1147">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="29385-1147">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="29385-1148">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="29385-1148">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="29385-1149">overrideObject</span><span class="sxs-lookup"><span data-stu-id="29385-1149">overrideObject</span></span>  

## <a name="method-arrange"></a><span data-ttu-id="29385-1150">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="29385-1150">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-onleaving"></a><span data-ttu-id="29385-1151">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="29385-1151">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="29385-1152">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="29385-1152">Parameters - OnLeaving</span></span>

<span data-ttu-id="29385-1153">sender</span><span class="sxs-lookup"><span data-stu-id="29385-1153">sender</span></span>  

<!-- -->

<span data-ttu-id="29385-1154">e</span><span class="sxs-lookup"><span data-stu-id="29385-1154">e</span></span>  

## <a name="method-deleterows"></a><span data-ttu-id="29385-1155">メソッド deleteRows</span><span class="sxs-lookup"><span data-stu-id="29385-1155">Method deleteRows</span></span>

<span data-ttu-id="29385-1156">;</span><span class="sxs-lookup"><span data-stu-id="29385-1156">;</span></span>

```xpp
public void deleteRows(int deleteAfterRow, int rows)
```

### <a name="parameters---deleterows"></a><span data-ttu-id="29385-1157">パラメーター - deleteRows</span><span class="sxs-lookup"><span data-stu-id="29385-1157">Parameters - deleteRows</span></span>

<span data-ttu-id="29385-1158">deleteAfterRow</span><span class="sxs-lookup"><span data-stu-id="29385-1158">deleteAfterRow</span></span>  

<!-- -->

<span data-ttu-id="29385-1159">行</span><span class="sxs-lookup"><span data-stu-id="29385-1159">rows</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="29385-1160">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="29385-1160">Method endDrag</span></span>

<span data-ttu-id="29385-1161">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="29385-1161">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="29385-1162">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="29385-1162">Remarks - endDrag</span></span>

<span data-ttu-id="29385-1163">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="29385-1163">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="29385-1164">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="29385-1164">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-deletecols"></a><span data-ttu-id="29385-1165">メソッド deleteCols</span><span class="sxs-lookup"><span data-stu-id="29385-1165">Method deleteCols</span></span>

```xpp
public void deleteCols(int deleteAfterColumn, int columns)
```

### <a name="parameters---deletecols"></a><span data-ttu-id="29385-1166">パラメーター - deleteCols</span><span class="sxs-lookup"><span data-stu-id="29385-1166">Parameters - deleteCols</span></span>

<span data-ttu-id="29385-1167">deleteAfterColumn</span><span class="sxs-lookup"><span data-stu-id="29385-1167">deleteAfterColumn</span></span>  

<!-- -->

<span data-ttu-id="29385-1168">列</span><span class="sxs-lookup"><span data-stu-id="29385-1168">columns</span></span>  

## <a name="method-clear"></a><span data-ttu-id="29385-1169">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="29385-1169">Method clear</span></span>

```xpp
public void clear()
```

## <a name="method-insertrows"></a><span data-ttu-id="29385-1170">メソッド insertRows</span><span class="sxs-lookup"><span data-stu-id="29385-1170">Method insertRows</span></span>

```xpp
public void insertRows(int insertAfterRow, int rows)
```

### <a name="parameters---insertrows"></a><span data-ttu-id="29385-1171">パラメーター - insertRows</span><span class="sxs-lookup"><span data-stu-id="29385-1171">Parameters - insertRows</span></span>

<span data-ttu-id="29385-1172">insertAfterRow</span><span class="sxs-lookup"><span data-stu-id="29385-1172">insertAfterRow</span></span>  

<!-- -->

<span data-ttu-id="29385-1173">行</span><span class="sxs-lookup"><span data-stu-id="29385-1173">rows</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="29385-1174">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="29385-1174">Method gotFocus</span></span>

<span data-ttu-id="29385-1175">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="29385-1175">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="29385-1176">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="29385-1176">Method displayControl</span></span>

<span data-ttu-id="29385-1177">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="29385-1177">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-onenter"></a><span data-ttu-id="29385-1178">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="29385-1178">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="29385-1179">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="29385-1179">Parameters - OnEnter</span></span>

<span data-ttu-id="29385-1180">sender</span><span class="sxs-lookup"><span data-stu-id="29385-1180">sender</span></span>  

<!-- -->

<span data-ttu-id="29385-1181">e</span><span class="sxs-lookup"><span data-stu-id="29385-1181">e</span></span>  

## <a name="method-copy"></a><span data-ttu-id="29385-1182">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="29385-1182">Method copy</span></span>

<span data-ttu-id="29385-1183">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="29385-1183">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-setrowlabel"></a><span data-ttu-id="29385-1184">メソッド setRowLabel</span><span class="sxs-lookup"><span data-stu-id="29385-1184">Method setRowLabel</span></span>

```xpp
public void setRowLabel(int row, str text)
```

### <a name="parameters---setrowlabel"></a><span data-ttu-id="29385-1185">パラメーター - setRowLabel</span><span class="sxs-lookup"><span data-stu-id="29385-1185">Parameters - setRowLabel</span></span>

<span data-ttu-id="29385-1186"> 行 </span><span class="sxs-lookup"><span data-stu-id="29385-1186">row</span></span>  

<!-- -->

<span data-ttu-id="29385-1187">テキスト</span><span class="sxs-lookup"><span data-stu-id="29385-1187">text</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="29385-1188">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="29385-1188">Method mouseLeave</span></span>

<span data-ttu-id="29385-1189">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="29385-1189">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-paste"></a><span data-ttu-id="29385-1190">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="29385-1190">Method paste</span></span>

<span data-ttu-id="29385-1191">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="29385-1191">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-enter"></a><span data-ttu-id="29385-1192">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="29385-1192">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-cut"></a><span data-ttu-id="29385-1193">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="29385-1193">Method cut</span></span>

<span data-ttu-id="29385-1194">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="29385-1194">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-dropex"></a><span data-ttu-id="29385-1195">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="29385-1195">Method dropEx</span></span>

<span data-ttu-id="29385-1196">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="29385-1196">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="29385-1197">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="29385-1197">Parameters - dropEx</span></span>

<span data-ttu-id="29385-1198">dragSource</span><span class="sxs-lookup"><span data-stu-id="29385-1198">dragSource</span></span>  
<span data-ttu-id="29385-1199">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1199">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-1200">dragMode</span><span class="sxs-lookup"><span data-stu-id="29385-1200">dragMode</span></span>  
<span data-ttu-id="29385-1201">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1201">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-1202">x</span><span class="sxs-lookup"><span data-stu-id="29385-1202">x</span></span>  
<span data-ttu-id="29385-1203">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1203">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="29385-1204">y</span><span class="sxs-lookup"><span data-stu-id="29385-1204">y</span></span>  
<span data-ttu-id="29385-1205">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29385-1205">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="29385-1206">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="29385-1206">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="29385-1207">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="29385-1207">Parameters - OnLostFocus</span></span>

<span data-ttu-id="29385-1208">sender</span><span class="sxs-lookup"><span data-stu-id="29385-1208">sender</span></span>  

<!-- -->

<span data-ttu-id="29385-1209">e</span><span class="sxs-lookup"><span data-stu-id="29385-1209">e</span></span>  

## <a name="method-updatecell"></a><span data-ttu-id="29385-1210">パラメーター - update</span><span class="sxs-lookup"><span data-stu-id="29385-1210">Method updateCell</span></span>

```xpp
public void updateCell(int column, int row)
```

### <a name="parameters---updatecell"></a><span data-ttu-id="29385-1211">パラメーター - updateCell</span><span class="sxs-lookup"><span data-stu-id="29385-1211">Parameters - updateCell</span></span>

<span data-ttu-id="29385-1212">column</span><span class="sxs-lookup"><span data-stu-id="29385-1212">column</span></span>  

<!-- -->

<span data-ttu-id="29385-1213"> 行 </span><span class="sxs-lookup"><span data-stu-id="29385-1213">row</span></span>  

## <a name="method-insertcols"></a><span data-ttu-id="29385-1214">メソッド insertCols</span><span class="sxs-lookup"><span data-stu-id="29385-1214">Method insertCols</span></span>

```xpp
public void insertCols(int insertAferColumn, int columns)
```

### <a name="parameters---insertcols"></a><span data-ttu-id="29385-1215">パラメーター - insertCols</span><span class="sxs-lookup"><span data-stu-id="29385-1215">Parameters - insertCols</span></span>

<span data-ttu-id="29385-1216">insertAferColumn</span><span class="sxs-lookup"><span data-stu-id="29385-1216">insertAferColumn</span></span>  

<!-- -->

<span data-ttu-id="29385-1217">列</span><span class="sxs-lookup"><span data-stu-id="29385-1217">columns</span></span>  

## <a name="method-activecellchanged"></a><span data-ttu-id="29385-1218">メソッド activeCellChanged</span><span class="sxs-lookup"><span data-stu-id="29385-1218">Method activeCellChanged</span></span>

```xpp
public void activeCellChanged()
```

## <a name="method-context"></a><span data-ttu-id="29385-1219">メソッド context</span><span class="sxs-lookup"><span data-stu-id="29385-1219">Method context</span></span>

<span data-ttu-id="29385-1220">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="29385-1220">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-setfocus"></a><span data-ttu-id="29385-1221">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="29385-1221">Method setFocus</span></span>

<span data-ttu-id="29385-1222">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="29385-1222">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

