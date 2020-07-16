---
title: FormActionPaneTabControl クラス
description: このトピックでは、FormActionPaneTabControl クラスについて説明します。
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
ms.openlocfilehash: 5d52910b213dadd6b472b376df8f967bf80206da
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502664"
---
# <a name="class-formactionpanetabcontrol"></a><span data-ttu-id="926c0-103">クラス FormActionPaneTabControl</span><span class="sxs-lookup"><span data-stu-id="926c0-103">Class FormActionPaneTabControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormActionPaneTabControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="926c0-104">備考</span><span class="sxs-lookup"><span data-stu-id="926c0-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="926c0-105">例</span><span class="sxs-lookup"><span data-stu-id="926c0-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="926c0-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="926c0-106">Methods</span></span>

| <span data-ttu-id="926c0-107">方法</span><span class="sxs-lookup"><span data-stu-id="926c0-107">Method</span></span>                                                                                                              | <span data-ttu-id="926c0-108">説明</span><span class="sxs-lookup"><span data-stu-id="926c0-108">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926c0-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="926c0-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                      |
| <span data-ttu-id="926c0-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="926c0-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                      |
| <span data-ttu-id="926c0-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="926c0-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                      |
| <span data-ttu-id="926c0-112">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-112">public boolean alignChild(\[boolean value\])</span></span>                                                                        |                                                                                                                                                      |
| <span data-ttu-id="926c0-113">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-113">public boolean alignChildren(\[boolean value\])</span></span>                                                                     |                                                                                                                                                      |
| <span data-ttu-id="926c0-114">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-114">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="926c0-115">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-115">Determines whether to align the control.</span></span>                                                                                                             |
| <span data-ttu-id="926c0-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="926c0-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-117">Determines whether the user can change the contents of the control.</span></span>                                                                                  |
| <span data-ttu-id="926c0-118">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="926c0-118">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="926c0-119">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-119">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                  |
| <span data-ttu-id="926c0-120">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-120">public int allowUserSetup(\[int value\])</span></span>                                                                            |                                                                                                                                                      |
| <span data-ttu-id="926c0-121">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-121">public int arrangeGuide(\[int value\])</span></span>                                                                              |                                                                                                                                                      |
| <span data-ttu-id="926c0-122">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-122">public int arrangeMethod(\[int value\])</span></span>                                                                             |                                                                                                                                                      |
| <span data-ttu-id="926c0-123">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-123">public int arrangeWhen(\[int value\])</span></span>                                                                               |                                                                                                                                                      |
| <span data-ttu-id="926c0-124">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-124">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="926c0-125">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-125">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                   |
| <span data-ttu-id="926c0-126">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="926c0-126">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="926c0-127">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-127">Called when the user starts to drag a form control.</span></span>                                                                                                  |
| <span data-ttu-id="926c0-128">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-128">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           |                                                                                                                                                      |
| <span data-ttu-id="926c0-129">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-129">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 |                                                                                                                                                      |
| <span data-ttu-id="926c0-130">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-130">public int bottomMarginValue(\[int value\])</span></span>                                                                         |                                                                                                                                                      |
| <span data-ttu-id="926c0-131">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="926c0-131">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="926c0-132">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-132">Retrieves the size of the control.</span></span>                                                                                                                   |
| <span data-ttu-id="926c0-133">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="926c0-133">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                      |
| <span data-ttu-id="926c0-134">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="926c0-134">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                      |
| <span data-ttu-id="926c0-135">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-135">public str caption(\[str value\])</span></span>                                                                                   | <span data-ttu-id="926c0-136">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-136">Gets or set the caption of the control.</span></span>                                                                                                              |
| <span data-ttu-id="926c0-137">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-137">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                             |                                                                                                                                                      |
| <span data-ttu-id="926c0-138">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-138">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                |                                                                                                                                                      |
| <span data-ttu-id="926c0-139">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-139">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                      |
| <span data-ttu-id="926c0-140">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-140">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                      |
| <span data-ttu-id="926c0-141">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-141">public int columnspaceValue(\[int value\])</span></span>                                                                          |                                                                                                                                                      |
| <span data-ttu-id="926c0-142">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-142">public int columnsValue(\[int value\])</span></span>                                                                              |                                                                                                                                                      |
| <span data-ttu-id="926c0-143">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-143">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="926c0-144">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-144">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                  |
| <span data-ttu-id="926c0-145">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="926c0-145">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="926c0-146">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-146">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                     |
| <span data-ttu-id="926c0-147">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="926c0-147">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                      |
| <span data-ttu-id="926c0-148">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="926c0-148">public int controlCount()</span></span>                                                                                           |                                                                                                                                                      |
| <span data-ttu-id="926c0-149">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="926c0-149">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                      |
| <span data-ttu-id="926c0-150">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-150">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="926c0-151">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-151">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                       |
| <span data-ttu-id="926c0-152">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-152">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                      |
| <span data-ttu-id="926c0-153">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-153">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="926c0-154">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-154">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                        |
| <span data-ttu-id="926c0-155">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-155">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="926c0-156">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-156">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                    |
| <span data-ttu-id="926c0-157">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-157">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="926c0-158">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-158">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>    |
| <span data-ttu-id="926c0-159">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-159">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="926c0-160">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-160">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                    |
| <span data-ttu-id="926c0-161">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="926c0-161">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="926c0-162">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-162">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                       |
| <span data-ttu-id="926c0-163">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="926c0-163">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="926c0-164">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-164">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                     |
| <span data-ttu-id="926c0-165">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="926c0-165">public str dragText()</span></span>                                                                                               | <span data-ttu-id="926c0-166">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-166">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                               |
| <span data-ttu-id="926c0-167">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-167">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="926c0-168">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-168">Determines whether to enable or disable the object.</span></span>                                                                                                  |
| <span data-ttu-id="926c0-169">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="926c0-169">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="926c0-170">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-170">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                             |
| <span data-ttu-id="926c0-171">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="926c0-171">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="926c0-172">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-172">Indicates whether the control has custom user settings.</span></span>                                                                                              |
| <span data-ttu-id="926c0-173">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-173">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="926c0-174">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-174">Gets or sets the height of the control.</span></span>                                                                                                              |
| <span data-ttu-id="926c0-175">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-175">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="926c0-176">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-176">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                       |
| <span data-ttu-id="926c0-177">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-177">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="926c0-178">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-178">Gets or sets the height of the control.</span></span>                                                                                                              |
| <span data-ttu-id="926c0-179">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="926c0-179">public str helpField()</span></span>                                                                                              | <span data-ttu-id="926c0-180">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-180">Retrieves the Help text for the control.</span></span>                                                                                                             |
| <span data-ttu-id="926c0-181">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-181">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="926c0-182">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-182">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                             |
| <span data-ttu-id="926c0-183">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-183">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |                                                                                                                                                      |
| <span data-ttu-id="926c0-184">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-184">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="926c0-185">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-185">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                      |
| <span data-ttu-id="926c0-186">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="926c0-186">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="926c0-187">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-187">Retrieves the Windows handle for the control.</span></span>                                                                                                        |
| <span data-ttu-id="926c0-188">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-188">public int imageLocation(\[int value\])</span></span>                                                                             |                                                                                                                                                      |
| <span data-ttu-id="926c0-189">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="926c0-189">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                      |
| <span data-ttu-id="926c0-190">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="926c0-190">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="926c0-191">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-191">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                   |
| <span data-ttu-id="926c0-192">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="926c0-192">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="926c0-193">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-193">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                  |
| <span data-ttu-id="926c0-194">public boolean isSelected()</span><span class="sxs-lookup"><span data-stu-id="926c0-194">public boolean isSelected()</span></span>                                                                                         |                                                                                                                                                      |
| <span data-ttu-id="926c0-195">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="926c0-195">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="926c0-196">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-196">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                |
| <span data-ttu-id="926c0-197">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-197">public str keyTip(\[str value\])</span></span>                                                                                    |                                                                                                                                                      |
| <span data-ttu-id="926c0-198">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="926c0-198">public boolean leave()</span></span>                                                                                              |                                                                                                                                                      |
| <span data-ttu-id="926c0-199">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-199">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="926c0-200">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-200">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                     |
| <span data-ttu-id="926c0-201">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-201">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             |                                                                                                                                                      |
| <span data-ttu-id="926c0-202">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-202">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   |                                                                                                                                                      |
| <span data-ttu-id="926c0-203">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-203">public int leftMarginValue(\[int value\])</span></span>                                                                           |                                                                                                                                                      |
| <span data-ttu-id="926c0-204">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-204">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="926c0-205">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-205">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="926c0-206">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-206">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="926c0-207">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-207">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                     |
| <span data-ttu-id="926c0-208">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-208">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="926c0-209">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="926c0-209">Marks or unmarks the control as a user-added control.</span></span>                                                                                                |
| <span data-ttu-id="926c0-210">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="926c0-210">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="926c0-211">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-211">Is called when the control is double-clicked by the user.</span></span>                                                                                            |
| <span data-ttu-id="926c0-212">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="926c0-212">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="926c0-213">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-213">Is called when the user clicks the mouse button over the control.</span></span>                                                                                    |
| <span data-ttu-id="926c0-214">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="926c0-214">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="926c0-215">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-215">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                    |
| <span data-ttu-id="926c0-216">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="926c0-216">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="926c0-217">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-217">Is called when the user releases the mouse button over the control area.</span></span>                                                                             |
| <span data-ttu-id="926c0-218">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="926c0-218">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                      |
| <span data-ttu-id="926c0-219">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-219">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="926c0-220">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-220">Gets or sets the name used in code to identify a form, report, table, query, or another application object.</span></span>                    |
| <span data-ttu-id="926c0-221">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-221">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                      |
| <span data-ttu-id="926c0-222">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-222">public str normalImage(\[str value\])</span></span>                                                                               |                                                                                                                                                      |
| <span data-ttu-id="926c0-223">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-223">public int normalResource(\[int value\])</span></span>                                                                            |                                                                                                                                                      |
| <span data-ttu-id="926c0-224">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="926c0-224">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                      |
| <span data-ttu-id="926c0-225">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="926c0-225">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="926c0-226">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-226">Retrieves the parent control for the control.</span></span>                                                                                                        |
| <span data-ttu-id="926c0-227">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-227">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                      |
| <span data-ttu-id="926c0-228">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-228">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                      |
| <span data-ttu-id="926c0-229">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-229">public int rightMarginValue(\[int value\])</span></span>                                                                          |                                                                                                                                                      |
| <span data-ttu-id="926c0-230">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-230">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="926c0-231">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-231">Sets or returns the ID of the security key for the control.</span></span>                                                                                          |
| <span data-ttu-id="926c0-232">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="926c0-232">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="926c0-233">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-233">Shows the shortcut menu for the control.</span></span>                                                                                                             |
| <span data-ttu-id="926c0-234">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-234">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="926c0-235">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-235">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                      |
| <span data-ttu-id="926c0-236">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="926c0-236">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                      |
| <span data-ttu-id="926c0-237">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="926c0-237">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="926c0-238">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-238">Retrieves the tooltip text for the control.</span></span>                                                                                                          |
| <span data-ttu-id="926c0-239">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-239">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="926c0-240">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-240">Gets or sets the vertical position of the control in the form.</span></span>                                                                                       |
| <span data-ttu-id="926c0-241">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-241">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              |                                                                                                                                                      |
| <span data-ttu-id="926c0-242">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-242">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    |                                                                                                                                                      |
| <span data-ttu-id="926c0-243">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-243">public int topMarginValue(\[int value\])</span></span>                                                                            |                                                                                                                                                      |
| <span data-ttu-id="926c0-244">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-244">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="926c0-245">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-245">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                          |
| <span data-ttu-id="926c0-246">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-246">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="926c0-247">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-247">Gets or sets the vertical position of the control in the form.</span></span>                                                                                       |
| <span data-ttu-id="926c0-248">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-248">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                      |
| <span data-ttu-id="926c0-249">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="926c0-249">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                      |
| <span data-ttu-id="926c0-250">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-250">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="926c0-251">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-251">Gets or sets the user data for the control.</span></span>                                                                                                          |
| <span data-ttu-id="926c0-252">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-252">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="926c0-253">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-253">Gets or sets the user data item for the control.</span></span>                                                                                                     |
| <span data-ttu-id="926c0-254">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-254">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="926c0-255">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-255">Gets or sets the number of user data items for the control.</span></span>                                                                                          |
| <span data-ttu-id="926c0-256">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-256">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="926c0-257">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-257">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                  |
| <span data-ttu-id="926c0-258">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-258">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="926c0-259">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-259">Gets or sets the custom user height for the control.</span></span>                                                                                                 |
| <span data-ttu-id="926c0-260">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-260">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="926c0-261">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-261">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                   |
| <span data-ttu-id="926c0-262">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-262">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="926c0-263">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-263">Gets or sets the organization container for the control.</span></span>                                                                                             |
| <span data-ttu-id="926c0-264">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-264">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="926c0-265">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-265">Gets or sets the organization sibling for the control.</span></span>                                                                                               |
| <span data-ttu-id="926c0-266">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-266">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="926c0-267">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-267">Gets or sets the user label text for the control.</span></span>                                                                                                    |
| <span data-ttu-id="926c0-268">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-268">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="926c0-269">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-269">Gets or sets the user security level for the control.</span></span>                                                                                                |
| <span data-ttu-id="926c0-270">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-270">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="926c0-271">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-271">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span> |
| <span data-ttu-id="926c0-272">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-272">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="926c0-273">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-273">Sets or returns the width of the control in pixels.</span></span>                                                                                                  |
| <span data-ttu-id="926c0-274">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-274">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                      |
| <span data-ttu-id="926c0-275">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-275">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="926c0-276">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-276">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="926c0-277">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-277">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="926c0-278">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-278">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                          |
| <span data-ttu-id="926c0-279">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-279">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="926c0-280">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-280">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                        |
| <span data-ttu-id="926c0-281">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-281">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="926c0-282">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-282">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                               |
| <span data-ttu-id="926c0-283">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="926c0-283">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="926c0-284">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-284">Gets or sets the width of the control.</span></span>                                                                                                               |
| <span data-ttu-id="926c0-285">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-285">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="926c0-286">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-286">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                       |
| <span data-ttu-id="926c0-287">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="926c0-287">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="926c0-288">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-288">Gets or sets the width of the control.</span></span>                                                                                                               |
| <span data-ttu-id="926c0-289">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="926c0-289">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                      |
| <span data-ttu-id="926c0-290">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="926c0-290">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="926c0-291">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-291">Sets the focus on the control.</span></span>                                                                                                                       |
| <span data-ttu-id="926c0-292">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="926c0-292">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="926c0-293">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="926c0-293">Resets the user settings for the control.</span></span>                                                                                                            |
| <span data-ttu-id="926c0-294">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="926c0-294">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="926c0-295">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-295">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                   |
| <span data-ttu-id="926c0-296">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="926c0-296">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="926c0-297">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-297">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                               |
| <span data-ttu-id="926c0-298">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="926c0-298">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="926c0-299">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-299">Indicates that the control has received focus.</span></span>                                                                                                       |
| <span data-ttu-id="926c0-300">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="926c0-300">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                      |
| <span data-ttu-id="926c0-301">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="926c0-301">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="926c0-302">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-302">Specifies the preferred column width and height for the form control.</span></span>                                                                                |
| <span data-ttu-id="926c0-303">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="926c0-303">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="926c0-304">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-304">Is called when the user has finished dragging a form control.</span></span>                                                                                        |
| <span data-ttu-id="926c0-305">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="926c0-305">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="926c0-306">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-306">Indicates that the mouse pointer has left the control.</span></span>                                                                                               |
| <span data-ttu-id="926c0-307">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="926c0-307">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="926c0-308">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="926c0-308">Performs data filtering for the control, based on the specified string.</span></span>                                                                              |
| <span data-ttu-id="926c0-309">public void enter()</span><span class="sxs-lookup"><span data-stu-id="926c0-309">public void enter()</span></span>                                                                                                 |                                                                                                                                                      |
| <span data-ttu-id="926c0-310">public void context()</span><span class="sxs-lookup"><span data-stu-id="926c0-310">public void context()</span></span>                                                                                               | <span data-ttu-id="926c0-311">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-311">Shows the shortcut menu for the control.</span></span>                                                                                                             |
| <span data-ttu-id="926c0-312">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="926c0-312">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="926c0-313">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-313">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                 |
| <span data-ttu-id="926c0-314">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="926c0-314">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                      |
| <span data-ttu-id="926c0-315">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="926c0-315">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                      |
| <span data-ttu-id="926c0-316">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="926c0-316">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                      |
| <span data-ttu-id="926c0-317">public void cut()</span><span class="sxs-lookup"><span data-stu-id="926c0-317">public void cut()</span></span>                                                                                                   | <span data-ttu-id="926c0-318">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="926c0-318">Cuts the contents of the control.</span></span>                                                                                                                    |
| <span data-ttu-id="926c0-319">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="926c0-319">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="926c0-320">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-320">Indicates that the control has lost focus.</span></span>                                                                                                           |
| <span data-ttu-id="926c0-321">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="926c0-321">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                      |
| <span data-ttu-id="926c0-322">public void copy()</span><span class="sxs-lookup"><span data-stu-id="926c0-322">public void copy()</span></span>                                                                                                  | <span data-ttu-id="926c0-323">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="926c0-323">Copies the contents of the control to the clipboard.</span></span>                                                                                                 |
| <span data-ttu-id="926c0-324">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="926c0-324">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="926c0-325">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-325">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                     |
| <span data-ttu-id="926c0-326">public void selectionChanged()</span><span class="sxs-lookup"><span data-stu-id="926c0-326">public void selectionChanged()</span></span>                                                                                      |                                                                                                                                                      |
| <span data-ttu-id="926c0-327">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="926c0-327">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="926c0-328">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-328">Displays the control.</span></span>                                                                                                                                |
| <span data-ttu-id="926c0-329">public void paste()</span><span class="sxs-lookup"><span data-stu-id="926c0-329">public void paste()</span></span>                                                                                                 | <span data-ttu-id="926c0-330">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="926c0-330">Pastes the contents of the clipboard into the control.</span></span>                                                                                               |
| <span data-ttu-id="926c0-331">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="926c0-331">public void arrange()</span></span>                                                                                               |                                                                                                                                                      |
| <span data-ttu-id="926c0-332">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="926c0-332">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                      |
| <span data-ttu-id="926c0-333">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="926c0-333">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                      |

## <a name="method-addcontrol"></a><span data-ttu-id="926c0-334">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="926c0-334">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="926c0-335">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="926c0-335">Parameters - addControl</span></span>

<span data-ttu-id="926c0-336">controlType</span><span class="sxs-lookup"><span data-stu-id="926c0-336">controlType</span></span>  

<!-- -->

<span data-ttu-id="926c0-337">controlName</span><span class="sxs-lookup"><span data-stu-id="926c0-337">controlName</span></span>  

<!-- -->

<span data-ttu-id="926c0-338">insertAfter</span><span class="sxs-lookup"><span data-stu-id="926c0-338">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="926c0-339">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="926c0-339">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="926c0-340">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="926c0-340">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="926c0-341">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="926c0-341">Parameters - addControlEx</span></span>

<span data-ttu-id="926c0-342">controlClass</span><span class="sxs-lookup"><span data-stu-id="926c0-342">controlClass</span></span>  

<!-- -->

<span data-ttu-id="926c0-343">controlName</span><span class="sxs-lookup"><span data-stu-id="926c0-343">controlName</span></span>  

<!-- -->

<span data-ttu-id="926c0-344">insertAfter</span><span class="sxs-lookup"><span data-stu-id="926c0-344">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="926c0-345">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="926c0-345">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="926c0-346">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="926c0-346">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="926c0-347">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="926c0-347">Parameters - addDataField</span></span>

<span data-ttu-id="926c0-348">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="926c0-348">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="926c0-349">fieldId</span><span class="sxs-lookup"><span data-stu-id="926c0-349">fieldId</span></span>  

<!-- -->

<span data-ttu-id="926c0-350">insertAfter</span><span class="sxs-lookup"><span data-stu-id="926c0-350">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="926c0-351">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="926c0-351">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="926c0-352">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="926c0-352">Return Value - addDataField</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="926c0-353">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="926c0-353">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="926c0-354">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="926c0-354">Parameters - alignChild</span></span>

<span data-ttu-id="926c0-355">値</span><span class="sxs-lookup"><span data-stu-id="926c0-355">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="926c0-356">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="926c0-356">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="926c0-357">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="926c0-357">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="926c0-358">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="926c0-358">Parameters - alignChildren</span></span>

<span data-ttu-id="926c0-359">値</span><span class="sxs-lookup"><span data-stu-id="926c0-359">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="926c0-360">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="926c0-360">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="926c0-361">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="926c0-361">Method alignControl</span></span>

<span data-ttu-id="926c0-362">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-362">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="926c0-363">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="926c0-363">Parameters - alignControl</span></span>

<span data-ttu-id="926c0-364">値</span><span class="sxs-lookup"><span data-stu-id="926c0-364">value</span></span>  
<span data-ttu-id="926c0-365">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-365">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="926c0-366">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="926c0-366">Return Value - alignControl</span></span>

<span data-ttu-id="926c0-367">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="926c0-367">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="926c0-368">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="926c0-368">Remarks - alignControl</span></span>

<span data-ttu-id="926c0-369">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-369">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="926c0-370">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="926c0-370">Method allowEdit</span></span>

<span data-ttu-id="926c0-371">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-371">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="926c0-372">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="926c0-372">Parameters - allowEdit</span></span>

<span data-ttu-id="926c0-373">値</span><span class="sxs-lookup"><span data-stu-id="926c0-373">value</span></span>  
<span data-ttu-id="926c0-374">allowEdit プロパティに割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="926c0-374">The value to be assigned to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="926c0-375">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="926c0-375">Return Value - allowEdit</span></span>

<span data-ttu-id="926c0-376">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-376">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="926c0-377">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="926c0-377">Remarks - allowEdit</span></span>

<span data-ttu-id="926c0-378">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="926c0-378">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="926c0-379">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="926c0-379">Method allowSysSetup</span></span>

<span data-ttu-id="926c0-380">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-380">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="926c0-381">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="926c0-381">Return Value - allowSysSetup</span></span>

<span data-ttu-id="926c0-382">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-382">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="926c0-383">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="926c0-383">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="926c0-384">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="926c0-384">Parameters - allowUserSetup</span></span>

<span data-ttu-id="926c0-385">値</span><span class="sxs-lookup"><span data-stu-id="926c0-385">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="926c0-386">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="926c0-386">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="926c0-387">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="926c0-387">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="926c0-388">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="926c0-388">Parameters - arrangeGuide</span></span>

<span data-ttu-id="926c0-389">値</span><span class="sxs-lookup"><span data-stu-id="926c0-389">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="926c0-390">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="926c0-390">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="926c0-391">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="926c0-391">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="926c0-392">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="926c0-392">Parameters - arrangeMethod</span></span>

<span data-ttu-id="926c0-393">値</span><span class="sxs-lookup"><span data-stu-id="926c0-393">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="926c0-394">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="926c0-394">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="926c0-395">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="926c0-395">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="926c0-396">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="926c0-396">Parameters - arrangeWhen</span></span>

<span data-ttu-id="926c0-397">値</span><span class="sxs-lookup"><span data-stu-id="926c0-397">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="926c0-398">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="926c0-398">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="926c0-399">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="926c0-399">Method autoDeclaration</span></span>

<span data-ttu-id="926c0-400">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-400">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="926c0-401">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="926c0-401">Parameters - autoDeclaration</span></span>

<span data-ttu-id="926c0-402">値</span><span class="sxs-lookup"><span data-stu-id="926c0-402">value</span></span>  
<span data-ttu-id="926c0-403">指定されている場合、プロパティはこの値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-403">The property is set to this value, if supplied.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="926c0-404">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="926c0-404">Return Value - autoDeclaration</span></span>

<span data-ttu-id="926c0-405">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-405">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="926c0-406">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="926c0-406">Remarks - autoDeclaration</span></span>

<span data-ttu-id="926c0-407">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="926c0-407">Controls cannot have identical names.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="926c0-408">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="926c0-408">Method beginDrag</span></span>

<span data-ttu-id="926c0-409">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-409">Called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="926c0-410">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="926c0-410">Parameters - beginDrag</span></span>

<span data-ttu-id="926c0-411">x</span><span class="sxs-lookup"><span data-stu-id="926c0-411">x</span></span>  
<span data-ttu-id="926c0-412">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-412">An integer value that indicates the y-coordinate of the mouse pointer.</span></span>

<!-- -->

<span data-ttu-id="926c0-413">y</span><span class="sxs-lookup"><span data-stu-id="926c0-413">y</span></span>  
<span data-ttu-id="926c0-414">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-414">An integer value that indicates the y-coordinate of the mouse pointer.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="926c0-415">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="926c0-415">Return Value - beginDrag</span></span>

<span data-ttu-id="926c0-416">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="926c0-416">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="926c0-417">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="926c0-417">Remarks - beginDrag</span></span>

<span data-ttu-id="926c0-418">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="926c0-418">This event will not be raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="926c0-419">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="926c0-419">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="926c0-420">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-420">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="926c0-421">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-421">Parameters - bottomMargin</span></span>

<span data-ttu-id="926c0-422">値</span><span class="sxs-lookup"><span data-stu-id="926c0-422">value</span></span>  

<!-- -->

<span data-ttu-id="926c0-423">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-423">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="926c0-424">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-424">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="926c0-425">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-425">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="926c0-426">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-426">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="926c0-427">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-427">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="926c0-428">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-428">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="926c0-429">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-429">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="926c0-430">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-430">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="926c0-431">値</span><span class="sxs-lookup"><span data-stu-id="926c0-431">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="926c0-432">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-432">Return Value - bottomMarginValue</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="926c0-433">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="926c0-433">Method calcControlSize</span></span>

<span data-ttu-id="926c0-434">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-434">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="926c0-435">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="926c0-435">Parameters - calcControlSize</span></span>

<span data-ttu-id="926c0-436">chars</span><span class="sxs-lookup"><span data-stu-id="926c0-436">chars</span></span>  
<span data-ttu-id="926c0-437">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="926c0-437">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="926c0-438">明細行</span><span class="sxs-lookup"><span data-stu-id="926c0-438">lines</span></span>  
<span data-ttu-id="926c0-439">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="926c0-439">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="926c0-440">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="926c0-440">Return Value - calcControlSize</span></span>

<span data-ttu-id="926c0-441">幅と高さのあるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="926c0-441">The container that has the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="926c0-442">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="926c0-442">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="926c0-443">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="926c0-443">Parameters - canAddDataField</span></span>

<span data-ttu-id="926c0-444">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="926c0-444">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="926c0-445">fieldId</span><span class="sxs-lookup"><span data-stu-id="926c0-445">fieldId</span></span>  

<!-- -->

<span data-ttu-id="926c0-446">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="926c0-446">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="926c0-447">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="926c0-447">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="926c0-448">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="926c0-448">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="926c0-449">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="926c0-449">Parameters - canContain</span></span>

<span data-ttu-id="926c0-450">control</span><span class="sxs-lookup"><span data-stu-id="926c0-450">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="926c0-451">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="926c0-451">Return Value - canContain</span></span>

## <a name="method-caption"></a><span data-ttu-id="926c0-452">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="926c0-452">Method caption</span></span>

<span data-ttu-id="926c0-453">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-453">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="926c0-454">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="926c0-454">Parameters - caption</span></span>

<span data-ttu-id="926c0-455">値</span><span class="sxs-lookup"><span data-stu-id="926c0-455">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="926c0-456">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="926c0-456">Return Value - caption</span></span>

<span data-ttu-id="926c0-457">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="926c0-457">The string that is used as the caption of the control.</span></span>

## <a name="method-columns"></a><span data-ttu-id="926c0-458">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="926c0-458">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="926c0-459">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="926c0-459">Parameters - columns</span></span>

<span data-ttu-id="926c0-460">値</span><span class="sxs-lookup"><span data-stu-id="926c0-460">value</span></span>  

<!-- -->

<span data-ttu-id="926c0-461">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-461">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="926c0-462">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="926c0-462">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="926c0-463">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="926c0-463">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="926c0-464">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="926c0-464">Parameters - columnsMode</span></span>

<span data-ttu-id="926c0-465">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-465">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="926c0-466">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="926c0-466">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="926c0-467">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="926c0-467">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="926c0-468">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="926c0-468">Parameters - columnspace</span></span>

<span data-ttu-id="926c0-469">値</span><span class="sxs-lookup"><span data-stu-id="926c0-469">value</span></span>  

<!-- -->

<span data-ttu-id="926c0-470">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-470">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="926c0-471">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="926c0-471">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="926c0-472">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="926c0-472">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="926c0-473">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="926c0-473">Parameters - columnspaceMode</span></span>

<span data-ttu-id="926c0-474">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-474">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="926c0-475">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="926c0-475">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="926c0-476">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="926c0-476">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="926c0-477">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="926c0-477">Parameters - columnspaceValue</span></span>

<span data-ttu-id="926c0-478">値</span><span class="sxs-lookup"><span data-stu-id="926c0-478">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="926c0-479">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="926c0-479">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="926c0-480">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="926c0-480">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="926c0-481">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="926c0-481">Parameters - columnsValue</span></span>

<span data-ttu-id="926c0-482">値</span><span class="sxs-lookup"><span data-stu-id="926c0-482">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="926c0-483">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="926c0-483">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="926c0-484">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="926c0-484">Method configurationKey</span></span>

<span data-ttu-id="926c0-485">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-485">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="926c0-486">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="926c0-486">Parameters - configurationKey</span></span>

<span data-ttu-id="926c0-487">値</span><span class="sxs-lookup"><span data-stu-id="926c0-487">value</span></span>  
<span data-ttu-id="926c0-488">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-488">The ID of the configuration key being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="926c0-489">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="926c0-489">Return Value - configurationKey</span></span>

<span data-ttu-id="926c0-490">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="926c0-490">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="926c0-491">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="926c0-491">Remarks - configurationKey</span></span>

<span data-ttu-id="926c0-492">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-492">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="926c0-493">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="926c0-493">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="926c0-494">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="926c0-494">Method configurationKeyEx</span></span>

<span data-ttu-id="926c0-495">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-495">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="926c0-496">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="926c0-496">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="926c0-497">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="926c0-497">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="926c0-498">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="926c0-498">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="926c0-499">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="926c0-499">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="926c0-500">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="926c0-500">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="926c0-501">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="926c0-501">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-contains"></a><span data-ttu-id="926c0-502">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="926c0-502">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="926c0-503">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="926c0-503">Parameters - contains</span></span>

<span data-ttu-id="926c0-504">control</span><span class="sxs-lookup"><span data-stu-id="926c0-504">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="926c0-505">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="926c0-505">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="926c0-506">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="926c0-506">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="926c0-507">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="926c0-507">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="926c0-508">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="926c0-508">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="926c0-509">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="926c0-509">Parameters - controlNum</span></span>

<span data-ttu-id="926c0-510">controlNo</span><span class="sxs-lookup"><span data-stu-id="926c0-510">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="926c0-511">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="926c0-511">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="926c0-512">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="926c0-512">Method countryRegionCodes</span></span>

<span data-ttu-id="926c0-513">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-513">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="926c0-514">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="926c0-514">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="926c0-515">値</span><span class="sxs-lookup"><span data-stu-id="926c0-515">value</span></span>  
<span data-ttu-id="926c0-516">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-516">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="926c0-517">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="926c0-517">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="926c0-518">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="926c0-518">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="926c0-519">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="926c0-519">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="926c0-520">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="926c0-520">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="926c0-521">値</span><span class="sxs-lookup"><span data-stu-id="926c0-521">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="926c0-522">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="926c0-522">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="926c0-523">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="926c0-523">Method dataRelationPath</span></span>

<span data-ttu-id="926c0-524">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-524">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="926c0-525">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="926c0-525">Parameters - dataRelationPath</span></span>

<span data-ttu-id="926c0-526">値</span><span class="sxs-lookup"><span data-stu-id="926c0-526">value</span></span>  
<span data-ttu-id="926c0-527">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-527">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="926c0-528">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="926c0-528">Return Value - dataRelationPath</span></span>

<span data-ttu-id="926c0-529">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="926c0-529">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="926c0-530">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="926c0-530">Remarks - dataRelationPath</span></span>

<span data-ttu-id="926c0-531">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="926c0-531">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="926c0-532">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="926c0-532">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="926c0-533">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="926c0-533">Method dataSource</span></span>

<span data-ttu-id="926c0-534">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-534">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="926c0-535">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="926c0-535">Parameters - dataSource</span></span>

<span data-ttu-id="926c0-536">値</span><span class="sxs-lookup"><span data-stu-id="926c0-536">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="926c0-537">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="926c0-537">Return Value - dataSource</span></span>

<span data-ttu-id="926c0-538">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="926c0-538">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="926c0-539">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="926c0-539">Method displayTarget</span></span>

<span data-ttu-id="926c0-540">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-540">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="926c0-541">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="926c0-541">Parameters - displayTarget</span></span>

<span data-ttu-id="926c0-542">値</span><span class="sxs-lookup"><span data-stu-id="926c0-542">value</span></span>  
<span data-ttu-id="926c0-543">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-543">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="926c0-544">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="926c0-544">Return Value - displayTarget</span></span>

<span data-ttu-id="926c0-545">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="926c0-545">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="926c0-546">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="926c0-546">Method dragDrop</span></span>

<span data-ttu-id="926c0-547">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-547">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="926c0-548">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="926c0-548">Parameters - dragDrop</span></span>

<span data-ttu-id="926c0-549">値</span><span class="sxs-lookup"><span data-stu-id="926c0-549">value</span></span>  
<span data-ttu-id="926c0-550">ドラッグ アンド ドロップの動作が有効かどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-550">An Integer data type that indicates whether the drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="926c0-551">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="926c0-551">Return Value - dragDrop</span></span>

<span data-ttu-id="926c0-552">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="926c0-552">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="926c0-553">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="926c0-553">Remarks - dragDrop</span></span>

<span data-ttu-id="926c0-554">FormControl::dragLeave、FormControl::dragOver、および FormControl::dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-554">Use the FormControl::dragLeave, FormControl::dragOver, and FormControl::dragOverEx methods to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="926c0-555">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="926c0-555">Method dragOver</span></span>

<span data-ttu-id="926c0-556">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-556">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="926c0-557">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="926c0-557">Parameters - dragOver</span></span>

<span data-ttu-id="926c0-558">dragSource</span><span class="sxs-lookup"><span data-stu-id="926c0-558">dragSource</span></span>  
<span data-ttu-id="926c0-559">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-559">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-560">dragMode</span><span class="sxs-lookup"><span data-stu-id="926c0-560">dragMode</span></span>  
<span data-ttu-id="926c0-561">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-561">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-562">x</span><span class="sxs-lookup"><span data-stu-id="926c0-562">x</span></span>  
<span data-ttu-id="926c0-563">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-563">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-564">y</span><span class="sxs-lookup"><span data-stu-id="926c0-564">y</span></span>  
<span data-ttu-id="926c0-565">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-565">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="926c0-566">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="926c0-566">Return Value - dragOver</span></span>

<span data-ttu-id="926c0-567">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="926c0-567">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="926c0-568">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="926c0-568">Method dragOverEx</span></span>

<span data-ttu-id="926c0-569">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-569">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="926c0-570">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="926c0-570">Parameters - dragOverEx</span></span>

<span data-ttu-id="926c0-571">dragSource</span><span class="sxs-lookup"><span data-stu-id="926c0-571">dragSource</span></span>  
<span data-ttu-id="926c0-572">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-572">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-573">dragMode</span><span class="sxs-lookup"><span data-stu-id="926c0-573">dragMode</span></span>  
<span data-ttu-id="926c0-574">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-574">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-575">x</span><span class="sxs-lookup"><span data-stu-id="926c0-575">x</span></span>  
<span data-ttu-id="926c0-576">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-576">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-577">y</span><span class="sxs-lookup"><span data-stu-id="926c0-577">y</span></span>  
<span data-ttu-id="926c0-578">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-578">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="926c0-579">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="926c0-579">Return Value - dragOverEx</span></span>

<span data-ttu-id="926c0-580">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="926c0-580">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="926c0-581">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="926c0-581">Method dragText</span></span>

<span data-ttu-id="926c0-582">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-582">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="926c0-583">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="926c0-583">Return Value - dragText</span></span>

<span data-ttu-id="926c0-584">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="926c0-584">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="926c0-585">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="926c0-585">Method enabled</span></span>

<span data-ttu-id="926c0-586">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-586">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="926c0-587">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="926c0-587">Parameters - enabled</span></span>

<span data-ttu-id="926c0-588">値</span><span class="sxs-lookup"><span data-stu-id="926c0-588">value</span></span>  
<span data-ttu-id="926c0-589">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-589">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="926c0-590">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="926c0-590">Return Value - enabled</span></span>

<span data-ttu-id="926c0-591">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-591">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="926c0-592">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="926c0-592">Remarks - enabled</span></span>

<span data-ttu-id="926c0-593">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="926c0-593">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="926c0-594">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="926c0-594">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="926c0-595">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="926c0-595">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="926c0-596">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="926c0-596">Method hasChanged</span></span>

<span data-ttu-id="926c0-597">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-597">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="926c0-598">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="926c0-598">Parameters - hasChanged</span></span>

<span data-ttu-id="926c0-599">val</span><span class="sxs-lookup"><span data-stu-id="926c0-599">val</span></span>  
<span data-ttu-id="926c0-600">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-600">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="926c0-601">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="926c0-601">Return Value - hasChanged</span></span>

<span data-ttu-id="926c0-602">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-602">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="926c0-603">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="926c0-603">Method hasUserSetting</span></span>

<span data-ttu-id="926c0-604">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-604">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="926c0-605">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="926c0-605">Return Value - hasUserSetting</span></span>

<span data-ttu-id="926c0-606">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-606">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="926c0-607">メソッド height</span><span class="sxs-lookup"><span data-stu-id="926c0-607">Method height</span></span>

<span data-ttu-id="926c0-608">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-608">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="926c0-609">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="926c0-609">Parameters - height</span></span>

<span data-ttu-id="926c0-610">値</span><span class="sxs-lookup"><span data-stu-id="926c0-610">value</span></span>  
<span data-ttu-id="926c0-611">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="926c0-611">An Integer data type that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="926c0-612">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-612">mode</span></span>  
<span data-ttu-id="926c0-613">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="926c0-613">An Integer data type that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="926c0-614">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="926c0-614">Return Value - height</span></span>

<span data-ttu-id="926c0-615">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="926c0-615">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="926c0-616">備考 - height</span><span class="sxs-lookup"><span data-stu-id="926c0-616">Remarks - height</span></span>

<span data-ttu-id="926c0-617">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-617">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="926c0-618">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="926c0-618">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="926c0-619">モード。</span><span class="sxs-lookup"><span data-stu-id="926c0-619">Mode.</span></span>            | <span data-ttu-id="926c0-620">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="926c0-620">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="926c0-621">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="926c0-621">-1 Exact.</span></span>        | <span data-ttu-id="926c0-622">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-622">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="926c0-623">0 自動。</span><span class="sxs-lookup"><span data-stu-id="926c0-623">0 Auto.</span></span>          | <span data-ttu-id="926c0-624">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-624">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="926c0-625">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="926c0-625">1 Column height.</span></span> | <span data-ttu-id="926c0-626">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="926c0-626">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="926c0-627">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="926c0-627">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="926c0-628">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="926c0-628">Method heightMode</span></span>

<span data-ttu-id="926c0-629">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-629">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="926c0-630">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="926c0-630">Parameters - heightMode</span></span>

<span data-ttu-id="926c0-631">値</span><span class="sxs-lookup"><span data-stu-id="926c0-631">value</span></span>  
<span data-ttu-id="926c0-632">コントロールの高さの計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-632">An Integer data type value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="926c0-633">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="926c0-633">Return Value - heightMode</span></span>

<span data-ttu-id="926c0-634">計算モード。</span><span class="sxs-lookup"><span data-stu-id="926c0-634">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="926c0-635">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="926c0-635">Remarks - heightMode</span></span>

<span data-ttu-id="926c0-636">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="926c0-636">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="926c0-637">モード。</span><span class="sxs-lookup"><span data-stu-id="926c0-637">Mode.</span></span>          | <span data-ttu-id="926c0-638">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="926c0-638">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="926c0-639">正確。</span><span class="sxs-lookup"><span data-stu-id="926c0-639">Exact.</span></span>         | <span data-ttu-id="926c0-640">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-640">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="926c0-641">自動。</span><span class="sxs-lookup"><span data-stu-id="926c0-641">Auto.</span></span>          | <span data-ttu-id="926c0-642">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-642">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="926c0-643">列の高さ</span><span class="sxs-lookup"><span data-stu-id="926c0-643">Column height.</span></span> | <span data-ttu-id="926c0-644">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="926c0-644">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="926c0-645">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="926c0-645">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="926c0-646">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="926c0-646">Method heightValue</span></span>

<span data-ttu-id="926c0-647">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-647">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="926c0-648">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="926c0-648">Parameters - heightValue</span></span>

<span data-ttu-id="926c0-649">値</span><span class="sxs-lookup"><span data-stu-id="926c0-649">value</span></span>  
<span data-ttu-id="926c0-650">高さをピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-650">An Integer data type that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="926c0-651">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="926c0-651">Return Value - heightValue</span></span>

<span data-ttu-id="926c0-652">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="926c0-652">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="926c0-653">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="926c0-653">Remarks - heightValue</span></span>

<span data-ttu-id="926c0-654">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="926c0-654">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="926c0-655">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="926c0-655">Method helpField</span></span>

<span data-ttu-id="926c0-656">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-656">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="926c0-657">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="926c0-657">Return Value - helpField</span></span>

<span data-ttu-id="926c0-658">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="926c0-658">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="926c0-659">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="926c0-659">Remarks - helpField</span></span>

<span data-ttu-id="926c0-660">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="926c0-660">The helpField method cannot be used to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="926c0-661">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="926c0-661">Method helpText</span></span>

<span data-ttu-id="926c0-662">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-662">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="926c0-663">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="926c0-663">Parameters - helpText</span></span>

<span data-ttu-id="926c0-664">値</span><span class="sxs-lookup"><span data-stu-id="926c0-664">value</span></span>  
<span data-ttu-id="926c0-665">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="926c0-665">The value that is assigned as the help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="926c0-666">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="926c0-666">Return Value - helpText</span></span>

<span data-ttu-id="926c0-667">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="926c0-667">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="926c0-668">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="926c0-668">Remarks - helpText</span></span>

<span data-ttu-id="926c0-669">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-669">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="926c0-670">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="926c0-670">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="926c0-671">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="926c0-671">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="926c0-672">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="926c0-672">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="926c0-673">値</span><span class="sxs-lookup"><span data-stu-id="926c0-673">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="926c0-674">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="926c0-674">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="926c0-675">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="926c0-675">Method hierarchyParent</span></span>

<span data-ttu-id="926c0-676">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-676">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="926c0-677">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="926c0-677">Parameters - hierarchyParent</span></span>

<span data-ttu-id="926c0-678">値</span><span class="sxs-lookup"><span data-stu-id="926c0-678">value</span></span>  
<span data-ttu-id="926c0-679">コントロールの HierarchyParent 値として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="926c0-679">The value to assign as the HierarchyParent value of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="926c0-680">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="926c0-680">Return Value - hierarchyParent</span></span>

<span data-ttu-id="926c0-681">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="926c0-681">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="926c0-682">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="926c0-682">Method hWnd</span></span>

<span data-ttu-id="926c0-683">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-683">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="926c0-684">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="926c0-684">Return Value - hWnd</span></span>

<span data-ttu-id="926c0-685">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="926c0-685">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="926c0-686">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="926c0-686">Remarks - hWnd</span></span>

<span data-ttu-id="926c0-687">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="926c0-687">The handle can be used with the Windows API.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="926c0-688">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="926c0-688">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="926c0-689">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="926c0-689">Parameters - imageLocation</span></span>

<span data-ttu-id="926c0-690">値</span><span class="sxs-lookup"><span data-stu-id="926c0-690">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="926c0-691">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="926c0-691">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="926c0-692">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="926c0-692">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="926c0-693">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="926c0-693">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="926c0-694">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="926c0-694">Method isDisplayed</span></span>

<span data-ttu-id="926c0-695">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-695">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="926c0-696">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="926c0-696">Return Value - isDisplayed</span></span>

<span data-ttu-id="926c0-697">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="926c0-697">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="926c0-698">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="926c0-698">Remarks - isDisplayed</span></span>

<span data-ttu-id="926c0-699">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="926c0-699">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="926c0-700">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="926c0-700">Method isRestricted</span></span>

<span data-ttu-id="926c0-701">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-701">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="926c0-702">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="926c0-702">Return Value - isRestricted</span></span>

<span data-ttu-id="926c0-703">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="926c0-703">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isselected"></a><span data-ttu-id="926c0-704">メソッド isSelected</span><span class="sxs-lookup"><span data-stu-id="926c0-704">Method isSelected</span></span>

```xpp
public boolean isSelected()
```

### <a name="return-value---isselected"></a><span data-ttu-id="926c0-705">戻り値 - isSelected</span><span class="sxs-lookup"><span data-stu-id="926c0-705">Return Value - isSelected</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="926c0-706">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="926c0-706">Method isUserSetupEnabled</span></span>

<span data-ttu-id="926c0-707">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-707">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="926c0-708">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="926c0-708">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="926c0-709">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="926c0-709">neededSetupRights</span></span>  
<span data-ttu-id="926c0-710">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="926c0-710">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="926c0-711">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="926c0-711">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="926c0-712">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-712">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="926c0-713">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="926c0-713">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="926c0-714">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="926c0-714">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926c0-715">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="926c0-715">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="926c0-716">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="926c0-716">No changes can be made to the control.</span></span> <span data-ttu-id="926c0-717">neededSetupRights パラメーターにこの値を使用すると、常に、true が返ってきます。</span><span class="sxs-lookup"><span data-stu-id="926c0-717">Using this value for the neededSetupRights parameter always returns true.</span></span>                 |
| <span data-ttu-id="926c0-718">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="926c0-718">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="926c0-719">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="926c0-719">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="926c0-720">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="926c0-720">The user cannot move the control.</span></span>   |
| <span data-ttu-id="926c0-721">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="926c0-721">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="926c0-722">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="926c0-722">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="926c0-723">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="926c0-723">The user can also move the control.</span></span> |

<span data-ttu-id="926c0-724">このメソッドは、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメーターで指定されたアクセスレベルを許可している場合にのみ true を返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-724">This method returns true only if the AllowUserSetup property for the design and all parent containers allows for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-keytip"></a><span data-ttu-id="926c0-725">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="926c0-725">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="926c0-726">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="926c0-726">Parameters - keyTip</span></span>

<span data-ttu-id="926c0-727">値</span><span class="sxs-lookup"><span data-stu-id="926c0-727">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="926c0-728">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="926c0-728">Return Value - keyTip</span></span>

## <a name="method-leave"></a><span data-ttu-id="926c0-729">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="926c0-729">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="926c0-730">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="926c0-730">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="926c0-731">メソッド left</span><span class="sxs-lookup"><span data-stu-id="926c0-731">Method left</span></span>

<span data-ttu-id="926c0-732">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-732">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="926c0-733">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="926c0-733">Parameters - left</span></span>

<span data-ttu-id="926c0-734">値</span><span class="sxs-lookup"><span data-stu-id="926c0-734">value</span></span>  
<span data-ttu-id="926c0-735">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-735">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="926c0-736">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-736">mode</span></span>  
<span data-ttu-id="926c0-737">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-737">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="926c0-738">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="926c0-738">Return Value - left</span></span>

<span data-ttu-id="926c0-739">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="926c0-739">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="926c0-740">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-740">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="926c0-741">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-741">Parameters - leftMargin</span></span>

<span data-ttu-id="926c0-742">値</span><span class="sxs-lookup"><span data-stu-id="926c0-742">value</span></span>  

<!-- -->

<span data-ttu-id="926c0-743">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-743">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="926c0-744">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-744">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="926c0-745">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-745">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="926c0-746">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-746">Parameters - leftMarginMode</span></span>

<span data-ttu-id="926c0-747">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-747">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="926c0-748">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-748">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="926c0-749">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-749">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="926c0-750">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-750">Parameters - leftMarginValue</span></span>

<span data-ttu-id="926c0-751">値</span><span class="sxs-lookup"><span data-stu-id="926c0-751">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="926c0-752">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-752">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="926c0-753">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="926c0-753">Method leftMode</span></span>

<span data-ttu-id="926c0-754">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-754">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="926c0-755">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="926c0-755">Parameters - leftMode</span></span>

<span data-ttu-id="926c0-756">値</span><span class="sxs-lookup"><span data-stu-id="926c0-756">value</span></span>  
<span data-ttu-id="926c0-757">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-757">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="926c0-758">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="926c0-758">Return Value - leftMode</span></span>

<span data-ttu-id="926c0-759">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="926c0-759">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="926c0-760">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="926c0-760">Method leftValue</span></span>

<span data-ttu-id="926c0-761">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-761">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="926c0-762">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="926c0-762">Parameters - leftValue</span></span>

<span data-ttu-id="926c0-763">値</span><span class="sxs-lookup"><span data-stu-id="926c0-763">value</span></span>  
<span data-ttu-id="926c0-764">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-764">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="926c0-765">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="926c0-765">Return Value - leftValue</span></span>

<span data-ttu-id="926c0-766">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="926c0-766">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="926c0-767">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="926c0-767">Method markAsUserAdd</span></span>

<span data-ttu-id="926c0-768">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="926c0-768">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="926c0-769">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="926c0-769">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="926c0-770">値</span><span class="sxs-lookup"><span data-stu-id="926c0-770">value</span></span>  
<span data-ttu-id="926c0-771">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-771">A Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="926c0-772">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="926c0-772">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="926c0-773">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-773">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="926c0-774">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="926c0-774">Method mouseDblClick</span></span>

<span data-ttu-id="926c0-775">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-775">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="926c0-776">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="926c0-776">Parameters - mouseDblClick</span></span>

<span data-ttu-id="926c0-777">x</span><span class="sxs-lookup"><span data-stu-id="926c0-777">x</span></span>  
<span data-ttu-id="926c0-778">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-778">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-779">y</span><span class="sxs-lookup"><span data-stu-id="926c0-779">y</span></span>  
<span data-ttu-id="926c0-780">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-780">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-781">ボタン</span><span class="sxs-lookup"><span data-stu-id="926c0-781">button</span></span>  
<span data-ttu-id="926c0-782">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-782">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-783">Ctrl</span><span class="sxs-lookup"><span data-stu-id="926c0-783">Ctrl</span></span>  
<span data-ttu-id="926c0-784">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-784">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-785">シフト</span><span class="sxs-lookup"><span data-stu-id="926c0-785">Shift</span></span>  
<span data-ttu-id="926c0-786">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-786">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="926c0-787">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="926c0-787">Return Value - mouseDblClick</span></span>

<span data-ttu-id="926c0-788">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="926c0-788">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="926c0-789">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="926c0-789">Remarks - mouseDblClick</span></span>

<span data-ttu-id="926c0-790">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-790">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="926c0-791">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="926c0-791">Method mouseDown</span></span>

<span data-ttu-id="926c0-792">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-792">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="926c0-793">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="926c0-793">Parameters - mouseDown</span></span>

<span data-ttu-id="926c0-794">x</span><span class="sxs-lookup"><span data-stu-id="926c0-794">x</span></span>  
<span data-ttu-id="926c0-795">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-795">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-796">y</span><span class="sxs-lookup"><span data-stu-id="926c0-796">y</span></span>  
<span data-ttu-id="926c0-797">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-797">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-798">ボタン</span><span class="sxs-lookup"><span data-stu-id="926c0-798">button</span></span>  
<span data-ttu-id="926c0-799">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-799">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-800">Ctrl</span><span class="sxs-lookup"><span data-stu-id="926c0-800">Ctrl</span></span>  
<span data-ttu-id="926c0-801">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-801">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-802">シフト</span><span class="sxs-lookup"><span data-stu-id="926c0-802">Shift</span></span>  
<span data-ttu-id="926c0-803">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-803">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="926c0-804">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="926c0-804">Return Value - mouseDown</span></span>

<span data-ttu-id="926c0-805">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="926c0-805">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="926c0-806">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="926c0-806">Remarks - mouseDown</span></span>

<span data-ttu-id="926c0-807">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-807">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="926c0-808">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-808">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="926c0-809">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="926c0-809">Method mouseMove</span></span>

<span data-ttu-id="926c0-810">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-810">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="926c0-811">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="926c0-811">Parameters - mouseMove</span></span>

<span data-ttu-id="926c0-812">x</span><span class="sxs-lookup"><span data-stu-id="926c0-812">x</span></span>  
<span data-ttu-id="926c0-813">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-813">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-814">y</span><span class="sxs-lookup"><span data-stu-id="926c0-814">y</span></span>  
<span data-ttu-id="926c0-815">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-815">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-816">ボタン</span><span class="sxs-lookup"><span data-stu-id="926c0-816">button</span></span>  
<span data-ttu-id="926c0-817">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-817">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-818">Ctrl</span><span class="sxs-lookup"><span data-stu-id="926c0-818">Ctrl</span></span>  
<span data-ttu-id="926c0-819">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-819">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-820">シフト</span><span class="sxs-lookup"><span data-stu-id="926c0-820">Shift</span></span>  
<span data-ttu-id="926c0-821">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-821">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="926c0-822">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="926c0-822">Return Value - mouseMove</span></span>

<span data-ttu-id="926c0-823">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="926c0-823">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="926c0-824">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="926c0-824">Remarks - mouseMove</span></span>

<span data-ttu-id="926c0-825">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-825">Typically, when this method is overridden, the return value from a call to super is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="926c0-826">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="926c0-826">Method mouseUp</span></span>

<span data-ttu-id="926c0-827">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-827">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="926c0-828">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="926c0-828">Parameters - mouseUp</span></span>

<span data-ttu-id="926c0-829">x</span><span class="sxs-lookup"><span data-stu-id="926c0-829">x</span></span>  
<span data-ttu-id="926c0-830">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-830">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-831">y</span><span class="sxs-lookup"><span data-stu-id="926c0-831">y</span></span>  
<span data-ttu-id="926c0-832">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-832">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-833">ボタン</span><span class="sxs-lookup"><span data-stu-id="926c0-833">button</span></span>  
<span data-ttu-id="926c0-834">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-834">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-835">Ctrl</span><span class="sxs-lookup"><span data-stu-id="926c0-835">Ctrl</span></span>  
<span data-ttu-id="926c0-836">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-836">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-837">シフト</span><span class="sxs-lookup"><span data-stu-id="926c0-837">Shift</span></span>  
<span data-ttu-id="926c0-838">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-838">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="926c0-839">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="926c0-839">Return Value - mouseUp</span></span>

<span data-ttu-id="926c0-840">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="926c0-840">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="926c0-841">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="926c0-841">Remarks - mouseUp</span></span>

<span data-ttu-id="926c0-842">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-842">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="926c0-843">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-843">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="926c0-844">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="926c0-844">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="926c0-845">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="926c0-845">Parameters - moveControl</span></span>

<span data-ttu-id="926c0-846">controlId</span><span class="sxs-lookup"><span data-stu-id="926c0-846">controlId</span></span>  

<!-- -->

<span data-ttu-id="926c0-847">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="926c0-847">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="926c0-848">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="926c0-848">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="926c0-849">メソッド名</span><span class="sxs-lookup"><span data-stu-id="926c0-849">Method name</span></span>

<span data-ttu-id="926c0-850">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-850">Gets or sets the name used in code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="926c0-851">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="926c0-851">Parameters - name</span></span>

<span data-ttu-id="926c0-852">値</span><span class="sxs-lookup"><span data-stu-id="926c0-852">value</span></span>  
<span data-ttu-id="926c0-853">コントロールに割り当てられた名前。</span><span class="sxs-lookup"><span data-stu-id="926c0-853">The name assigned to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="926c0-854">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="926c0-854">Return Value - name</span></span>

<span data-ttu-id="926c0-855">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="926c0-855">The name used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="926c0-856">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="926c0-856">Remarks - name</span></span>

<span data-ttu-id="926c0-857">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="926c0-857">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="926c0-858">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="926c0-858">Begins with a letter.</span></span>
-   <span data-ttu-id="926c0-859">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="926c0-859">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="926c0-860">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="926c0-860">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="926c0-861">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="926c0-861">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="926c0-862">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="926c0-862">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="926c0-863">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="926c0-863">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="926c0-864">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="926c0-864">Parameters - neededPermission</span></span>

<span data-ttu-id="926c0-865">値</span><span class="sxs-lookup"><span data-stu-id="926c0-865">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="926c0-866">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="926c0-866">Return Value - neededPermission</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="926c0-867">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="926c0-867">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="926c0-868">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="926c0-868">Parameters - normalImage</span></span>

<span data-ttu-id="926c0-869">値</span><span class="sxs-lookup"><span data-stu-id="926c0-869">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="926c0-870">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="926c0-870">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="926c0-871">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="926c0-871">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="926c0-872">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="926c0-872">Parameters - normalResource</span></span>

<span data-ttu-id="926c0-873">値</span><span class="sxs-lookup"><span data-stu-id="926c0-873">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="926c0-874">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="926c0-874">Return Value - normalResource</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="926c0-875">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="926c0-875">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="926c0-876">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="926c0-876">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="926c0-877">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="926c0-877">Method parentControl</span></span>

<span data-ttu-id="926c0-878">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-878">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="926c0-879">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="926c0-879">Return Value - parentControl</span></span>

<span data-ttu-id="926c0-880">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="926c0-880">The parent control for the control.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="926c0-881">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-881">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="926c0-882">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-882">Parameters - rightMargin</span></span>

<span data-ttu-id="926c0-883">値</span><span class="sxs-lookup"><span data-stu-id="926c0-883">value</span></span>  

<!-- -->

<span data-ttu-id="926c0-884">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-884">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="926c0-885">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-885">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="926c0-886">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-886">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="926c0-887">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-887">Parameters - rightMarginMode</span></span>

<span data-ttu-id="926c0-888">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-888">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="926c0-889">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-889">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="926c0-890">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-890">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="926c0-891">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-891">Parameters - rightMarginValue</span></span>

<span data-ttu-id="926c0-892">値</span><span class="sxs-lookup"><span data-stu-id="926c0-892">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="926c0-893">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-893">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="926c0-894">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="926c0-894">Method securityKey</span></span>

<span data-ttu-id="926c0-895">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-895">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="926c0-896">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="926c0-896">Parameters - securityKey</span></span>

<span data-ttu-id="926c0-897">値</span><span class="sxs-lookup"><span data-stu-id="926c0-897">value</span></span>  
<span data-ttu-id="926c0-898">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-898">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="926c0-899">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="926c0-899">Return Value - securityKey</span></span>

<span data-ttu-id="926c0-900">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="926c0-900">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="926c0-901">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="926c0-901">Method showContextMenu</span></span>

<span data-ttu-id="926c0-902">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-902">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="926c0-903">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="926c0-903">Parameters - showContextMenu</span></span>

<span data-ttu-id="926c0-904">menuHandle</span><span class="sxs-lookup"><span data-stu-id="926c0-904">menuHandle</span></span>  
<span data-ttu-id="926c0-905">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="926c0-905">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="926c0-906">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="926c0-906">Return Value - showContextMenu</span></span>

<span data-ttu-id="926c0-907">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-907">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="926c0-908">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="926c0-908">Method skip</span></span>

<span data-ttu-id="926c0-909">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-909">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="926c0-910">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="926c0-910">Parameters - skip</span></span>

<span data-ttu-id="926c0-911">値</span><span class="sxs-lookup"><span data-stu-id="926c0-911">value</span></span>  
<span data-ttu-id="926c0-912">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-912">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="926c0-913">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="926c0-913">Return Value - skip</span></span>

<span data-ttu-id="926c0-914">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="926c0-914">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="926c0-915">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="926c0-915">Remarks - skip</span></span>

<span data-ttu-id="926c0-916">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="926c0-916">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="926c0-917">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="926c0-917">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="926c0-918">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="926c0-918">Parameters - sort</span></span>

<span data-ttu-id="926c0-919">sortDirection</span><span class="sxs-lookup"><span data-stu-id="926c0-919">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="926c0-920">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="926c0-920">Return Value - sort</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="926c0-921">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="926c0-921">Method toolTip</span></span>

<span data-ttu-id="926c0-922">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="926c0-922">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="926c0-923">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="926c0-923">Return Value - toolTip</span></span>

<span data-ttu-id="926c0-924">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="926c0-924">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="926c0-925">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="926c0-925">Remarks - toolTip</span></span>

<span data-ttu-id="926c0-926">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="926c0-926">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="926c0-927">メソッド top</span><span class="sxs-lookup"><span data-stu-id="926c0-927">Method top</span></span>

<span data-ttu-id="926c0-928">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-928">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="926c0-929">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="926c0-929">Parameters - top</span></span>

<span data-ttu-id="926c0-930">値</span><span class="sxs-lookup"><span data-stu-id="926c0-930">value</span></span>  
<span data-ttu-id="926c0-931">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-931">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="926c0-932">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-932">mode</span></span>  
<span data-ttu-id="926c0-933">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-933">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="926c0-934">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="926c0-934">Return Value - top</span></span>

<span data-ttu-id="926c0-935">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="926c0-935">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="926c0-936">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-936">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="926c0-937">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-937">Parameters - topMargin</span></span>

<span data-ttu-id="926c0-938">値</span><span class="sxs-lookup"><span data-stu-id="926c0-938">value</span></span>  

<!-- -->

<span data-ttu-id="926c0-939">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-939">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="926c0-940">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="926c0-940">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="926c0-941">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-941">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="926c0-942">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-942">Parameters - topMarginMode</span></span>

<span data-ttu-id="926c0-943">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-943">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="926c0-944">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="926c0-944">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="926c0-945">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-945">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="926c0-946">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-946">Parameters - topMarginValue</span></span>

<span data-ttu-id="926c0-947">値</span><span class="sxs-lookup"><span data-stu-id="926c0-947">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="926c0-948">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="926c0-948">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="926c0-949">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="926c0-949">Method topMode</span></span>

<span data-ttu-id="926c0-950">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-950">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="926c0-951">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="926c0-951">Parameters - topMode</span></span>

<span data-ttu-id="926c0-952">値</span><span class="sxs-lookup"><span data-stu-id="926c0-952">value</span></span>  
<span data-ttu-id="926c0-953">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-953">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="926c0-954">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="926c0-954">Return Value - topMode</span></span>

<span data-ttu-id="926c0-955">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="926c0-955">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="926c0-956">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="926c0-956">Method topValue</span></span>

<span data-ttu-id="926c0-957">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-957">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="926c0-958">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="926c0-958">Parameters - topValue</span></span>

<span data-ttu-id="926c0-959">値</span><span class="sxs-lookup"><span data-stu-id="926c0-959">value</span></span>  
<span data-ttu-id="926c0-960">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-960">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="926c0-961">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="926c0-961">Return Value - topValue</span></span>

<span data-ttu-id="926c0-962">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="926c0-962">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="926c0-963">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="926c0-963">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="926c0-964">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="926c0-964">Parameters - type</span></span>

<span data-ttu-id="926c0-965">値</span><span class="sxs-lookup"><span data-stu-id="926c0-965">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="926c0-966">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="926c0-966">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="926c0-967">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="926c0-967">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="926c0-968">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="926c0-968">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="926c0-969">データ</span><span class="sxs-lookup"><span data-stu-id="926c0-969">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="926c0-970">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="926c0-970">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="926c0-971">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="926c0-971">Method userData</span></span>

<span data-ttu-id="926c0-972">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-972">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="926c0-973">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="926c0-973">Parameters - userData</span></span>

<span data-ttu-id="926c0-974">値</span><span class="sxs-lookup"><span data-stu-id="926c0-974">value</span></span>  
<span data-ttu-id="926c0-975">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-975">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="926c0-976">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="926c0-976">Return Value - userData</span></span>

<span data-ttu-id="926c0-977">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="926c0-977">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="926c0-978">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="926c0-978">Method userDataItem</span></span>

<span data-ttu-id="926c0-979">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-979">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="926c0-980">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="926c0-980">Parameters - userDataItem</span></span>

<span data-ttu-id="926c0-981">値</span><span class="sxs-lookup"><span data-stu-id="926c0-981">value</span></span>  
<span data-ttu-id="926c0-982">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-982">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="926c0-983">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="926c0-983">Return Value - userDataItem</span></span>

<span data-ttu-id="926c0-984">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="926c0-984">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="926c0-985">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="926c0-985">Method userDataItems</span></span>

<span data-ttu-id="926c0-986">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-986">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="926c0-987">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="926c0-987">Parameters - userDataItems</span></span>

<span data-ttu-id="926c0-988">値</span><span class="sxs-lookup"><span data-stu-id="926c0-988">value</span></span>  
<span data-ttu-id="926c0-989">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-989">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="926c0-990">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="926c0-990">Return Value - userDataItems</span></span>

<span data-ttu-id="926c0-991">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="926c0-991">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="926c0-992">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="926c0-992">Method userDisable</span></span>

<span data-ttu-id="926c0-993">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-993">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="926c0-994">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="926c0-994">Parameters - userDisable</span></span>

<span data-ttu-id="926c0-995">値</span><span class="sxs-lookup"><span data-stu-id="926c0-995">value</span></span>  
<span data-ttu-id="926c0-996">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-996">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="926c0-997">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="926c0-997">Return Value - userDisable</span></span>

<span data-ttu-id="926c0-998">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="926c0-998">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="926c0-999">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="926c0-999">Method userHeight</span></span>

<span data-ttu-id="926c0-1000">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1000">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="926c0-1001">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="926c0-1001">Parameters - userHeight</span></span>

<span data-ttu-id="926c0-1002">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1002">value</span></span>  
<span data-ttu-id="926c0-1003">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1003">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="926c0-1004">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="926c0-1004">Return Value - userHeight</span></span>

<span data-ttu-id="926c0-1005">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="926c0-1005">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="926c0-1006">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="926c0-1006">Method userHide</span></span>

<span data-ttu-id="926c0-1007">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1007">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="926c0-1008">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="926c0-1008">Parameters - userHide</span></span>

<span data-ttu-id="926c0-1009">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1009">value</span></span>  
<span data-ttu-id="926c0-1010">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1010">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="926c0-1011">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="926c0-1011">Return Value - userHide</span></span>

<span data-ttu-id="926c0-1012">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="926c0-1012">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="926c0-1013">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="926c0-1013">Remarks - userHide</span></span>

<span data-ttu-id="926c0-1014">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1014">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="926c0-1015">右クリックすると、コントロールを非表示または表示できるメニューが起動します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1015">Right-clicking invokes a menu that enables the control to be hidden or displayed.</span></span> <span data-ttu-id="926c0-1016">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1016">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="926c0-1017">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="926c0-1017">Method userOrgContainer</span></span>

<span data-ttu-id="926c0-1018">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1018">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="926c0-1019">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="926c0-1019">Parameters - userOrgContainer</span></span>

<span data-ttu-id="926c0-1020">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1020">value</span></span>  
<span data-ttu-id="926c0-1021">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1021">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="926c0-1022">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="926c0-1022">Return Value - userOrgContainer</span></span>

<span data-ttu-id="926c0-1023">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="926c0-1023">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="926c0-1024">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="926c0-1024">Method userOrgSibling</span></span>

<span data-ttu-id="926c0-1025">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1025">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="926c0-1026">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="926c0-1026">Parameters - userOrgSibling</span></span>

<span data-ttu-id="926c0-1027">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1027">value</span></span>  
<span data-ttu-id="926c0-1028">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1028">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="926c0-1029">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="926c0-1029">Return Value - userOrgSibling</span></span>

<span data-ttu-id="926c0-1030">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="926c0-1030">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="926c0-1031">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="926c0-1031">Method userPromptText</span></span>

<span data-ttu-id="926c0-1032">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1032">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="926c0-1033">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="926c0-1033">Parameters - userPromptText</span></span>

<span data-ttu-id="926c0-1034">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1034">value</span></span>  
<span data-ttu-id="926c0-1035">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1035">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="926c0-1036">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="926c0-1036">Return Value - userPromptText</span></span>

<span data-ttu-id="926c0-1037">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="926c0-1037">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="926c0-1038">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="926c0-1038">Method userSecurityLevel</span></span>

<span data-ttu-id="926c0-1039">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1039">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="926c0-1040">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="926c0-1040">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="926c0-1041">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1041">value</span></span>  
<span data-ttu-id="926c0-1042">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1042">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="926c0-1043">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="926c0-1043">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="926c0-1044">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="926c0-1044">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="926c0-1045">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="926c0-1045">Method userSkip</span></span>

<span data-ttu-id="926c0-1046">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1046">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="926c0-1047">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="926c0-1047">Parameters - userSkip</span></span>

<span data-ttu-id="926c0-1048">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1048">value</span></span>  
<span data-ttu-id="926c0-1049">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1049">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="926c0-1050">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="926c0-1050">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="926c0-1051">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="926c0-1051">Return Value - userSkip</span></span>

<span data-ttu-id="926c0-1052">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="926c0-1052">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="926c0-1053">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="926c0-1053">Method userWidth</span></span>

<span data-ttu-id="926c0-1054">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1054">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="926c0-1055">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="926c0-1055">Parameters - userWidth</span></span>

<span data-ttu-id="926c0-1056">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1056">value</span></span>  
<span data-ttu-id="926c0-1057">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1057">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="926c0-1058">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="926c0-1058">Return Value - userWidth</span></span>

<span data-ttu-id="926c0-1059">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1059">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="926c0-1060">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="926c0-1060">Remarks - userWidth</span></span>

<span data-ttu-id="926c0-1061">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1061">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="926c0-1062">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻りは 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="926c0-1062">For example, if the user has specified 30 characters as the width for the control, the return is 6 \* 30 = 180.</span></span> <span data-ttu-id="926c0-1063">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1063">To specify the width of the control in characters, users can right-click the control to invoke the setup form in which the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="926c0-1064">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="926c0-1064">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="926c0-1065">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="926c0-1065">Parameters - useUserLayout</span></span>

<span data-ttu-id="926c0-1066">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1066">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="926c0-1067">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="926c0-1067">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="926c0-1068">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="926c0-1068">Method verticalSpacing</span></span>

<span data-ttu-id="926c0-1069">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1069">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="926c0-1070">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="926c0-1070">Parameters - verticalSpacing</span></span>

<span data-ttu-id="926c0-1071">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1071">value</span></span>  
<span data-ttu-id="926c0-1072">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-1072">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="926c0-1073">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-1073">mode</span></span>  
<span data-ttu-id="926c0-1074">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-1074">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="926c0-1075">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="926c0-1075">Return Value - verticalSpacing</span></span>

<span data-ttu-id="926c0-1076">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="926c0-1076">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="926c0-1077">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="926c0-1077">Method verticalSpacingMode</span></span>

<span data-ttu-id="926c0-1078">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1078">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="926c0-1079">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="926c0-1079">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="926c0-1080">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-1080">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="926c0-1081">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="926c0-1081">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="926c0-1082">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="926c0-1082">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="926c0-1083">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="926c0-1083">Method verticalSpacingValue</span></span>

<span data-ttu-id="926c0-1084">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1084">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="926c0-1085">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="926c0-1085">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="926c0-1086">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1086">value</span></span>  
<span data-ttu-id="926c0-1087">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="926c0-1087">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="926c0-1088">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="926c0-1088">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="926c0-1089">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="926c0-1089">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="926c0-1090">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="926c0-1090">Method visible</span></span>

<span data-ttu-id="926c0-1091">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1091">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="926c0-1092">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="926c0-1092">Parameters - visible</span></span>

<span data-ttu-id="926c0-1093">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1093">value</span></span>  
<span data-ttu-id="926c0-1094">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1094">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="926c0-1095">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="926c0-1095">Return Value - visible</span></span>

<span data-ttu-id="926c0-1096">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="926c0-1096">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="926c0-1097">メソッド width</span><span class="sxs-lookup"><span data-stu-id="926c0-1097">Method width</span></span>

<span data-ttu-id="926c0-1098">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1098">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="926c0-1099">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="926c0-1099">Parameters - width</span></span>

<span data-ttu-id="926c0-1100">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1100">value</span></span>  
<span data-ttu-id="926c0-1101">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="926c0-1101">An Integer data type that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="926c0-1102">モード</span><span class="sxs-lookup"><span data-stu-id="926c0-1102">mode</span></span>  
<span data-ttu-id="926c0-1103">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="926c0-1103">An Integer data type that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="926c0-1104">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="926c0-1104">Return Value - width</span></span>

<span data-ttu-id="926c0-1105">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="926c0-1105">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="926c0-1106">備考 - width</span><span class="sxs-lookup"><span data-stu-id="926c0-1106">Remarks - width</span></span>

<span data-ttu-id="926c0-1107">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1107">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="926c0-1108">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="926c0-1108">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="926c0-1109">モード。</span><span class="sxs-lookup"><span data-stu-id="926c0-1109">Mode.</span></span>           | <span data-ttu-id="926c0-1110">幅計算。</span><span class="sxs-lookup"><span data-stu-id="926c0-1110">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="926c0-1111">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="926c0-1111">-1 Exact.</span></span>       | <span data-ttu-id="926c0-1112">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1112">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="926c0-1113">0 自動。</span><span class="sxs-lookup"><span data-stu-id="926c0-1113">0 Auto.</span></span>         | <span data-ttu-id="926c0-1114">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1114">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="926c0-1115">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="926c0-1115">1 Column width.</span></span> | <span data-ttu-id="926c0-1116">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="926c0-1116">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="926c0-1117">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1117">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="926c0-1118">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="926c0-1118">Method widthMode</span></span>

<span data-ttu-id="926c0-1119">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1119">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="926c0-1120">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="926c0-1120">Parameters - widthMode</span></span>

<span data-ttu-id="926c0-1121">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1121">value</span></span>  
<span data-ttu-id="926c0-1122">コントロール幅の計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1122">An Integer data type value that indicates how the control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="926c0-1123">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="926c0-1123">Return Value - widthMode</span></span>

<span data-ttu-id="926c0-1124">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1124">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="926c0-1125">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="926c0-1125">Remarks - widthMode</span></span>

<span data-ttu-id="926c0-1126">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="926c0-1126">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="926c0-1127">モード。</span><span class="sxs-lookup"><span data-stu-id="926c0-1127">Mode.</span></span>         | <span data-ttu-id="926c0-1128">幅計算。</span><span class="sxs-lookup"><span data-stu-id="926c0-1128">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="926c0-1129">正確。</span><span class="sxs-lookup"><span data-stu-id="926c0-1129">Exact.</span></span>        | <span data-ttu-id="926c0-1130">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1130">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="926c0-1131">自動。</span><span class="sxs-lookup"><span data-stu-id="926c0-1131">Auto.</span></span>         | <span data-ttu-id="926c0-1132">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1132">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="926c0-1133">列の幅。</span><span class="sxs-lookup"><span data-stu-id="926c0-1133">Column width.</span></span> | <span data-ttu-id="926c0-1134">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="926c0-1134">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="926c0-1135">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="926c0-1135">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="926c0-1136">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="926c0-1136">Method widthValue</span></span>

<span data-ttu-id="926c0-1137">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1137">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="926c0-1138">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="926c0-1138">Parameters - widthValue</span></span>

<span data-ttu-id="926c0-1139">値</span><span class="sxs-lookup"><span data-stu-id="926c0-1139">value</span></span>  
<span data-ttu-id="926c0-1140">幅をピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1140">An Integer data type that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="926c0-1141">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="926c0-1141">Return Value - widthValue</span></span>

<span data-ttu-id="926c0-1142">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="926c0-1142">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="926c0-1143">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="926c0-1143">Remarks - widthValue</span></span>

<span data-ttu-id="926c0-1144">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1144">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-onenter"></a><span data-ttu-id="926c0-1145">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="926c0-1145">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="926c0-1146">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="926c0-1146">Parameters - OnEnter</span></span>

<span data-ttu-id="926c0-1147">sender</span><span class="sxs-lookup"><span data-stu-id="926c0-1147">sender</span></span>  

<!-- -->

<span data-ttu-id="926c0-1148">e</span><span class="sxs-lookup"><span data-stu-id="926c0-1148">e</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="926c0-1149">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="926c0-1149">Method setFocus</span></span>

<span data-ttu-id="926c0-1150">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1150">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="926c0-1151">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="926c0-1151">Method resetUserSetting</span></span>

<span data-ttu-id="926c0-1152">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="926c0-1152">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-drop"></a><span data-ttu-id="926c0-1153">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="926c0-1153">Method drop</span></span>

<span data-ttu-id="926c0-1154">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1154">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="926c0-1155">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="926c0-1155">Parameters - drop</span></span>

<span data-ttu-id="926c0-1156">dragSource</span><span class="sxs-lookup"><span data-stu-id="926c0-1156">dragSource</span></span>  
<span data-ttu-id="926c0-1157">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1157">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-1158">dragMode</span><span class="sxs-lookup"><span data-stu-id="926c0-1158">dragMode</span></span>  
<span data-ttu-id="926c0-1159">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1159">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-1160">x</span><span class="sxs-lookup"><span data-stu-id="926c0-1160">x</span></span>  
<span data-ttu-id="926c0-1161">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1161">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-1162">y</span><span class="sxs-lookup"><span data-stu-id="926c0-1162">y</span></span>  
<span data-ttu-id="926c0-1163">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1163">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="926c0-1164">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="926c0-1164">Method mouseEnter</span></span>

<span data-ttu-id="926c0-1165">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1165">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="926c0-1166">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="926c0-1166">Parameters - mouseEnter</span></span>

<span data-ttu-id="926c0-1167">x</span><span class="sxs-lookup"><span data-stu-id="926c0-1167">x</span></span>  
<span data-ttu-id="926c0-1168">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1168">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-1169">y</span><span class="sxs-lookup"><span data-stu-id="926c0-1169">y</span></span>  
<span data-ttu-id="926c0-1170">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1170">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-1171">ボタン</span><span class="sxs-lookup"><span data-stu-id="926c0-1171">button</span></span>  
<span data-ttu-id="926c0-1172">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1172">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-1173">Ctrl</span><span class="sxs-lookup"><span data-stu-id="926c0-1173">Ctrl</span></span>  
<span data-ttu-id="926c0-1174">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1174">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="926c0-1175">シフト</span><span class="sxs-lookup"><span data-stu-id="926c0-1175">Shift</span></span>  
<span data-ttu-id="926c0-1176">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1176">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-gotfocus"></a><span data-ttu-id="926c0-1177">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="926c0-1177">Method gotFocus</span></span>

<span data-ttu-id="926c0-1178">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1178">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-onleaving"></a><span data-ttu-id="926c0-1179">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="926c0-1179">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="926c0-1180">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="926c0-1180">Parameters - OnLeaving</span></span>

<span data-ttu-id="926c0-1181">sender</span><span class="sxs-lookup"><span data-stu-id="926c0-1181">sender</span></span>  

<!-- -->

<span data-ttu-id="926c0-1182">e</span><span class="sxs-lookup"><span data-stu-id="926c0-1182">e</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="926c0-1183">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="926c0-1183">Method prefColumnSize</span></span>

<span data-ttu-id="926c0-1184">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1184">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="926c0-1185">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="926c0-1185">Parameters - prefColumnSize</span></span>

<span data-ttu-id="926c0-1186">width</span><span class="sxs-lookup"><span data-stu-id="926c0-1186">width</span></span>  
<span data-ttu-id="926c0-1187">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="926c0-1187">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="926c0-1188">height</span><span class="sxs-lookup"><span data-stu-id="926c0-1188">height</span></span>  
<span data-ttu-id="926c0-1189">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="926c0-1189">The preferred height of the control.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="926c0-1190">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="926c0-1190">Method endDrag</span></span>

<span data-ttu-id="926c0-1191">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1191">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="926c0-1192">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="926c0-1192">Remarks - endDrag</span></span>

<span data-ttu-id="926c0-1193">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="926c0-1193">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="926c0-1194">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1194">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="926c0-1195">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="926c0-1195">Method mouseLeave</span></span>

<span data-ttu-id="926c0-1196">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1196">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-inputsearch"></a><span data-ttu-id="926c0-1197">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="926c0-1197">Method inputSearch</span></span>

<span data-ttu-id="926c0-1198">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1198">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="926c0-1199">パラメーター - inputSerach</span><span class="sxs-lookup"><span data-stu-id="926c0-1199">Parameters - inputSearch</span></span>

<span data-ttu-id="926c0-1200">searchStr</span><span class="sxs-lookup"><span data-stu-id="926c0-1200">searchStr</span></span>  
<span data-ttu-id="926c0-1201">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="926c0-1201">The string value to use to filter data; optional.</span></span>

## <a name="method-enter"></a><span data-ttu-id="926c0-1202">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="926c0-1202">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-context"></a><span data-ttu-id="926c0-1203">メソッド context</span><span class="sxs-lookup"><span data-stu-id="926c0-1203">Method context</span></span>

<span data-ttu-id="926c0-1204">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1204">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-dropex"></a><span data-ttu-id="926c0-1205">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="926c0-1205">Method dropEx</span></span>

<span data-ttu-id="926c0-1206">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1206">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="926c0-1207">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="926c0-1207">Parameters - dropEx</span></span>

<span data-ttu-id="926c0-1208">dragSource</span><span class="sxs-lookup"><span data-stu-id="926c0-1208">dragSource</span></span>  
<span data-ttu-id="926c0-1209">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1209">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-1210">dragMode</span><span class="sxs-lookup"><span data-stu-id="926c0-1210">dragMode</span></span>  
<span data-ttu-id="926c0-1211">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1211">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-1212">x</span><span class="sxs-lookup"><span data-stu-id="926c0-1212">x</span></span>  
<span data-ttu-id="926c0-1213">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1213">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="926c0-1214">y</span><span class="sxs-lookup"><span data-stu-id="926c0-1214">y</span></span>  
<span data-ttu-id="926c0-1215">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="926c0-1215">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-jumpref"></a><span data-ttu-id="926c0-1216">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="926c0-1216">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-onselectionchanged"></a><span data-ttu-id="926c0-1217">メソッド OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="926c0-1217">Method OnSelectionChanged</span></span>

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a><span data-ttu-id="926c0-1218">パラメーター - OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="926c0-1218">Parameters - OnSelectionChanged</span></span>

<span data-ttu-id="926c0-1219">sender</span><span class="sxs-lookup"><span data-stu-id="926c0-1219">sender</span></span>  

<!-- -->

<span data-ttu-id="926c0-1220">e</span><span class="sxs-lookup"><span data-stu-id="926c0-1220">e</span></span>  

## <a name="method-registeroverridemethod"></a><span data-ttu-id="926c0-1221">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="926c0-1221">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="926c0-1222">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="926c0-1222">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="926c0-1223">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="926c0-1223">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="926c0-1224">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="926c0-1224">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="926c0-1225">overrideObject</span><span class="sxs-lookup"><span data-stu-id="926c0-1225">overrideObject</span></span>  

## <a name="method-cut"></a><span data-ttu-id="926c0-1226">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="926c0-1226">Method cut</span></span>

<span data-ttu-id="926c0-1227">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="926c0-1227">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-lostfocus"></a><span data-ttu-id="926c0-1228">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="926c0-1228">Method lostFocus</span></span>

<span data-ttu-id="926c0-1229">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1229">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="926c0-1230">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="926c0-1230">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="926c0-1231">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="926c0-1231">Parameters - OnGotFocus</span></span>

<span data-ttu-id="926c0-1232">sender</span><span class="sxs-lookup"><span data-stu-id="926c0-1232">sender</span></span>  

<!-- -->

<span data-ttu-id="926c0-1233">e</span><span class="sxs-lookup"><span data-stu-id="926c0-1233">e</span></span>  

## <a name="method-copy"></a><span data-ttu-id="926c0-1234">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="926c0-1234">Method copy</span></span>

<span data-ttu-id="926c0-1235">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="926c0-1235">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-dragleave"></a><span data-ttu-id="926c0-1236">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="926c0-1236">Method dragLeave</span></span>

<span data-ttu-id="926c0-1237">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1237">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-selectionchanged"></a><span data-ttu-id="926c0-1238">メソッド selectionChanged</span><span class="sxs-lookup"><span data-stu-id="926c0-1238">Method selectionChanged</span></span>

```xpp
public void selectionChanged()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="926c0-1239">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="926c0-1239">Method displayControl</span></span>

<span data-ttu-id="926c0-1240">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="926c0-1240">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-paste"></a><span data-ttu-id="926c0-1241">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="926c0-1241">Method paste</span></span>

<span data-ttu-id="926c0-1242">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="926c0-1242">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-arrange"></a><span data-ttu-id="926c0-1243">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="926c0-1243">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="926c0-1244">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="926c0-1244">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="926c0-1245">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="926c0-1245">Parameters - OnLostFocus</span></span>

<span data-ttu-id="926c0-1246">sender</span><span class="sxs-lookup"><span data-stu-id="926c0-1246">sender</span></span>  

<!-- -->

<span data-ttu-id="926c0-1247">e</span><span class="sxs-lookup"><span data-stu-id="926c0-1247">e</span></span>  

## <a name="method-filter"></a><span data-ttu-id="926c0-1248">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="926c0-1248">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="926c0-1249">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="926c0-1249">Parameters - filter</span></span>

<span data-ttu-id="926c0-1250">filterStr</span><span class="sxs-lookup"><span data-stu-id="926c0-1250">filterStr</span></span>  

