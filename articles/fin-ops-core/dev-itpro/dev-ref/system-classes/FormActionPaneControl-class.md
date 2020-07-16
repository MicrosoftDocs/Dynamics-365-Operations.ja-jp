---
title: FormActionPaneControl クラス
description: このトピックでは、FormActionPaneControl クラスについて説明します。
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
ms.openlocfilehash: 11eaa164d8166964083c1da1d8880c2312cb7690
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502667"
---
# <a name="class-formactionpanecontrol"></a><span data-ttu-id="d81a1-103">クラス FormActionPaneControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-103">Class FormActionPaneControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormActionPaneControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="d81a1-104">備考</span><span class="sxs-lookup"><span data-stu-id="d81a1-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d81a1-105">例</span><span class="sxs-lookup"><span data-stu-id="d81a1-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d81a1-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d81a1-106">Methods</span></span>

| <span data-ttu-id="d81a1-107">方法</span><span class="sxs-lookup"><span data-stu-id="d81a1-107">Method</span></span>                                                                                                              | <span data-ttu-id="d81a1-108">説明</span><span class="sxs-lookup"><span data-stu-id="d81a1-108">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81a1-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                      |
| <span data-ttu-id="d81a1-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                      |
| <span data-ttu-id="d81a1-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                      |
| <span data-ttu-id="d81a1-112">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-112">public boolean alignChild(\[boolean value\])</span></span>                                                                        |                                                                                                                                                      |
| <span data-ttu-id="d81a1-113">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-113">public boolean alignChildren(\[boolean value\])</span></span>                                                                     |                                                                                                                                                      |
| <span data-ttu-id="d81a1-114">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-114">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="d81a1-115">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-115">Determines whether to align the control.</span></span>                                                                                                             |
| <span data-ttu-id="d81a1-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="d81a1-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-117">Determines whether the user can change the contents of the control.</span></span>                                                                                  |
| <span data-ttu-id="d81a1-118">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="d81a1-118">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="d81a1-119">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-119">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                  |
| <span data-ttu-id="d81a1-120">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-120">public int allowUserSetup(\[int value\])</span></span>                                                                            |                                                                                                                                                      |
| <span data-ttu-id="d81a1-121">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-121">public int arrangeGuide(\[int value\])</span></span>                                                                              |                                                                                                                                                      |
| <span data-ttu-id="d81a1-122">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-122">public int arrangeMethod(\[int value\])</span></span>                                                                             |                                                                                                                                                      |
| <span data-ttu-id="d81a1-123">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-123">public int arrangeWhen(\[int value\])</span></span>                                                                               |                                                                                                                                                      |
| <span data-ttu-id="d81a1-124">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-124">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="d81a1-125">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-125">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                   |
| <span data-ttu-id="d81a1-126">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d81a1-126">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="d81a1-127">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-127">Is called when the user starts to drag a form control.</span></span>                                                                                               |
| <span data-ttu-id="d81a1-128">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-128">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           |                                                                                                                                                      |
| <span data-ttu-id="d81a1-129">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-129">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 |                                                                                                                                                      |
| <span data-ttu-id="d81a1-130">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-130">public int bottomMarginValue(\[int value\])</span></span>                                                                         |                                                                                                                                                      |
| <span data-ttu-id="d81a1-131">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="d81a1-131">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="d81a1-132">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-132">Retrieves the size of the control.</span></span>                                                                                                                   |
| <span data-ttu-id="d81a1-133">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-133">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                      |
| <span data-ttu-id="d81a1-134">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="d81a1-134">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                      |
| <span data-ttu-id="d81a1-135">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-135">public str caption(\[str value\])</span></span>                                                                                   | <span data-ttu-id="d81a1-136">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-136">Gets or set the caption of the control.</span></span>                                                                                                              |
| <span data-ttu-id="d81a1-137">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-137">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                             |                                                                                                                                                      |
| <span data-ttu-id="d81a1-138">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-138">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                |                                                                                                                                                      |
| <span data-ttu-id="d81a1-139">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-139">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                      |
| <span data-ttu-id="d81a1-140">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-140">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                      |
| <span data-ttu-id="d81a1-141">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-141">public int columnspaceValue(\[int value\])</span></span>                                                                          |                                                                                                                                                      |
| <span data-ttu-id="d81a1-142">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-142">public int columnsValue(\[int value\])</span></span>                                                                              |                                                                                                                                                      |
| <span data-ttu-id="d81a1-143">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-143">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="d81a1-144">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-144">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                  |
| <span data-ttu-id="d81a1-145">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="d81a1-145">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="d81a1-146">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-146">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                     |
| <span data-ttu-id="d81a1-147">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="d81a1-147">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                      |
| <span data-ttu-id="d81a1-148">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="d81a1-148">public int controlCount()</span></span>                                                                                           |                                                                                                                                                      |
| <span data-ttu-id="d81a1-149">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="d81a1-149">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                      |
| <span data-ttu-id="d81a1-150">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-150">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="d81a1-151">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-151">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                        |
| <span data-ttu-id="d81a1-152">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-152">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="d81a1-153">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-153">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                             |
| <span data-ttu-id="d81a1-154">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-154">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="d81a1-155">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-155">Gets or sets the value that indicates whether the control is displayed in the client, or in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="d81a1-156">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-156">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="d81a1-157">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-157">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                    |
| <span data-ttu-id="d81a1-158">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d81a1-158">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="d81a1-159">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-159">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                       |
| <span data-ttu-id="d81a1-160">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d81a1-160">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="d81a1-161">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-161">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                     |
| <span data-ttu-id="d81a1-162">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="d81a1-162">public str dragText()</span></span>                                                                                               | <span data-ttu-id="d81a1-163">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-163">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                               |
| <span data-ttu-id="d81a1-164">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-164">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="d81a1-165">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-165">Determines whether to enable or disable the object.</span></span>                                                                                                  |
| <span data-ttu-id="d81a1-166">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-166">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="d81a1-167">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-167">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                             |
| <span data-ttu-id="d81a1-168">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="d81a1-168">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="d81a1-169">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-169">Indicates whether the control has custom user settings.</span></span>                                                                                              |
| <span data-ttu-id="d81a1-170">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-170">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="d81a1-171">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-171">Gets or sets the height of the control.</span></span>                                                                                                              |
| <span data-ttu-id="d81a1-172">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-172">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="d81a1-173">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-173">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                       |
| <span data-ttu-id="d81a1-174">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-174">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="d81a1-175">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-175">Gets or sets the height of the control.</span></span>                                                                                                              |
| <span data-ttu-id="d81a1-176">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="d81a1-176">public str helpField()</span></span>                                                                                              | <span data-ttu-id="d81a1-177">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-177">Retrieves the Help text for the control.</span></span>                                                                                                             |
| <span data-ttu-id="d81a1-178">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-178">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="d81a1-179">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-179">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                             |
| <span data-ttu-id="d81a1-180">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-180">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |                                                                                                                                                      |
| <span data-ttu-id="d81a1-181">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-181">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="d81a1-182">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-182">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                      |
| <span data-ttu-id="d81a1-183">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="d81a1-183">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="d81a1-184">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-184">Retrieves the Windows handle for the control.</span></span>                                                                                                        |
| <span data-ttu-id="d81a1-185">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="d81a1-185">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                      |
| <span data-ttu-id="d81a1-186">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="d81a1-186">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="d81a1-187">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-187">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                   |
| <span data-ttu-id="d81a1-188">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="d81a1-188">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="d81a1-189">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-189">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                  |
| <span data-ttu-id="d81a1-190">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="d81a1-190">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="d81a1-191">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-191">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                |
| <span data-ttu-id="d81a1-192">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="d81a1-192">public boolean leave()</span></span>                                                                                              |                                                                                                                                                      |
| <span data-ttu-id="d81a1-193">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-193">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="d81a1-194">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-194">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                     |
| <span data-ttu-id="d81a1-195">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-195">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             |                                                                                                                                                      |
| <span data-ttu-id="d81a1-196">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-196">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   |                                                                                                                                                      |
| <span data-ttu-id="d81a1-197">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-197">public int leftMarginValue(\[int value\])</span></span>                                                                           |                                                                                                                                                      |
| <span data-ttu-id="d81a1-198">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-198">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="d81a1-199">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-199">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="d81a1-200">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-200">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="d81a1-201">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-201">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                     |
| <span data-ttu-id="d81a1-202">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-202">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="d81a1-203">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="d81a1-203">Marks or unmarks the control as a user-added control.</span></span>                                                                                                |
| <span data-ttu-id="d81a1-204">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d81a1-204">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="d81a1-205">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-205">Is called when the control is double-clicked by the user.</span></span>                                                                                            |
| <span data-ttu-id="d81a1-206">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d81a1-206">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="d81a1-207">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-207">Is called when the user clicks the mouse button over the control.</span></span>                                                                                    |
| <span data-ttu-id="d81a1-208">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d81a1-208">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="d81a1-209">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-209">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                    |
| <span data-ttu-id="d81a1-210">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d81a1-210">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="d81a1-211">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-211">Is called when the user releases the mouse button over the control area.</span></span>                                                                             |
| <span data-ttu-id="d81a1-212">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-212">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                      |
| <span data-ttu-id="d81a1-213">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-213">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="d81a1-214">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-214">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span>        |
| <span data-ttu-id="d81a1-215">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-215">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                      |
| <span data-ttu-id="d81a1-216">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="d81a1-216">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                      |
| <span data-ttu-id="d81a1-217">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="d81a1-217">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="d81a1-218">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-218">Retrieves the parent control for the control.</span></span>                                                                                                        |
| <span data-ttu-id="d81a1-219">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-219">public int position(\[int value\])</span></span>                                                                                  |                                                                                                                                                      |
| <span data-ttu-id="d81a1-220">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-220">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                      |
| <span data-ttu-id="d81a1-221">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-221">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                      |
| <span data-ttu-id="d81a1-222">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-222">public int rightMarginValue(\[int value\])</span></span>                                                                          |                                                                                                                                                      |
| <span data-ttu-id="d81a1-223">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-223">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="d81a1-224">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-224">Sets or returns the ID of the security key for the control.</span></span>                                                                                          |
| <span data-ttu-id="d81a1-225">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="d81a1-225">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="d81a1-226">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-226">Shows the shortcut menu for the control.</span></span>                                                                                                             |
| <span data-ttu-id="d81a1-227">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-227">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="d81a1-228">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-228">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                      |
| <span data-ttu-id="d81a1-229">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-229">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                      |
| <span data-ttu-id="d81a1-230">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-230">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                      |
| <span data-ttu-id="d81a1-231">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="d81a1-231">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="d81a1-232">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-232">Retrieves the tooltip text for the control.</span></span>                                                                                                          |
| <span data-ttu-id="d81a1-233">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-233">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="d81a1-234">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-234">Gets or sets the vertical position of the control in the form.</span></span>                                                                                       |
| <span data-ttu-id="d81a1-235">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-235">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              |                                                                                                                                                      |
| <span data-ttu-id="d81a1-236">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-236">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    |                                                                                                                                                      |
| <span data-ttu-id="d81a1-237">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-237">public int topMarginValue(\[int value\])</span></span>                                                                            |                                                                                                                                                      |
| <span data-ttu-id="d81a1-238">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-238">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="d81a1-239">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-239">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                          |
| <span data-ttu-id="d81a1-240">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-240">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="d81a1-241">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-241">Gets or sets the vertical position of the control in the form.</span></span>                                                                                       |
| <span data-ttu-id="d81a1-242">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-242">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                      |
| <span data-ttu-id="d81a1-243">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="d81a1-243">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                      |
| <span data-ttu-id="d81a1-244">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-244">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="d81a1-245">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-245">Gets or sets the user data for the control.</span></span>                                                                                                          |
| <span data-ttu-id="d81a1-246">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-246">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="d81a1-247">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-247">Gets or sets the user data item for the control.</span></span>                                                                                                     |
| <span data-ttu-id="d81a1-248">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-248">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="d81a1-249">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-249">Gets or sets the number of user data items for the control.</span></span>                                                                                          |
| <span data-ttu-id="d81a1-250">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-250">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="d81a1-251">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-251">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                  |
| <span data-ttu-id="d81a1-252">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-252">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="d81a1-253">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-253">Gets or sets the custom user height for the control.</span></span>                                                                                                 |
| <span data-ttu-id="d81a1-254">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-254">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="d81a1-255">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-255">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                   |
| <span data-ttu-id="d81a1-256">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-256">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="d81a1-257">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-257">Gets or sets the organization container for the control.</span></span>                                                                                             |
| <span data-ttu-id="d81a1-258">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-258">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="d81a1-259">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-259">Gets or sets the organization sibling for the control.</span></span>                                                                                               |
| <span data-ttu-id="d81a1-260">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-260">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="d81a1-261">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-261">Gets or sets the user label text for the control.</span></span>                                                                                                    |
| <span data-ttu-id="d81a1-262">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-262">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="d81a1-263">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-263">Gets or sets the user security level for the control.</span></span>                                                                                                |
| <span data-ttu-id="d81a1-264">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-264">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="d81a1-265">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-265">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span> |
| <span data-ttu-id="d81a1-266">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-266">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="d81a1-267">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-267">Sets or returns the width of the control in pixels.</span></span>                                                                                                  |
| <span data-ttu-id="d81a1-268">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-268">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                      |
| <span data-ttu-id="d81a1-269">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-269">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="d81a1-270">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-270">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="d81a1-271">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-271">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="d81a1-272">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-272">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                          |
| <span data-ttu-id="d81a1-273">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-273">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="d81a1-274">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-274">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="d81a1-275">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-275">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="d81a1-276">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-276">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                               |
| <span data-ttu-id="d81a1-277">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-277">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="d81a1-278">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-278">Gets or sets the width of the control.</span></span>                                                                                                               |
| <span data-ttu-id="d81a1-279">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-279">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="d81a1-280">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-280">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                       |
| <span data-ttu-id="d81a1-281">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-281">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="d81a1-282">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-282">Gets or sets the width of the control.</span></span>                                                                                                               |
| <span data-ttu-id="d81a1-283">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d81a1-283">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="d81a1-284">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-284">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                   |
| <span data-ttu-id="d81a1-285">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="d81a1-285">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="d81a1-286">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-286">Indicates that the control has lost focus.</span></span>                                                                                                           |
| <span data-ttu-id="d81a1-287">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-287">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                      |
| <span data-ttu-id="d81a1-288">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="d81a1-288">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="d81a1-289">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-289">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                     |
| <span data-ttu-id="d81a1-290">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d81a1-290">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="d81a1-291">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-291">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                               |
| <span data-ttu-id="d81a1-292">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="d81a1-292">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="d81a1-293">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-293">Indicates that the control has received focus.</span></span>                                                                                                       |
| <span data-ttu-id="d81a1-294">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="d81a1-294">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="d81a1-295">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-295">Indicates that the mouse pointer has left the control.</span></span>                                                                                               |
| <span data-ttu-id="d81a1-296">public void setArea(str area)</span><span class="sxs-lookup"><span data-stu-id="d81a1-296">public void setArea(str area)</span></span>                                                                                       |                                                                                                                                                      |
| <span data-ttu-id="d81a1-297">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="d81a1-297">public void arrange()</span></span>                                                                                               |                                                                                                                                                      |
| <span data-ttu-id="d81a1-298">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-298">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                      |
| <span data-ttu-id="d81a1-299">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-299">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                      |
| <span data-ttu-id="d81a1-300">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="d81a1-300">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                      |
| <span data-ttu-id="d81a1-301">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-301">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                      |
| <span data-ttu-id="d81a1-302">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="d81a1-302">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="d81a1-303">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-303">Performs data filtering for the control, based on the specified string.</span></span>                                                                              |
| <span data-ttu-id="d81a1-304">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="d81a1-304">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="d81a1-305">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-305">Is called when the user has finished dragging a form control.</span></span>                                                                                        |
| <span data-ttu-id="d81a1-306">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="d81a1-306">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="d81a1-307">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-307">Sets the focus on the control.</span></span>                                                                                                                       |
| <span data-ttu-id="d81a1-308">public void tabChanged(str newTab)</span><span class="sxs-lookup"><span data-stu-id="d81a1-308">public void tabChanged(str newTab)</span></span>                                                                                  | <span data-ttu-id="d81a1-309">アクティブなタブが変更されると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-309">Is called when the active tab is changed.</span></span>                                                                                                            |
| <span data-ttu-id="d81a1-310">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-310">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                      |
| <span data-ttu-id="d81a1-311">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="d81a1-311">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="d81a1-312">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-312">Displays the control.</span></span>                                                                                                                                |
| <span data-ttu-id="d81a1-313">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="d81a1-313">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="d81a1-314">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-314">Specifies the preferred column width and height for the form control.</span></span>                                                                                |
| <span data-ttu-id="d81a1-315">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-315">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                      |
| <span data-ttu-id="d81a1-316">public void cut()</span><span class="sxs-lookup"><span data-stu-id="d81a1-316">public void cut()</span></span>                                                                                                   | <span data-ttu-id="d81a1-317">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="d81a1-317">Cuts the contents of the control.</span></span>                                                                                                                    |
| <span data-ttu-id="d81a1-318">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="d81a1-318">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="d81a1-319">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="d81a1-319">Resets the user settings for the control.</span></span>                                                                                                            |
| <span data-ttu-id="d81a1-320">private void OnTabChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d81a1-320">private void OnTabChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                       |                                                                                                                                                      |
| <span data-ttu-id="d81a1-321">public void paste()</span><span class="sxs-lookup"><span data-stu-id="d81a1-321">public void paste()</span></span>                                                                                                 | <span data-ttu-id="d81a1-322">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-322">Pastes the contents of the clipboard into the control.</span></span>                                                                                               |
| <span data-ttu-id="d81a1-323">public void copy()</span><span class="sxs-lookup"><span data-stu-id="d81a1-323">public void copy()</span></span>                                                                                                  | <span data-ttu-id="d81a1-324">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d81a1-324">Copies the contents of the control to the clipboard.</span></span>                                                                                                 |
| <span data-ttu-id="d81a1-325">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d81a1-325">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="d81a1-326">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-326">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                 |
| <span data-ttu-id="d81a1-327">public void context()</span><span class="sxs-lookup"><span data-stu-id="d81a1-327">public void context()</span></span>                                                                                               | <span data-ttu-id="d81a1-328">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-328">Shows the shortcut menu for the control.</span></span>                                                                                                             |
| <span data-ttu-id="d81a1-329">public void enter()</span><span class="sxs-lookup"><span data-stu-id="d81a1-329">public void enter()</span></span>                                                                                                 |                                                                                                                                                      |

## <a name="method-addcontrol"></a><span data-ttu-id="d81a1-330">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-330">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="d81a1-331">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-331">Parameters - addControl</span></span>

<span data-ttu-id="d81a1-332">controlType</span><span class="sxs-lookup"><span data-stu-id="d81a1-332">controlType</span></span>  

<!-- -->

<span data-ttu-id="d81a1-333">controlName</span><span class="sxs-lookup"><span data-stu-id="d81a1-333">controlName</span></span>  

<!-- -->

<span data-ttu-id="d81a1-334">insertAfter</span><span class="sxs-lookup"><span data-stu-id="d81a1-334">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="d81a1-335">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-335">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="d81a1-336">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-336">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="d81a1-337">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-337">Parameters - addControlEx</span></span>

<span data-ttu-id="d81a1-338">controlClass</span><span class="sxs-lookup"><span data-stu-id="d81a1-338">controlClass</span></span>  

<!-- -->

<span data-ttu-id="d81a1-339">controlName</span><span class="sxs-lookup"><span data-stu-id="d81a1-339">controlName</span></span>  

<!-- -->

<span data-ttu-id="d81a1-340">insertAfter</span><span class="sxs-lookup"><span data-stu-id="d81a1-340">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="d81a1-341">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-341">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="d81a1-342">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="d81a1-342">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="d81a1-343">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="d81a1-343">Parameters - addDataField</span></span>

<span data-ttu-id="d81a1-344">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="d81a1-344">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="d81a1-345">fieldId</span><span class="sxs-lookup"><span data-stu-id="d81a1-345">fieldId</span></span>  

<!-- -->

<span data-ttu-id="d81a1-346">insertAfter</span><span class="sxs-lookup"><span data-stu-id="d81a1-346">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="d81a1-347">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="d81a1-347">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="d81a1-348">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="d81a1-348">Return Value - addDataField</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="d81a1-349">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="d81a1-349">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="d81a1-350">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="d81a1-350">Parameters - alignChild</span></span>

<span data-ttu-id="d81a1-351">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-351">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="d81a1-352">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="d81a1-352">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="d81a1-353">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="d81a1-353">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="d81a1-354">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="d81a1-354">Parameters - alignChildren</span></span>

<span data-ttu-id="d81a1-355">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-355">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="d81a1-356">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="d81a1-356">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="d81a1-357">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-357">Method alignControl</span></span>

<span data-ttu-id="d81a1-358">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-358">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="d81a1-359">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-359">Parameters - alignControl</span></span>

<span data-ttu-id="d81a1-360">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-360">value</span></span>  
<span data-ttu-id="d81a1-361">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-361">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="d81a1-362">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-362">Return Value - alignControl</span></span>

<span data-ttu-id="d81a1-363">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-363">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="d81a1-364">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-364">Remarks - alignControl</span></span>

<span data-ttu-id="d81a1-365">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-365">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="d81a1-366">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="d81a1-366">Method allowEdit</span></span>

<span data-ttu-id="d81a1-367">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-367">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="d81a1-368">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d81a1-368">Parameters - allowEdit</span></span>

<span data-ttu-id="d81a1-369">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-369">value</span></span>  
<span data-ttu-id="d81a1-370">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-370">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="d81a1-371">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d81a1-371">Return Value - allowEdit</span></span>

<span data-ttu-id="d81a1-372">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-372">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="d81a1-373">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d81a1-373">Remarks - allowEdit</span></span>

<span data-ttu-id="d81a1-374">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-374">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="d81a1-375">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="d81a1-375">Method allowSysSetup</span></span>

<span data-ttu-id="d81a1-376">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-376">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="d81a1-377">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="d81a1-377">Return Value - allowSysSetup</span></span>

<span data-ttu-id="d81a1-378">コントロールが SysSetup フォームに表示されるようになる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-378">true if the control will be shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="d81a1-379">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="d81a1-379">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="d81a1-380">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="d81a1-380">Parameters - allowUserSetup</span></span>

<span data-ttu-id="d81a1-381">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-381">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="d81a1-382">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="d81a1-382">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="d81a1-383">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="d81a1-383">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="d81a1-384">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="d81a1-384">Parameters - arrangeGuide</span></span>

<span data-ttu-id="d81a1-385">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-385">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="d81a1-386">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="d81a1-386">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="d81a1-387">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="d81a1-387">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="d81a1-388">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="d81a1-388">Parameters - arrangeMethod</span></span>

<span data-ttu-id="d81a1-389">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-389">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="d81a1-390">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="d81a1-390">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="d81a1-391">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="d81a1-391">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="d81a1-392">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="d81a1-392">Parameters - arrangeWhen</span></span>

<span data-ttu-id="d81a1-393">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-393">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="d81a1-394">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="d81a1-394">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="d81a1-395">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d81a1-395">Method autoDeclaration</span></span>

<span data-ttu-id="d81a1-396">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-396">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="d81a1-397">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d81a1-397">Parameters - autoDeclaration</span></span>

<span data-ttu-id="d81a1-398">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-398">value</span></span>  
<span data-ttu-id="d81a1-399">プロパティはこの値に設定されます (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-399">The property is set to this value; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="d81a1-400">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d81a1-400">Return Value - autoDeclaration</span></span>

<span data-ttu-id="d81a1-401">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-401">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="d81a1-402">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d81a1-402">Remarks - autoDeclaration</span></span>

<span data-ttu-id="d81a1-403">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-403">Controls cannot have identical names.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="d81a1-404">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="d81a1-404">Method beginDrag</span></span>

<span data-ttu-id="d81a1-405">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-405">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="d81a1-406">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="d81a1-406">Parameters - beginDrag</span></span>

<span data-ttu-id="d81a1-407">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-407">x</span></span>  
<span data-ttu-id="d81a1-408">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-408">An integer value that indicates the y-coordinate of the mouse pointer.</span></span>

<!-- -->

<span data-ttu-id="d81a1-409">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-409">y</span></span>  
<span data-ttu-id="d81a1-410">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-410">An integer value that indicates the y-coordinate of the mouse pointer.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="d81a1-411">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="d81a1-411">Return Value - beginDrag</span></span>

<span data-ttu-id="d81a1-412">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-412">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="d81a1-413">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="d81a1-413">Remarks - beginDrag</span></span>

<span data-ttu-id="d81a1-414">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-414">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="d81a1-415">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-415">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="d81a1-416">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-416">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="d81a1-417">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-417">Parameters - bottomMargin</span></span>

<span data-ttu-id="d81a1-418">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-418">value</span></span>  

<!-- -->

<span data-ttu-id="d81a1-419">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-419">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="d81a1-420">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-420">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="d81a1-421">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-421">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="d81a1-422">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-422">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="d81a1-423">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-423">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="d81a1-424">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-424">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="d81a1-425">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-425">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="d81a1-426">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-426">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="d81a1-427">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-427">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="d81a1-428">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-428">Return Value - bottomMarginValue</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="d81a1-429">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="d81a1-429">Method calcControlSize</span></span>

<span data-ttu-id="d81a1-430">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-430">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="d81a1-431">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="d81a1-431">Parameters - calcControlSize</span></span>

<span data-ttu-id="d81a1-432">chars</span><span class="sxs-lookup"><span data-stu-id="d81a1-432">chars</span></span>  
<span data-ttu-id="d81a1-433">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="d81a1-433">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="d81a1-434">明細行</span><span class="sxs-lookup"><span data-stu-id="d81a1-434">lines</span></span>  
<span data-ttu-id="d81a1-435">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="d81a1-435">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="d81a1-436">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="d81a1-436">Return Value - calcControlSize</span></span>

<span data-ttu-id="d81a1-437">幅と高さのあるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="d81a1-437">The container that has the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="d81a1-438">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="d81a1-438">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="d81a1-439">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="d81a1-439">Parameters - canAddDataField</span></span>

<span data-ttu-id="d81a1-440">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="d81a1-440">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="d81a1-441">fieldId</span><span class="sxs-lookup"><span data-stu-id="d81a1-441">fieldId</span></span>  

<!-- -->

<span data-ttu-id="d81a1-442">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="d81a1-442">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="d81a1-443">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="d81a1-443">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="d81a1-444">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="d81a1-444">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="d81a1-445">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="d81a1-445">Parameters - canContain</span></span>

<span data-ttu-id="d81a1-446">control</span><span class="sxs-lookup"><span data-stu-id="d81a1-446">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="d81a1-447">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="d81a1-447">Return Value - canContain</span></span>

## <a name="method-caption"></a><span data-ttu-id="d81a1-448">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="d81a1-448">Method caption</span></span>

<span data-ttu-id="d81a1-449">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-449">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="d81a1-450">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="d81a1-450">Parameters - caption</span></span>

<span data-ttu-id="d81a1-451">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-451">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="d81a1-452">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="d81a1-452">Return Value - caption</span></span>

<span data-ttu-id="d81a1-453">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="d81a1-453">The string that is used as the caption of the control.</span></span>

## <a name="method-columns"></a><span data-ttu-id="d81a1-454">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="d81a1-454">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="d81a1-455">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="d81a1-455">Parameters - columns</span></span>

<span data-ttu-id="d81a1-456">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-456">value</span></span>  

<!-- -->

<span data-ttu-id="d81a1-457">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-457">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="d81a1-458">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="d81a1-458">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="d81a1-459">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-459">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="d81a1-460">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-460">Parameters - columnsMode</span></span>

<span data-ttu-id="d81a1-461">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-461">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="d81a1-462">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-462">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="d81a1-463">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="d81a1-463">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="d81a1-464">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="d81a1-464">Parameters - columnspace</span></span>

<span data-ttu-id="d81a1-465">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-465">value</span></span>  

<!-- -->

<span data-ttu-id="d81a1-466">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-466">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="d81a1-467">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="d81a1-467">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="d81a1-468">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-468">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="d81a1-469">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-469">Parameters - columnspaceMode</span></span>

<span data-ttu-id="d81a1-470">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-470">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="d81a1-471">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-471">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="d81a1-472">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-472">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="d81a1-473">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-473">Parameters - columnspaceValue</span></span>

<span data-ttu-id="d81a1-474">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-474">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="d81a1-475">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-475">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="d81a1-476">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-476">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="d81a1-477">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-477">Parameters - columnsValue</span></span>

<span data-ttu-id="d81a1-478">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-478">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="d81a1-479">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-479">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="d81a1-480">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="d81a1-480">Method configurationKey</span></span>

<span data-ttu-id="d81a1-481">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-481">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="d81a1-482">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d81a1-482">Parameters - configurationKey</span></span>

<span data-ttu-id="d81a1-483">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-483">value</span></span>  
<span data-ttu-id="d81a1-484">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-484">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="d81a1-485">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d81a1-485">Return Value - configurationKey</span></span>

<span data-ttu-id="d81a1-486">コントロールに割り当てられるコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="d81a1-486">The ID of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="d81a1-487">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d81a1-487">Remarks - configurationKey</span></span>

<span data-ttu-id="d81a1-488">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-488">The configuration key is used to determine whether this control can be displayed.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="d81a1-489">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-489">Method configurationKeyEx</span></span>

<span data-ttu-id="d81a1-490">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-490">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="d81a1-491">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-491">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="d81a1-492">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="d81a1-492">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="d81a1-493">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-493">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="d81a1-494">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-494">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="d81a1-495">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-495">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="d81a1-496">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-496">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-contains"></a><span data-ttu-id="d81a1-497">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="d81a1-497">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="d81a1-498">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="d81a1-498">Parameters - contains</span></span>

<span data-ttu-id="d81a1-499">control</span><span class="sxs-lookup"><span data-stu-id="d81a1-499">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="d81a1-500">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="d81a1-500">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="d81a1-501">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="d81a1-501">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="d81a1-502">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="d81a1-502">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="d81a1-503">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="d81a1-503">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="d81a1-504">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="d81a1-504">Parameters - controlNum</span></span>

<span data-ttu-id="d81a1-505">controlNo</span><span class="sxs-lookup"><span data-stu-id="d81a1-505">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="d81a1-506">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="d81a1-506">Return Value - controlNum</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="d81a1-507">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d81a1-507">Method dataRelationPath</span></span>

<span data-ttu-id="d81a1-508">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-508">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="d81a1-509">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d81a1-509">Parameters - dataRelationPath</span></span>

<span data-ttu-id="d81a1-510">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-510">value</span></span>  
<span data-ttu-id="d81a1-511">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-511">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="d81a1-512">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d81a1-512">Return Value - dataRelationPath</span></span>

<span data-ttu-id="d81a1-513">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="d81a1-513">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="d81a1-514">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d81a1-514">Remarks - dataRelationPath</span></span>

<span data-ttu-id="d81a1-515">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-515">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="d81a1-516">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="d81a1-516">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="d81a1-517">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="d81a1-517">Method dataSource</span></span>

<span data-ttu-id="d81a1-518">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-518">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="d81a1-519">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="d81a1-519">Parameters - dataSource</span></span>

<span data-ttu-id="d81a1-520">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-520">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="d81a1-521">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="d81a1-521">Return Value - dataSource</span></span>

<span data-ttu-id="d81a1-522">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="d81a1-522">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="d81a1-523">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="d81a1-523">Method displayTarget</span></span>

<span data-ttu-id="d81a1-524">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-524">Gets or sets the value that indicates whether the control is displayed in the client, or in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="d81a1-525">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="d81a1-525">Parameters - displayTarget</span></span>

<span data-ttu-id="d81a1-526">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-526">value</span></span>  
<span data-ttu-id="d81a1-527">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-527">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="d81a1-528">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="d81a1-528">Return Value - displayTarget</span></span>

<span data-ttu-id="d81a1-529">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-529">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="d81a1-530">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="d81a1-530">Method dragDrop</span></span>

<span data-ttu-id="d81a1-531">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-531">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="d81a1-532">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="d81a1-532">Parameters - dragDrop</span></span>

<span data-ttu-id="d81a1-533">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-533">value</span></span>  
<span data-ttu-id="d81a1-534">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-534">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="d81a1-535">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="d81a1-535">Return Value - dragDrop</span></span>

<span data-ttu-id="d81a1-536">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-536">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="d81a1-537">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="d81a1-537">Remarks - dragDrop</span></span>

<span data-ttu-id="d81a1-538">FormControl::dragLeave メソッド、FormControl::dragOver メソッド、および FormControl::dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-538">Use the FormControl::dragLeave method , the FormControl::dragOver method, and the FormControl::dragOverEx method to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="d81a1-539">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="d81a1-539">Method dragOver</span></span>

<span data-ttu-id="d81a1-540">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-540">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="d81a1-541">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="d81a1-541">Parameters - dragOver</span></span>

<span data-ttu-id="d81a1-542">dragSource</span><span class="sxs-lookup"><span data-stu-id="d81a1-542">dragSource</span></span>  
<span data-ttu-id="d81a1-543">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-543">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-544">dragMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-544">dragMode</span></span>  
<span data-ttu-id="d81a1-545">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-545">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-546">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-546">x</span></span>  
<span data-ttu-id="d81a1-547">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-547">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-548">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-548">y</span></span>  
<span data-ttu-id="d81a1-549">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-549">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="d81a1-550">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="d81a1-550">Return Value - dragOver</span></span>

<span data-ttu-id="d81a1-551">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-551">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="d81a1-552">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-552">Method dragOverEx</span></span>

<span data-ttu-id="d81a1-553">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-553">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="d81a1-554">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-554">Parameters - dragOverEx</span></span>

<span data-ttu-id="d81a1-555">dragSource</span><span class="sxs-lookup"><span data-stu-id="d81a1-555">dragSource</span></span>  
<span data-ttu-id="d81a1-556">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-556">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-557">dragMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-557">dragMode</span></span>  
<span data-ttu-id="d81a1-558">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-558">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-559">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-559">x</span></span>  
<span data-ttu-id="d81a1-560">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-560">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-561">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-561">y</span></span>  
<span data-ttu-id="d81a1-562">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-562">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="d81a1-563">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-563">Return Value - dragOverEx</span></span>

<span data-ttu-id="d81a1-564">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-564">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="d81a1-565">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="d81a1-565">Method dragText</span></span>

<span data-ttu-id="d81a1-566">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-566">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="d81a1-567">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="d81a1-567">Return Value - dragText</span></span>

<span data-ttu-id="d81a1-568">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="d81a1-568">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="d81a1-569">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="d81a1-569">Method enabled</span></span>

<span data-ttu-id="d81a1-570">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-570">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="d81a1-571">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="d81a1-571">Parameters - enabled</span></span>

<span data-ttu-id="d81a1-572">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-572">value</span></span>  
<span data-ttu-id="d81a1-573">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-573">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="d81a1-574">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="d81a1-574">Return Value - enabled</span></span>

<span data-ttu-id="d81a1-575">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-575">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="d81a1-576">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="d81a1-576">Remarks - enabled</span></span>

<span data-ttu-id="d81a1-577">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-577">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="d81a1-578">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-578">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="d81a1-579">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-579">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="d81a1-580">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="d81a1-580">Method hasChanged</span></span>

<span data-ttu-id="d81a1-581">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-581">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="d81a1-582">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="d81a1-582">Parameters - hasChanged</span></span>

<span data-ttu-id="d81a1-583">val</span><span class="sxs-lookup"><span data-stu-id="d81a1-583">val</span></span>  
<span data-ttu-id="d81a1-584">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-584">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="d81a1-585">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="d81a1-585">Return Value - hasChanged</span></span>

<span data-ttu-id="d81a1-586">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-586">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="d81a1-587">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="d81a1-587">Method hasUserSetting</span></span>

<span data-ttu-id="d81a1-588">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-588">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="d81a1-589">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="d81a1-589">Return Value - hasUserSetting</span></span>

<span data-ttu-id="d81a1-590">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-590">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="d81a1-591">メソッド height</span><span class="sxs-lookup"><span data-stu-id="d81a1-591">Method height</span></span>

<span data-ttu-id="d81a1-592">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-592">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="d81a1-593">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="d81a1-593">Parameters - height</span></span>

<span data-ttu-id="d81a1-594">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-594">value</span></span>  
<span data-ttu-id="d81a1-595">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-595">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="d81a1-596">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-596">mode</span></span>  
<span data-ttu-id="d81a1-597">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-597">An Integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="d81a1-598">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="d81a1-598">Return Value - height</span></span>

<span data-ttu-id="d81a1-599">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="d81a1-599">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="d81a1-600">備考 - height</span><span class="sxs-lookup"><span data-stu-id="d81a1-600">Remarks - height</span></span>

<span data-ttu-id="d81a1-601">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-601">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="d81a1-602">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="d81a1-602">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="d81a1-603">モード。</span><span class="sxs-lookup"><span data-stu-id="d81a1-603">Mode.</span></span>            | <span data-ttu-id="d81a1-604">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="d81a1-604">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81a1-605">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="d81a1-605">-1 Exact.</span></span>        | <span data-ttu-id="d81a1-606">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-606">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d81a1-607">0 自動。</span><span class="sxs-lookup"><span data-stu-id="d81a1-607">0 Auto.</span></span>          | <span data-ttu-id="d81a1-608">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-608">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d81a1-609">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="d81a1-609">1 Column height.</span></span> | <span data-ttu-id="d81a1-610">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-610">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="d81a1-611">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-611">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="d81a1-612">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-612">Method heightMode</span></span>

<span data-ttu-id="d81a1-613">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-613">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="d81a1-614">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-614">Parameters - heightMode</span></span>

<span data-ttu-id="d81a1-615">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-615">value</span></span>  
<span data-ttu-id="d81a1-616">コントロールの高さの計算方法を示す整数値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-616">An Integer value that indicates how the control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="d81a1-617">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-617">Return Value - heightMode</span></span>

<span data-ttu-id="d81a1-618">計算モード。</span><span class="sxs-lookup"><span data-stu-id="d81a1-618">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="d81a1-619">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-619">Remarks - heightMode</span></span>

<span data-ttu-id="d81a1-620">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="d81a1-620">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="d81a1-621">モード。</span><span class="sxs-lookup"><span data-stu-id="d81a1-621">Mode.</span></span>          | <span data-ttu-id="d81a1-622">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="d81a1-622">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81a1-623">正確。</span><span class="sxs-lookup"><span data-stu-id="d81a1-623">Exact.</span></span>         | <span data-ttu-id="d81a1-624">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-624">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d81a1-625">自動。</span><span class="sxs-lookup"><span data-stu-id="d81a1-625">Auto.</span></span>          | <span data-ttu-id="d81a1-626">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-626">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d81a1-627">列の高さ</span><span class="sxs-lookup"><span data-stu-id="d81a1-627">Column height.</span></span> | <span data-ttu-id="d81a1-628">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-628">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="d81a1-629">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-629">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="d81a1-630">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-630">Method heightValue</span></span>

<span data-ttu-id="d81a1-631">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-631">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="d81a1-632">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-632">Parameters - heightValue</span></span>

<span data-ttu-id="d81a1-633">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-633">value</span></span>  
<span data-ttu-id="d81a1-634">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-634">An Integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="d81a1-635">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-635">Return Value - heightValue</span></span>

<span data-ttu-id="d81a1-636">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="d81a1-636">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="d81a1-637">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-637">Remarks - heightValue</span></span>

<span data-ttu-id="d81a1-638">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-638">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="d81a1-639">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="d81a1-639">Method helpField</span></span>

<span data-ttu-id="d81a1-640">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-640">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="d81a1-641">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="d81a1-641">Return Value - helpField</span></span>

<span data-ttu-id="d81a1-642">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="d81a1-642">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="d81a1-643">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="d81a1-643">Remarks - helpField</span></span>

<span data-ttu-id="d81a1-644">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-644">The helpField method cannot be used to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="d81a1-645">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="d81a1-645">Method helpText</span></span>

<span data-ttu-id="d81a1-646">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-646">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="d81a1-647">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="d81a1-647">Parameters - helpText</span></span>

<span data-ttu-id="d81a1-648">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-648">value</span></span>  
<span data-ttu-id="d81a1-649">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-649">The value that is assigned as the help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="d81a1-650">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="d81a1-650">Return Value - helpText</span></span>

<span data-ttu-id="d81a1-651">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="d81a1-651">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="d81a1-652">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="d81a1-652">Remarks - helpText</span></span>

<span data-ttu-id="d81a1-653">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-653">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="d81a1-654">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-654">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="d81a1-655">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="d81a1-655">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="d81a1-656">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="d81a1-656">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="d81a1-657">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-657">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="d81a1-658">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="d81a1-658">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="d81a1-659">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d81a1-659">Method hierarchyParent</span></span>

<span data-ttu-id="d81a1-660">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-660">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="d81a1-661">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d81a1-661">Parameters - hierarchyParent</span></span>

<span data-ttu-id="d81a1-662">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-662">value</span></span>  
<span data-ttu-id="d81a1-663">コントロールの HierarchyParent 値として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-663">The value to assign as the HierarchyParent value of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="d81a1-664">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d81a1-664">Return Value - hierarchyParent</span></span>

<span data-ttu-id="d81a1-665">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-665">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="d81a1-666">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="d81a1-666">Method hWnd</span></span>

<span data-ttu-id="d81a1-667">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-667">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="d81a1-668">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="d81a1-668">Return Value - hWnd</span></span>

<span data-ttu-id="d81a1-669">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="d81a1-669">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="d81a1-670">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="d81a1-670">Remarks - hWnd</span></span>

<span data-ttu-id="d81a1-671">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-671">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="d81a1-672">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="d81a1-672">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="d81a1-673">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="d81a1-673">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="d81a1-674">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="d81a1-674">Method isDisplayed</span></span>

<span data-ttu-id="d81a1-675">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-675">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="d81a1-676">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="d81a1-676">Return Value - isDisplayed</span></span>

<span data-ttu-id="d81a1-677">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-677">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="d81a1-678">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="d81a1-678">Remarks - isDisplayed</span></span>

<span data-ttu-id="d81a1-679">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-679">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="d81a1-680">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="d81a1-680">Method isRestricted</span></span>

<span data-ttu-id="d81a1-681">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-681">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="d81a1-682">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="d81a1-682">Return Value - isRestricted</span></span>

<span data-ttu-id="d81a1-683">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-683">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="d81a1-684">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="d81a1-684">Method isUserSetupEnabled</span></span>

<span data-ttu-id="d81a1-685">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-685">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="d81a1-686">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="d81a1-686">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="d81a1-687">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="d81a1-687">neededSetupRights</span></span>  
<span data-ttu-id="d81a1-688">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-688">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="d81a1-689">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="d81a1-689">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="d81a1-690">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-690">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="d81a1-691">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="d81a1-691">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="d81a1-692">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-692">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81a1-693">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="d81a1-693">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="d81a1-694">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-694">No changes can be made to the control.</span></span> <span data-ttu-id="d81a1-695">neededSetupRights パラメーターにこの値を使用すると、常に、true が返ってきます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-695">Using this value for the neededSetupRights parameter always returns true.</span></span>                 |
| <span data-ttu-id="d81a1-696">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="d81a1-696">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="d81a1-697">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-697">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="d81a1-698">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-698">The user cannot move the control.</span></span>   |
| <span data-ttu-id="d81a1-699">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="d81a1-699">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="d81a1-700">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-700">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="d81a1-701">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-701">The user can also move the control.</span></span> |

<span data-ttu-id="d81a1-702">このメソッドは、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメーターで指定されたアクセスレベルを許可している場合にのみ true を返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-702">This method returns true only if the AllowUserSetup property for the design and all parent containers allows for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-leave"></a><span data-ttu-id="d81a1-703">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="d81a1-703">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="d81a1-704">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="d81a1-704">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="d81a1-705">メソッド left</span><span class="sxs-lookup"><span data-stu-id="d81a1-705">Method left</span></span>

<span data-ttu-id="d81a1-706">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-706">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="d81a1-707">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="d81a1-707">Parameters - left</span></span>

<span data-ttu-id="d81a1-708">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-708">value</span></span>  
<span data-ttu-id="d81a1-709">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-709">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="d81a1-710">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-710">mode</span></span>  
<span data-ttu-id="d81a1-711">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-711">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="d81a1-712">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="d81a1-712">Return Value - left</span></span>

<span data-ttu-id="d81a1-713">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="d81a1-713">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="d81a1-714">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-714">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="d81a1-715">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-715">Parameters - leftMargin</span></span>

<span data-ttu-id="d81a1-716">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-716">value</span></span>  

<!-- -->

<span data-ttu-id="d81a1-717">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-717">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="d81a1-718">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-718">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="d81a1-719">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-719">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="d81a1-720">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-720">Parameters - leftMarginMode</span></span>

<span data-ttu-id="d81a1-721">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-721">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="d81a1-722">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-722">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="d81a1-723">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-723">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="d81a1-724">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-724">Parameters - leftMarginValue</span></span>

<span data-ttu-id="d81a1-725">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-725">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="d81a1-726">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-726">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="d81a1-727">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-727">Method leftMode</span></span>

<span data-ttu-id="d81a1-728">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-728">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="d81a1-729">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-729">Parameters - leftMode</span></span>

<span data-ttu-id="d81a1-730">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-730">value</span></span>  
<span data-ttu-id="d81a1-731">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-731">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="d81a1-732">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-732">Return Value - leftMode</span></span>

<span data-ttu-id="d81a1-733">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="d81a1-733">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="d81a1-734">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-734">Method leftValue</span></span>

<span data-ttu-id="d81a1-735">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-735">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="d81a1-736">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-736">Parameters - leftValue</span></span>

<span data-ttu-id="d81a1-737">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-737">value</span></span>  
<span data-ttu-id="d81a1-738">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-738">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="d81a1-739">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-739">Return Value - leftValue</span></span>

<span data-ttu-id="d81a1-740">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="d81a1-740">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="d81a1-741">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="d81a1-741">Method markAsUserAdd</span></span>

<span data-ttu-id="d81a1-742">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="d81a1-742">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="d81a1-743">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="d81a1-743">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="d81a1-744">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-744">value</span></span>  
<span data-ttu-id="d81a1-745">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-745">A Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="d81a1-746">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="d81a1-746">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="d81a1-747">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-747">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="d81a1-748">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="d81a1-748">Method mouseDblClick</span></span>

<span data-ttu-id="d81a1-749">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-749">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="d81a1-750">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="d81a1-750">Parameters - mouseDblClick</span></span>

<span data-ttu-id="d81a1-751">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-751">x</span></span>  
<span data-ttu-id="d81a1-752">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-752">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-753">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-753">y</span></span>  
<span data-ttu-id="d81a1-754">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-754">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-755">ボタン</span><span class="sxs-lookup"><span data-stu-id="d81a1-755">button</span></span>  
<span data-ttu-id="d81a1-756">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-756">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-757">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d81a1-757">Ctrl</span></span>  
<span data-ttu-id="d81a1-758">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-758">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-759">シフト</span><span class="sxs-lookup"><span data-stu-id="d81a1-759">Shift</span></span>  
<span data-ttu-id="d81a1-760">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-760">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="d81a1-761">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="d81a1-761">Return Value - mouseDblClick</span></span>

<span data-ttu-id="d81a1-762">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-762">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="d81a1-763">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="d81a1-763">Remarks - mouseDblClick</span></span>

<span data-ttu-id="d81a1-764">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-764">Typically, when this method is overridden, the return value from a call to super is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="d81a1-765">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="d81a1-765">Method mouseDown</span></span>

<span data-ttu-id="d81a1-766">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-766">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="d81a1-767">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="d81a1-767">Parameters - mouseDown</span></span>

<span data-ttu-id="d81a1-768">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-768">x</span></span>  
<span data-ttu-id="d81a1-769">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-769">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-770">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-770">y</span></span>  
<span data-ttu-id="d81a1-771">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-771">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-772">ボタン</span><span class="sxs-lookup"><span data-stu-id="d81a1-772">button</span></span>  
<span data-ttu-id="d81a1-773">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-773">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-774">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d81a1-774">Ctrl</span></span>  
<span data-ttu-id="d81a1-775">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-775">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-776">シフト</span><span class="sxs-lookup"><span data-stu-id="d81a1-776">Shift</span></span>  
<span data-ttu-id="d81a1-777">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-777">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="d81a1-778">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="d81a1-778">Return Value - mouseDown</span></span>

<span data-ttu-id="d81a1-779">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-779">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="d81a1-780">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="d81a1-780">Remarks - mouseDown</span></span>

<span data-ttu-id="d81a1-781">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-781">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="d81a1-782">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-782">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="d81a1-783">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="d81a1-783">Method mouseMove</span></span>

<span data-ttu-id="d81a1-784">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-784">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="d81a1-785">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="d81a1-785">Parameters - mouseMove</span></span>

<span data-ttu-id="d81a1-786">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-786">x</span></span>  
<span data-ttu-id="d81a1-787">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-787">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-788">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-788">y</span></span>  
<span data-ttu-id="d81a1-789">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-789">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-790">ボタン</span><span class="sxs-lookup"><span data-stu-id="d81a1-790">button</span></span>  
<span data-ttu-id="d81a1-791">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-791">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-792">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d81a1-792">Ctrl</span></span>  
<span data-ttu-id="d81a1-793">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-793">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-794">シフト</span><span class="sxs-lookup"><span data-stu-id="d81a1-794">Shift</span></span>  
<span data-ttu-id="d81a1-795">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-795">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="d81a1-796">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="d81a1-796">Return Value - mouseMove</span></span>

<span data-ttu-id="d81a1-797">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-797">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="d81a1-798">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="d81a1-798">Remarks - mouseMove</span></span>

<span data-ttu-id="d81a1-799">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-799">Typically, when this method is overridden, the return value from a call to super is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="d81a1-800">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="d81a1-800">Method mouseUp</span></span>

<span data-ttu-id="d81a1-801">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-801">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="d81a1-802">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="d81a1-802">Parameters - mouseUp</span></span>

<span data-ttu-id="d81a1-803">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-803">x</span></span>  
<span data-ttu-id="d81a1-804">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-804">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-805">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-805">y</span></span>  
<span data-ttu-id="d81a1-806">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-806">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-807">ボタン</span><span class="sxs-lookup"><span data-stu-id="d81a1-807">button</span></span>  
<span data-ttu-id="d81a1-808">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-808">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-809">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d81a1-809">Ctrl</span></span>  
<span data-ttu-id="d81a1-810">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-810">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-811">シフト</span><span class="sxs-lookup"><span data-stu-id="d81a1-811">Shift</span></span>  
<span data-ttu-id="d81a1-812">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-812">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="d81a1-813">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="d81a1-813">Return Value - mouseUp</span></span>

<span data-ttu-id="d81a1-814">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-814">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="d81a1-815">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="d81a1-815">Remarks - mouseUp</span></span>

<span data-ttu-id="d81a1-816">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-816">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="d81a1-817">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-817">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="d81a1-818">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-818">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="d81a1-819">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-819">Parameters - moveControl</span></span>

<span data-ttu-id="d81a1-820">controlId</span><span class="sxs-lookup"><span data-stu-id="d81a1-820">controlId</span></span>  

<!-- -->

<span data-ttu-id="d81a1-821">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="d81a1-821">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="d81a1-822">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-822">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="d81a1-823">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d81a1-823">Method name</span></span>

<span data-ttu-id="d81a1-824">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-824">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="d81a1-825">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="d81a1-825">Parameters - name</span></span>

<span data-ttu-id="d81a1-826">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-826">value</span></span>  
<span data-ttu-id="d81a1-827">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="d81a1-827">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="d81a1-828">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="d81a1-828">Return Value - name</span></span>

<span data-ttu-id="d81a1-829">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="d81a1-829">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="d81a1-830">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="d81a1-830">Remarks - name</span></span>

<span data-ttu-id="d81a1-831">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-831">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="d81a1-832">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-832">Begins with a letter.</span></span>
-   <span data-ttu-id="d81a1-833">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="d81a1-833">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="d81a1-834">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-834">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="d81a1-835">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-835">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="d81a1-836">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-836">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="d81a1-837">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="d81a1-837">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="d81a1-838">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="d81a1-838">Parameters - neededPermission</span></span>

<span data-ttu-id="d81a1-839">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-839">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="d81a1-840">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="d81a1-840">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="d81a1-841">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d81a1-841">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="d81a1-842">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d81a1-842">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="d81a1-843">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-843">Method parentControl</span></span>

<span data-ttu-id="d81a1-844">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-844">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="d81a1-845">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-845">Return Value - parentControl</span></span>

<span data-ttu-id="d81a1-846">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="d81a1-846">The parent control for the control.</span></span>

## <a name="method-position"></a><span data-ttu-id="d81a1-847">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="d81a1-847">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="d81a1-848">パラメーター - 位置</span><span class="sxs-lookup"><span data-stu-id="d81a1-848">Parameters - position</span></span>

<span data-ttu-id="d81a1-849">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-849">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="d81a1-850">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="d81a1-850">Return Value - position</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="d81a1-851">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-851">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="d81a1-852">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-852">Parameters - rightMargin</span></span>

<span data-ttu-id="d81a1-853">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-853">value</span></span>  

<!-- -->

<span data-ttu-id="d81a1-854">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-854">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="d81a1-855">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-855">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="d81a1-856">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-856">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="d81a1-857">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-857">Parameters - rightMarginMode</span></span>

<span data-ttu-id="d81a1-858">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-858">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="d81a1-859">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-859">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="d81a1-860">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-860">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="d81a1-861">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-861">Parameters - rightMarginValue</span></span>

<span data-ttu-id="d81a1-862">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-862">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="d81a1-863">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-863">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="d81a1-864">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="d81a1-864">Method securityKey</span></span>

<span data-ttu-id="d81a1-865">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-865">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="d81a1-866">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="d81a1-866">Parameters - securityKey</span></span>

<span data-ttu-id="d81a1-867">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-867">value</span></span>  
<span data-ttu-id="d81a1-868">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-868">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="d81a1-869">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="d81a1-869">Return Value - securityKey</span></span>

<span data-ttu-id="d81a1-870">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-870">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="d81a1-871">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="d81a1-871">Method showContextMenu</span></span>

<span data-ttu-id="d81a1-872">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-872">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="d81a1-873">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="d81a1-873">Parameters - showContextMenu</span></span>

<span data-ttu-id="d81a1-874">menuHandle</span><span class="sxs-lookup"><span data-stu-id="d81a1-874">menuHandle</span></span>  
<span data-ttu-id="d81a1-875">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="d81a1-875">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="d81a1-876">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="d81a1-876">Return Value - showContextMenu</span></span>

<span data-ttu-id="d81a1-877">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-877">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="d81a1-878">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="d81a1-878">Method skip</span></span>

<span data-ttu-id="d81a1-879">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-879">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="d81a1-880">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="d81a1-880">Parameters - skip</span></span>

<span data-ttu-id="d81a1-881">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-881">value</span></span>  
<span data-ttu-id="d81a1-882">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-882">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="d81a1-883">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="d81a1-883">Return Value - skip</span></span>

<span data-ttu-id="d81a1-884">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-884">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="d81a1-885">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="d81a1-885">Remarks - skip</span></span>

<span data-ttu-id="d81a1-886">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-886">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="d81a1-887">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="d81a1-887">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="d81a1-888">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="d81a1-888">Parameters - sort</span></span>

<span data-ttu-id="d81a1-889">sortDirection</span><span class="sxs-lookup"><span data-stu-id="d81a1-889">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="d81a1-890">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="d81a1-890">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="d81a1-891">メソッド style</span><span class="sxs-lookup"><span data-stu-id="d81a1-891">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="d81a1-892">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="d81a1-892">Parameters - style</span></span>

<span data-ttu-id="d81a1-893">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-893">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="d81a1-894">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="d81a1-894">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="d81a1-895">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="d81a1-895">Method toolTip</span></span>

<span data-ttu-id="d81a1-896">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-896">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="d81a1-897">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="d81a1-897">Return Value - toolTip</span></span>

<span data-ttu-id="d81a1-898">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="d81a1-898">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="d81a1-899">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="d81a1-899">Remarks - toolTip</span></span>

<span data-ttu-id="d81a1-900">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-900">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="d81a1-901">メソッド top</span><span class="sxs-lookup"><span data-stu-id="d81a1-901">Method top</span></span>

<span data-ttu-id="d81a1-902">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-902">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="d81a1-903">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="d81a1-903">Parameters - top</span></span>

<span data-ttu-id="d81a1-904">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-904">value</span></span>  
<span data-ttu-id="d81a1-905">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-905">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="d81a1-906">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-906">mode</span></span>  
<span data-ttu-id="d81a1-907">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-907">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="d81a1-908">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="d81a1-908">Return Value - top</span></span>

<span data-ttu-id="d81a1-909">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="d81a1-909">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="d81a1-910">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-910">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="d81a1-911">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-911">Parameters - topMargin</span></span>

<span data-ttu-id="d81a1-912">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-912">value</span></span>  

<!-- -->

<span data-ttu-id="d81a1-913">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-913">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="d81a1-914">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="d81a1-914">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="d81a1-915">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-915">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="d81a1-916">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-916">Parameters - topMarginMode</span></span>

<span data-ttu-id="d81a1-917">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-917">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="d81a1-918">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-918">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="d81a1-919">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-919">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="d81a1-920">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-920">Parameters - topMarginValue</span></span>

<span data-ttu-id="d81a1-921">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-921">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="d81a1-922">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-922">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="d81a1-923">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-923">Method topMode</span></span>

<span data-ttu-id="d81a1-924">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-924">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="d81a1-925">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-925">Parameters - topMode</span></span>

<span data-ttu-id="d81a1-926">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-926">value</span></span>  
<span data-ttu-id="d81a1-927">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-927">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="d81a1-928">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-928">Return Value - topMode</span></span>

<span data-ttu-id="d81a1-929">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="d81a1-929">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="d81a1-930">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-930">Method topValue</span></span>

<span data-ttu-id="d81a1-931">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-931">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="d81a1-932">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-932">Parameters - topValue</span></span>

<span data-ttu-id="d81a1-933">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-933">value</span></span>  
<span data-ttu-id="d81a1-934">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-934">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="d81a1-935">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-935">Return Value - topValue</span></span>

<span data-ttu-id="d81a1-936">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="d81a1-936">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="d81a1-937">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="d81a1-937">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="d81a1-938">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="d81a1-938">Parameters - type</span></span>

<span data-ttu-id="d81a1-939">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-939">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="d81a1-940">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="d81a1-940">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="d81a1-941">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d81a1-941">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="d81a1-942">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d81a1-942">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="d81a1-943">データ</span><span class="sxs-lookup"><span data-stu-id="d81a1-943">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="d81a1-944">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d81a1-944">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="d81a1-945">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="d81a1-945">Method userData</span></span>

<span data-ttu-id="d81a1-946">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-946">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="d81a1-947">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="d81a1-947">Parameters - userData</span></span>

<span data-ttu-id="d81a1-948">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-948">value</span></span>  
<span data-ttu-id="d81a1-949">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-949">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="d81a1-950">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="d81a1-950">Return Value - userData</span></span>

<span data-ttu-id="d81a1-951">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="d81a1-951">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="d81a1-952">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="d81a1-952">Method userDataItem</span></span>

<span data-ttu-id="d81a1-953">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-953">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="d81a1-954">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="d81a1-954">Parameters - userDataItem</span></span>

<span data-ttu-id="d81a1-955">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-955">value</span></span>  
<span data-ttu-id="d81a1-956">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-956">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="d81a1-957">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="d81a1-957">Return Value - userDataItem</span></span>

<span data-ttu-id="d81a1-958">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="d81a1-958">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="d81a1-959">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="d81a1-959">Method userDataItems</span></span>

<span data-ttu-id="d81a1-960">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-960">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="d81a1-961">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="d81a1-961">Parameters - userDataItems</span></span>

<span data-ttu-id="d81a1-962">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-962">value</span></span>  
<span data-ttu-id="d81a1-963">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-963">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="d81a1-964">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="d81a1-964">Return Value - userDataItems</span></span>

<span data-ttu-id="d81a1-965">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="d81a1-965">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="d81a1-966">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="d81a1-966">Method userDisable</span></span>

<span data-ttu-id="d81a1-967">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-967">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="d81a1-968">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="d81a1-968">Parameters - userDisable</span></span>

<span data-ttu-id="d81a1-969">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-969">value</span></span>  
<span data-ttu-id="d81a1-970">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-970">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="d81a1-971">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="d81a1-971">Return Value - userDisable</span></span>

<span data-ttu-id="d81a1-972">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-972">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="d81a1-973">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="d81a1-973">Method userHeight</span></span>

<span data-ttu-id="d81a1-974">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-974">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="d81a1-975">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="d81a1-975">Parameters - userHeight</span></span>

<span data-ttu-id="d81a1-976">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-976">value</span></span>  
<span data-ttu-id="d81a1-977">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-977">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="d81a1-978">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="d81a1-978">Return Value - userHeight</span></span>

<span data-ttu-id="d81a1-979">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="d81a1-979">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="d81a1-980">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="d81a1-980">Method userHide</span></span>

<span data-ttu-id="d81a1-981">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-981">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="d81a1-982">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="d81a1-982">Parameters - userHide</span></span>

<span data-ttu-id="d81a1-983">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-983">value</span></span>  
<span data-ttu-id="d81a1-984">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-984">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="d81a1-985">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="d81a1-985">Return Value - userHide</span></span>

<span data-ttu-id="d81a1-986">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-986">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="d81a1-987">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="d81a1-987">Remarks - userHide</span></span>

<span data-ttu-id="d81a1-988">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-988">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="d81a1-989">右クリックすると、コントロールを非表示または表示できるメニューが起動します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-989">Right-clicking invokes a menu that enables the control to be hidden or displayed.</span></span> <span data-ttu-id="d81a1-990">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-990">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="d81a1-991">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="d81a1-991">Method userOrgContainer</span></span>

<span data-ttu-id="d81a1-992">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-992">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="d81a1-993">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="d81a1-993">Parameters - userOrgContainer</span></span>

<span data-ttu-id="d81a1-994">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-994">value</span></span>  
<span data-ttu-id="d81a1-995">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-995">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="d81a1-996">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="d81a1-996">Return Value - userOrgContainer</span></span>

<span data-ttu-id="d81a1-997">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="d81a1-997">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="d81a1-998">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="d81a1-998">Method userOrgSibling</span></span>

<span data-ttu-id="d81a1-999">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-999">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="d81a1-1000">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="d81a1-1000">Parameters - userOrgSibling</span></span>

<span data-ttu-id="d81a1-1001">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1001">value</span></span>  
<span data-ttu-id="d81a1-1002">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1002">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="d81a1-1003">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="d81a1-1003">Return Value - userOrgSibling</span></span>

<span data-ttu-id="d81a1-1004">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1004">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="d81a1-1005">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="d81a1-1005">Method userPromptText</span></span>

<span data-ttu-id="d81a1-1006">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1006">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="d81a1-1007">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="d81a1-1007">Parameters - userPromptText</span></span>

<span data-ttu-id="d81a1-1008">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1008">value</span></span>  
<span data-ttu-id="d81a1-1009">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1009">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="d81a1-1010">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="d81a1-1010">Return Value - userPromptText</span></span>

<span data-ttu-id="d81a1-1011">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1011">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="d81a1-1012">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="d81a1-1012">Method userSecurityLevel</span></span>

<span data-ttu-id="d81a1-1013">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1013">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="d81a1-1014">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="d81a1-1014">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="d81a1-1015">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1015">value</span></span>  
<span data-ttu-id="d81a1-1016">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1016">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="d81a1-1017">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="d81a1-1017">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="d81a1-1018">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1018">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="d81a1-1019">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="d81a1-1019">Method userSkip</span></span>

<span data-ttu-id="d81a1-1020">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1020">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="d81a1-1021">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="d81a1-1021">Parameters - userSkip</span></span>

<span data-ttu-id="d81a1-1022">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1022">value</span></span>  
<span data-ttu-id="d81a1-1023">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1023">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="d81a1-1024">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1024">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="d81a1-1025">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="d81a1-1025">Return Value - userSkip</span></span>

<span data-ttu-id="d81a1-1026">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1026">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="d81a1-1027">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="d81a1-1027">Method userWidth</span></span>

<span data-ttu-id="d81a1-1028">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1028">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="d81a1-1029">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="d81a1-1029">Parameters - userWidth</span></span>

<span data-ttu-id="d81a1-1030">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1030">value</span></span>  
<span data-ttu-id="d81a1-1031">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1031">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="d81a1-1032">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="d81a1-1032">Return Value - userWidth</span></span>

<span data-ttu-id="d81a1-1033">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1033">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="d81a1-1034">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="d81a1-1034">Remarks - userWidth</span></span>

<span data-ttu-id="d81a1-1035">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1035">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="d81a1-1036">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻りは 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1036">For example, if the user has specified 30 characters as the width for the control, the return is 6 \* 30 = 180.</span></span> <span data-ttu-id="d81a1-1037">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1037">To specify the width of the control in characters, users can right-click the control to invoke the setup form in which the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="d81a1-1038">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="d81a1-1038">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="d81a1-1039">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="d81a1-1039">Parameters - useUserLayout</span></span>

<span data-ttu-id="d81a1-1040">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1040">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="d81a1-1041">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="d81a1-1041">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="d81a1-1042">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d81a1-1042">Method verticalSpacing</span></span>

<span data-ttu-id="d81a1-1043">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1043">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="d81a1-1044">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d81a1-1044">Parameters - verticalSpacing</span></span>

<span data-ttu-id="d81a1-1045">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1045">value</span></span>  
<span data-ttu-id="d81a1-1046">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1046">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1047">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-1047">mode</span></span>  
<span data-ttu-id="d81a1-1048">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1048">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="d81a1-1049">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d81a1-1049">Return Value - verticalSpacing</span></span>

<span data-ttu-id="d81a1-1050">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1050">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="d81a1-1051">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-1051">Method verticalSpacingMode</span></span>

<span data-ttu-id="d81a1-1052">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1052">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="d81a1-1053">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-1053">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="d81a1-1054">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-1054">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="d81a1-1055">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-1055">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="d81a1-1056">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1056">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="d81a1-1057">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-1057">Method verticalSpacingValue</span></span>

<span data-ttu-id="d81a1-1058">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1058">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="d81a1-1059">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-1059">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="d81a1-1060">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1060">value</span></span>  
<span data-ttu-id="d81a1-1061">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1061">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="d81a1-1062">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-1062">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="d81a1-1063">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1063">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="d81a1-1064">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="d81a1-1064">Method visible</span></span>

<span data-ttu-id="d81a1-1065">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1065">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="d81a1-1066">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="d81a1-1066">Parameters - visible</span></span>

<span data-ttu-id="d81a1-1067">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1067">value</span></span>  
<span data-ttu-id="d81a1-1068">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1068">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="d81a1-1069">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="d81a1-1069">Return Value - visible</span></span>

<span data-ttu-id="d81a1-1070">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1070">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="d81a1-1071">メソッド width</span><span class="sxs-lookup"><span data-stu-id="d81a1-1071">Method width</span></span>

<span data-ttu-id="d81a1-1072">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1072">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="d81a1-1073">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="d81a1-1073">Parameters - width</span></span>

<span data-ttu-id="d81a1-1074">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1074">value</span></span>  
<span data-ttu-id="d81a1-1075">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1075">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1076">モード</span><span class="sxs-lookup"><span data-stu-id="d81a1-1076">mode</span></span>  
<span data-ttu-id="d81a1-1077">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1077">An Integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="d81a1-1078">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="d81a1-1078">Return Value - width</span></span>

<span data-ttu-id="d81a1-1079">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1079">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="d81a1-1080">備考 - width</span><span class="sxs-lookup"><span data-stu-id="d81a1-1080">Remarks - width</span></span>

<span data-ttu-id="d81a1-1081">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1081">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="d81a1-1082">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="d81a1-1082">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="d81a1-1083">モード。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1083">Mode.</span></span>           | <span data-ttu-id="d81a1-1084">幅計算。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1084">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81a1-1085">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1085">-1 Exact.</span></span>       | <span data-ttu-id="d81a1-1086">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1086">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d81a1-1087">0 自動。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1087">0 Auto.</span></span>         | <span data-ttu-id="d81a1-1088">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1088">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d81a1-1089">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1089">1 Column width.</span></span> | <span data-ttu-id="d81a1-1090">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1090">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="d81a1-1091">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1091">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="d81a1-1092">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-1092">Method widthMode</span></span>

<span data-ttu-id="d81a1-1093">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1093">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="d81a1-1094">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-1094">Parameters - widthMode</span></span>

<span data-ttu-id="d81a1-1095">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1095">value</span></span>  
<span data-ttu-id="d81a1-1096">コントロール幅の計算方法を示す整数値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1096">An Integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="d81a1-1097">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-1097">Return Value - widthMode</span></span>

<span data-ttu-id="d81a1-1098">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1098">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="d81a1-1099">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-1099">Remarks - widthMode</span></span>

<span data-ttu-id="d81a1-1100">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="d81a1-1100">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="d81a1-1101">モード。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1101">Mode.</span></span>         | <span data-ttu-id="d81a1-1102">幅計算。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1102">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81a1-1103">正確。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1103">Exact.</span></span>        | <span data-ttu-id="d81a1-1104">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1104">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d81a1-1105">自動。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1105">Auto.</span></span>         | <span data-ttu-id="d81a1-1106">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1106">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d81a1-1107">列の幅。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1107">Column width.</span></span> | <span data-ttu-id="d81a1-1108">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1108">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="d81a1-1109">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1109">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="d81a1-1110">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-1110">Method widthValue</span></span>

<span data-ttu-id="d81a1-1111">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1111">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="d81a1-1112">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-1112">Parameters - widthValue</span></span>

<span data-ttu-id="d81a1-1113">値</span><span class="sxs-lookup"><span data-stu-id="d81a1-1113">value</span></span>  
<span data-ttu-id="d81a1-1114">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1114">An Integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="d81a1-1115">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-1115">Return Value - widthValue</span></span>

<span data-ttu-id="d81a1-1116">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1116">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="d81a1-1117">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="d81a1-1117">Remarks - widthValue</span></span>

<span data-ttu-id="d81a1-1118">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1118">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-drop"></a><span data-ttu-id="d81a1-1119">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="d81a1-1119">Method drop</span></span>

<span data-ttu-id="d81a1-1120">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1120">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="d81a1-1121">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="d81a1-1121">Parameters - drop</span></span>

<span data-ttu-id="d81a1-1122">dragSource</span><span class="sxs-lookup"><span data-stu-id="d81a1-1122">dragSource</span></span>  
<span data-ttu-id="d81a1-1123">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1123">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1124">dragMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-1124">dragMode</span></span>  
<span data-ttu-id="d81a1-1125">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1125">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1126">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-1126">x</span></span>  
<span data-ttu-id="d81a1-1127">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1127">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1128">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-1128">y</span></span>  
<span data-ttu-id="d81a1-1129">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1129">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="d81a1-1130">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="d81a1-1130">Method lostFocus</span></span>

<span data-ttu-id="d81a1-1131">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1131">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-filter"></a><span data-ttu-id="d81a1-1132">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="d81a1-1132">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="d81a1-1133">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="d81a1-1133">Parameters - filter</span></span>

<span data-ttu-id="d81a1-1134">filterStr</span><span class="sxs-lookup"><span data-stu-id="d81a1-1134">filterStr</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="d81a1-1135">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="d81a1-1135">Method dragLeave</span></span>

<span data-ttu-id="d81a1-1136">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1136">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-mouseenter"></a><span data-ttu-id="d81a1-1137">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="d81a1-1137">Method mouseEnter</span></span>

<span data-ttu-id="d81a1-1138">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1138">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="d81a1-1139">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="d81a1-1139">Parameters - mouseEnter</span></span>

<span data-ttu-id="d81a1-1140">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-1140">x</span></span>  
<span data-ttu-id="d81a1-1141">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1141">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1142">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-1142">y</span></span>  
<span data-ttu-id="d81a1-1143">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1143">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1144">ボタン</span><span class="sxs-lookup"><span data-stu-id="d81a1-1144">button</span></span>  
<span data-ttu-id="d81a1-1145">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1145">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1146">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d81a1-1146">Ctrl</span></span>  
<span data-ttu-id="d81a1-1147">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1147">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1148">シフト</span><span class="sxs-lookup"><span data-stu-id="d81a1-1148">Shift</span></span>  
<span data-ttu-id="d81a1-1149">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1149">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-gotfocus"></a><span data-ttu-id="d81a1-1150">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="d81a1-1150">Method gotFocus</span></span>

<span data-ttu-id="d81a1-1151">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1151">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-mouseleave"></a><span data-ttu-id="d81a1-1152">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="d81a1-1152">Method mouseLeave</span></span>

<span data-ttu-id="d81a1-1153">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1153">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-setarea"></a><span data-ttu-id="d81a1-1154">メソッド setArea</span><span class="sxs-lookup"><span data-stu-id="d81a1-1154">Method setArea</span></span>

```xpp
public void setArea(str area)
```

### <a name="parameters---setarea"></a><span data-ttu-id="d81a1-1155">パラメーター - setArea</span><span class="sxs-lookup"><span data-stu-id="d81a1-1155">Parameters - setArea</span></span>

<span data-ttu-id="d81a1-1156">エリア</span><span class="sxs-lookup"><span data-stu-id="d81a1-1156">area</span></span>  

## <a name="method-arrange"></a><span data-ttu-id="d81a1-1157">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="d81a1-1157">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-onleaving"></a><span data-ttu-id="d81a1-1158">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="d81a1-1158">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="d81a1-1159">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="d81a1-1159">Parameters - OnLeaving</span></span>

<span data-ttu-id="d81a1-1160">sender</span><span class="sxs-lookup"><span data-stu-id="d81a1-1160">sender</span></span>  

<!-- -->

<span data-ttu-id="d81a1-1161">e</span><span class="sxs-lookup"><span data-stu-id="d81a1-1161">e</span></span>  

## <a name="method-ongotfocus"></a><span data-ttu-id="d81a1-1162">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="d81a1-1162">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="d81a1-1163">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="d81a1-1163">Parameters - OnGotFocus</span></span>

<span data-ttu-id="d81a1-1164">sender</span><span class="sxs-lookup"><span data-stu-id="d81a1-1164">sender</span></span>  

<!-- -->

<span data-ttu-id="d81a1-1165">e</span><span class="sxs-lookup"><span data-stu-id="d81a1-1165">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="d81a1-1166">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="d81a1-1166">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-onenter"></a><span data-ttu-id="d81a1-1167">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="d81a1-1167">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="d81a1-1168">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="d81a1-1168">Parameters - OnEnter</span></span>

<span data-ttu-id="d81a1-1169">sender</span><span class="sxs-lookup"><span data-stu-id="d81a1-1169">sender</span></span>  

<!-- -->

<span data-ttu-id="d81a1-1170">e</span><span class="sxs-lookup"><span data-stu-id="d81a1-1170">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="d81a1-1171">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="d81a1-1171">Method inputSearch</span></span>

<span data-ttu-id="d81a1-1172">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1172">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="d81a1-1173">パラメーター - inputSerach</span><span class="sxs-lookup"><span data-stu-id="d81a1-1173">Parameters - inputSearch</span></span>

<span data-ttu-id="d81a1-1174">searchStr</span><span class="sxs-lookup"><span data-stu-id="d81a1-1174">searchStr</span></span>  
<span data-ttu-id="d81a1-1175">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1175">The string value to use to filter data; optional.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="d81a1-1176">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="d81a1-1176">Method endDrag</span></span>

<span data-ttu-id="d81a1-1177">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1177">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="d81a1-1178">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="d81a1-1178">Remarks - endDrag</span></span>

<span data-ttu-id="d81a1-1179">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1179">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="d81a1-1180">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1180">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="d81a1-1181">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="d81a1-1181">Method setFocus</span></span>

<span data-ttu-id="d81a1-1182">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1182">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-tabchanged"></a><span data-ttu-id="d81a1-1183">メソッド tabChanged</span><span class="sxs-lookup"><span data-stu-id="d81a1-1183">Method tabChanged</span></span>

<span data-ttu-id="d81a1-1184">アクティブなタブが変更されると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1184">Is called when the active tab is changed.</span></span>

```xpp
public void tabChanged(str newTab)
```

### <a name="parameters---tabchanged"></a><span data-ttu-id="d81a1-1185">パラメーター - tabChanged</span><span class="sxs-lookup"><span data-stu-id="d81a1-1185">Parameters - tabChanged</span></span>

<span data-ttu-id="d81a1-1186">newTab</span><span class="sxs-lookup"><span data-stu-id="d81a1-1186">newTab</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="d81a1-1187">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="d81a1-1187">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="d81a1-1188">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="d81a1-1188">Parameters - OnLostFocus</span></span>

<span data-ttu-id="d81a1-1189">sender</span><span class="sxs-lookup"><span data-stu-id="d81a1-1189">sender</span></span>  

<!-- -->

<span data-ttu-id="d81a1-1190">e</span><span class="sxs-lookup"><span data-stu-id="d81a1-1190">e</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="d81a1-1191">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="d81a1-1191">Method displayControl</span></span>

<span data-ttu-id="d81a1-1192">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1192">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="d81a1-1193">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="d81a1-1193">Method prefColumnSize</span></span>

<span data-ttu-id="d81a1-1194">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1194">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="d81a1-1195">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="d81a1-1195">Parameters - prefColumnSize</span></span>

<span data-ttu-id="d81a1-1196">width</span><span class="sxs-lookup"><span data-stu-id="d81a1-1196">width</span></span>  
<span data-ttu-id="d81a1-1197">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1197">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1198">height</span><span class="sxs-lookup"><span data-stu-id="d81a1-1198">height</span></span>  
<span data-ttu-id="d81a1-1199">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1199">The preferred height of the control.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="d81a1-1200">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="d81a1-1200">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="d81a1-1201">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="d81a1-1201">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="d81a1-1202">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="d81a1-1202">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="d81a1-1203">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="d81a1-1203">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="d81a1-1204">overrideObject</span><span class="sxs-lookup"><span data-stu-id="d81a1-1204">overrideObject</span></span>  

## <a name="method-cut"></a><span data-ttu-id="d81a1-1205">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="d81a1-1205">Method cut</span></span>

<span data-ttu-id="d81a1-1206">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1206">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="d81a1-1207">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="d81a1-1207">Method resetUserSetting</span></span>

<span data-ttu-id="d81a1-1208">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1208">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-ontabchanged"></a><span data-ttu-id="d81a1-1209">メソッド OnTabChanged</span><span class="sxs-lookup"><span data-stu-id="d81a1-1209">Method OnTabChanged</span></span>

```xpp
private void OnTabChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ontabchanged"></a><span data-ttu-id="d81a1-1210">パラメーター - OnTabChanged</span><span class="sxs-lookup"><span data-stu-id="d81a1-1210">Parameters - OnTabChanged</span></span>

<span data-ttu-id="d81a1-1211">sender</span><span class="sxs-lookup"><span data-stu-id="d81a1-1211">sender</span></span>  

<!-- -->

<span data-ttu-id="d81a1-1212">e</span><span class="sxs-lookup"><span data-stu-id="d81a1-1212">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="d81a1-1213">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="d81a1-1213">Method paste</span></span>

<span data-ttu-id="d81a1-1214">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1214">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-copy"></a><span data-ttu-id="d81a1-1215">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="d81a1-1215">Method copy</span></span>

<span data-ttu-id="d81a1-1216">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1216">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-dropex"></a><span data-ttu-id="d81a1-1217">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-1217">Method dropEx</span></span>

<span data-ttu-id="d81a1-1218">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1218">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="d81a1-1219">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="d81a1-1219">Parameters - dropEx</span></span>

<span data-ttu-id="d81a1-1220">dragSource</span><span class="sxs-lookup"><span data-stu-id="d81a1-1220">dragSource</span></span>  
<span data-ttu-id="d81a1-1221">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1221">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1222">dragMode</span><span class="sxs-lookup"><span data-stu-id="d81a1-1222">dragMode</span></span>  
<span data-ttu-id="d81a1-1223">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1223">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1224">x</span><span class="sxs-lookup"><span data-stu-id="d81a1-1224">x</span></span>  
<span data-ttu-id="d81a1-1225">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1225">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d81a1-1226">y</span><span class="sxs-lookup"><span data-stu-id="d81a1-1226">y</span></span>  
<span data-ttu-id="d81a1-1227">マウス位置の垂直クライアント座標を示す整数値です。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1227">An Integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-context"></a><span data-ttu-id="d81a1-1228">メソッド context</span><span class="sxs-lookup"><span data-stu-id="d81a1-1228">Method context</span></span>

<span data-ttu-id="d81a1-1229">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d81a1-1229">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enter"></a><span data-ttu-id="d81a1-1230">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="d81a1-1230">Method enter</span></span>

```xpp
public void enter()
```

