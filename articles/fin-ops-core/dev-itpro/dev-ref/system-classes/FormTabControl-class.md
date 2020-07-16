---
title: FormTabControl クラス
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
ms.openlocfilehash: 922a1ba49b29d4d59d4d247c8e52512ca06630d2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502911"
---
# <a name="class-formtabcontrol"></a><span data-ttu-id="09a33-103">クラス FormTabControl</span><span class="sxs-lookup"><span data-stu-id="09a33-103">Class FormTabControl</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormTabControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="09a33-104">備考</span><span class="sxs-lookup"><span data-stu-id="09a33-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="09a33-105">例</span><span class="sxs-lookup"><span data-stu-id="09a33-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="09a33-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="09a33-106">Methods</span></span>

| <span data-ttu-id="09a33-107">方法</span><span class="sxs-lookup"><span data-stu-id="09a33-107">Method</span></span>                                                                                                              | <span data-ttu-id="09a33-108">説明</span><span class="sxs-lookup"><span data-stu-id="09a33-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a33-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="09a33-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="09a33-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="09a33-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="09a33-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="09a33-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="09a33-112">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-112">public boolean alignChild(\[boolean value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-113">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-113">public boolean alignChildren(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="09a33-114">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-114">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="09a33-115">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-115">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="09a33-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="09a33-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-117">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="09a33-118">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="09a33-118">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="09a33-119">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-119">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="09a33-120">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-120">public int allowUserSetup(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="09a33-121">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-121">public int arrangeGuide(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="09a33-122">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-122">public int arrangeMethod(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="09a33-123">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-123">public int arrangeWhen(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="09a33-124">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-124">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="09a33-125">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-125">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="09a33-126">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-126">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="09a33-127">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-127">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="09a33-128">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-128">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="09a33-129">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-129">Determines whether the control background can be transparent.</span></span>                                                                                                           |
| <span data-ttu-id="09a33-130">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="09a33-130">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="09a33-131">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-131">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="09a33-132">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-132">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="09a33-133">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-133">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="09a33-134">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-134">public int bottomMarginValue(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="09a33-135">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="09a33-135">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="09a33-136">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-136">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="09a33-137">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="09a33-137">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="09a33-138">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="09a33-138">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="09a33-139">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-139">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="09a33-140">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-140">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="09a33-141">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-141">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="09a33-142">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-142">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="09a33-143">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-143">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="09a33-144">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-144">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="09a33-145">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-145">public int columnspaceValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="09a33-146">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-146">public int columnsValue(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="09a33-147">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-147">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="09a33-148">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-148">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="09a33-149">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="09a33-149">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="09a33-150">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-150">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="09a33-151">public int containerScrollHorizontalOffset(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-151">public int containerScrollHorizontalOffset(\[int value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="09a33-152">public int containerScrollVerticalOffset(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-152">public int containerScrollVerticalOffset(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="09a33-153">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="09a33-153">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-154">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="09a33-154">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="09a33-155">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="09a33-155">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-156">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-156">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="09a33-157">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-157">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="09a33-158">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-158">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="09a33-159">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-159">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="09a33-160">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-160">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="09a33-161">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-161">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="09a33-162">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-162">Gets or sets a data source that is used by the control or the form.</span></span>                                                                                                     |
| <span data-ttu-id="09a33-163">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-163">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="09a33-164">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-164">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="09a33-165">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-165">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="09a33-166">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-166">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="09a33-167">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="09a33-167">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="09a33-168">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-168">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="09a33-169">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="09a33-169">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="09a33-170">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-170">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="09a33-171">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="09a33-171">public str dragText()</span></span>                                                                                               | <span data-ttu-id="09a33-172">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-172">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="09a33-173">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-173">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="09a33-174">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-174">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="09a33-175">public FormControl getActivePage()</span><span class="sxs-lookup"><span data-stu-id="09a33-175">public FormControl getActivePage()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="09a33-176">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="09a33-176">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="09a33-177">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-177">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="09a33-178">public boolean hasControlPositionOverride()</span><span class="sxs-lookup"><span data-stu-id="09a33-178">public boolean hasControlPositionOverride()</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="09a33-179">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="09a33-179">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="09a33-180">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-180">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="09a33-181">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-181">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="09a33-182">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-182">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="09a33-183">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-183">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="09a33-184">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-184">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="09a33-185">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-185">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="09a33-186">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-186">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="09a33-187">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="09a33-187">public str helpField()</span></span>                                                                                              | <span data-ttu-id="09a33-188">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-188">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="09a33-189">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-189">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="09a33-190">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-190">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="09a33-191">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-191">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="09a33-192">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-192">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="09a33-193">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-193">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="09a33-194">public boolean horizontalScrollBarVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-194">public boolean horizontalScrollBarVisible(\[boolean value\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-195">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="09a33-195">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="09a33-196">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-196">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="09a33-197">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="09a33-197">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-198">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="09a33-198">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="09a33-199">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-199">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="09a33-200">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="09a33-200">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="09a33-201">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-201">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="09a33-202">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="09a33-202">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="09a33-203">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-203">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="09a33-204">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-204">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="09a33-205">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-205">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="09a33-206">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-206">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="09a33-207">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-207">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="09a33-208">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-208">public int leftMarginValue(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="09a33-209">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-209">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="09a33-210">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-210">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="09a33-211">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-211">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="09a33-212">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-212">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="09a33-213">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-213">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="09a33-214">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="09a33-214">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="09a33-215">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="09a33-215">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="09a33-216">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-216">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="09a33-217">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="09a33-217">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="09a33-218">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-218">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="09a33-219">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="09a33-219">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="09a33-220">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-220">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="09a33-221">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="09a33-221">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="09a33-222">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-222">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="09a33-223">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="09a33-223">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-224">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-224">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="09a33-225">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-225">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                               |
| <span data-ttu-id="09a33-226">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-226">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="09a33-227">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="09a33-227">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="09a33-228">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="09a33-228">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="09a33-229">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-229">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="09a33-230">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-230">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="09a33-231">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-231">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="09a33-232">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-232">public int rightMarginValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="09a33-233">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-233">public int scrollbars(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="09a33-234">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-234">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="09a33-235">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-235">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="09a33-236">public boolean selectControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-236">public boolean selectControl(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="09a33-237">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="09a33-237">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="09a33-238">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-238">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="09a33-239">public boolean showTabs(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-239">public boolean showTabs(\[boolean value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="09a33-240">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-240">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="09a33-241">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-241">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="09a33-242">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="09a33-242">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-243">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-243">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="09a33-244">public TabStyle styleValue()</span><span class="sxs-lookup"><span data-stu-id="09a33-244">public TabStyle styleValue()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-245">public int tab(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-245">public int tab(\[int value\], \[AutoMode mode\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="09a33-246">public int tabAppearance(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-246">public int tabAppearance(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="09a33-247">public boolean tabAutoChange(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-247">public boolean tabAutoChange(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="09a33-248">public boolean tabChange(int FromTab)</span><span class="sxs-lookup"><span data-stu-id="09a33-248">public boolean tabChange(int FromTab)</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="09a33-249">public int tabLayout(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-249">public int tabLayout(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="09a33-250">public AutoMode tabMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-250">public AutoMode tabMode(\[AutoMode mode\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="09a33-251">public int tabPlacement(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-251">public int tabPlacement(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="09a33-252">public int tabs(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-252">public int tabs(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="09a33-253">public int tabValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-253">public int tabValue(\[int value\])</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="09a33-254">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="09a33-254">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="09a33-255">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-255">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="09a33-256">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-256">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="09a33-257">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-257">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="09a33-258">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-258">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="09a33-259">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-259">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="09a33-260">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-260">public int topMarginValue(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="09a33-261">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-261">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="09a33-262">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-262">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="09a33-263">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-263">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="09a33-264">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-264">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="09a33-265">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-265">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="09a33-266">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="09a33-266">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="09a33-267">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-267">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="09a33-268">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-268">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="09a33-269">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-269">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="09a33-270">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-270">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="09a33-271">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-271">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="09a33-272">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-272">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="09a33-273">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-273">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="09a33-274">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-274">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="09a33-275">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-275">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="09a33-276">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-276">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="09a33-277">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-277">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="09a33-278">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-278">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="09a33-279">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-279">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="09a33-280">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-280">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="09a33-281">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-281">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="09a33-282">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-282">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="09a33-283">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-283">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="09a33-284">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-284">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="09a33-285">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-285">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="09a33-286">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-286">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="09a33-287">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-287">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="09a33-288">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-288">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="09a33-289">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-289">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="09a33-290">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-290">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="09a33-291">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-291">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="09a33-292">public boolean verticalScrollBarVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-292">public boolean verticalScrollBarVisible(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="09a33-293">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-293">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="09a33-294">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-294">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="09a33-295">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-295">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="09a33-296">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-296">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="09a33-297">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-297">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="09a33-298">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-298">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="09a33-299">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-299">public int viewEditMode(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="09a33-300">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-300">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="09a33-301">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-301">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="09a33-302">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="09a33-302">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="09a33-303">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-303">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="09a33-304">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-304">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="09a33-305">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-305">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="09a33-306">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09a33-306">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="09a33-307">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-307">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="09a33-308">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="09a33-308">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="09a33-309">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-309">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="09a33-310">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="09a33-310">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="09a33-311">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-311">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="09a33-312">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="09a33-312">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="09a33-313">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="09a33-313">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="09a33-314">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-314">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="09a33-315">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="09a33-315">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="09a33-316">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-316">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="09a33-317">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="09a33-317">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="09a33-318">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="09a33-318">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="09a33-319">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-319">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="09a33-320">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="09a33-320">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="09a33-321">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-321">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="09a33-322">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="09a33-322">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="09a33-323">public void paste()</span><span class="sxs-lookup"><span data-stu-id="09a33-323">public void paste()</span></span>                                                                                                 | <span data-ttu-id="09a33-324">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="09a33-324">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="09a33-325">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="09a33-325">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="09a33-326">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-326">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="09a33-327">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="09a33-327">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="09a33-328">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="09a33-328">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="09a33-329">public void context()</span><span class="sxs-lookup"><span data-stu-id="09a33-329">public void context()</span></span>                                                                                               | <span data-ttu-id="09a33-330">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-330">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="09a33-331">public void copy()</span><span class="sxs-lookup"><span data-stu-id="09a33-331">public void copy()</span></span>                                                                                                  | <span data-ttu-id="09a33-332">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="09a33-332">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="09a33-333">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="09a33-333">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="09a33-334">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="09a33-334">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="09a33-335">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="09a33-335">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="09a33-336">public void cut()</span><span class="sxs-lookup"><span data-stu-id="09a33-336">public void cut()</span></span>                                                                                                   | <span data-ttu-id="09a33-337">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="09a33-337">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="09a33-338">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="09a33-338">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="09a33-339">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-339">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="09a33-340">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="09a33-340">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="09a33-341">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-341">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="09a33-342">private void OnTabChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="09a33-342">private void OnTabChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                       |                                                                                                                                                                         |
| <span data-ttu-id="09a33-343">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="09a33-343">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="09a33-344">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="09a33-344">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="09a33-345">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="09a33-345">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="09a33-346">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-346">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="09a33-347">public void tabChanged(int FromTab, int ToTab)</span><span class="sxs-lookup"><span data-stu-id="09a33-347">public void tabChanged(int FromTab, int ToTab)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="09a33-348">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="09a33-348">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="09a33-349">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-349">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |

## <a name="method-addcontrol"></a><span data-ttu-id="09a33-350">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="09a33-350">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="09a33-351">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="09a33-351">Parameters - addControl</span></span>

<span data-ttu-id="09a33-352">controlType</span><span class="sxs-lookup"><span data-stu-id="09a33-352">controlType</span></span>  

<!-- -->

<span data-ttu-id="09a33-353">controlName</span><span class="sxs-lookup"><span data-stu-id="09a33-353">controlName</span></span>  

<!-- -->

<span data-ttu-id="09a33-354">insertAfter</span><span class="sxs-lookup"><span data-stu-id="09a33-354">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="09a33-355">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="09a33-355">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="09a33-356">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="09a33-356">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="09a33-357">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="09a33-357">Parameters - addControlEx</span></span>

<span data-ttu-id="09a33-358">controlClass</span><span class="sxs-lookup"><span data-stu-id="09a33-358">controlClass</span></span>  

<!-- -->

<span data-ttu-id="09a33-359">controlName</span><span class="sxs-lookup"><span data-stu-id="09a33-359">controlName</span></span>  

<!-- -->

<span data-ttu-id="09a33-360">insertAfter</span><span class="sxs-lookup"><span data-stu-id="09a33-360">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="09a33-361">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="09a33-361">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="09a33-362">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="09a33-362">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="09a33-363">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="09a33-363">Parameters - addDataField</span></span>

<span data-ttu-id="09a33-364">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="09a33-364">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="09a33-365">fieldId</span><span class="sxs-lookup"><span data-stu-id="09a33-365">fieldId</span></span>  

<!-- -->

<span data-ttu-id="09a33-366">insertAfter</span><span class="sxs-lookup"><span data-stu-id="09a33-366">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="09a33-367">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="09a33-367">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="09a33-368">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="09a33-368">Return Value - addDataField</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="09a33-369">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="09a33-369">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="09a33-370">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="09a33-370">Parameters - alignChild</span></span>

<span data-ttu-id="09a33-371">値</span><span class="sxs-lookup"><span data-stu-id="09a33-371">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="09a33-372">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="09a33-372">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="09a33-373">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="09a33-373">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="09a33-374">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="09a33-374">Parameters - alignChildren</span></span>

<span data-ttu-id="09a33-375">値</span><span class="sxs-lookup"><span data-stu-id="09a33-375">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="09a33-376">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="09a33-376">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="09a33-377">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="09a33-377">Method alignControl</span></span>

<span data-ttu-id="09a33-378">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-378">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="09a33-379">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="09a33-379">Parameters - alignControl</span></span>

<span data-ttu-id="09a33-380">値</span><span class="sxs-lookup"><span data-stu-id="09a33-380">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="09a33-381">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="09a33-381">Return Value - alignControl</span></span>

<span data-ttu-id="09a33-382">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="09a33-382">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="09a33-383">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="09a33-383">Remarks - alignControl</span></span>

<span data-ttu-id="09a33-384">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-384">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="09a33-385">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="09a33-385">Method allowEdit</span></span>

<span data-ttu-id="09a33-386">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-386">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="09a33-387">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="09a33-387">Parameters - allowEdit</span></span>

<span data-ttu-id="09a33-388">値</span><span class="sxs-lookup"><span data-stu-id="09a33-388">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="09a33-389">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="09a33-389">Return Value - allowEdit</span></span>

<span data-ttu-id="09a33-390">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-390">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="09a33-391">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="09a33-391">Remarks - allowEdit</span></span>

<span data-ttu-id="09a33-392">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="09a33-392">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="09a33-393">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="09a33-393">Method allowSysSetup</span></span>

<span data-ttu-id="09a33-394">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-394">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="09a33-395">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="09a33-395">Return Value - allowSysSetup</span></span>

<span data-ttu-id="09a33-396">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-396">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="09a33-397">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="09a33-397">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="09a33-398">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="09a33-398">Parameters - allowUserSetup</span></span>

<span data-ttu-id="09a33-399">値</span><span class="sxs-lookup"><span data-stu-id="09a33-399">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="09a33-400">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="09a33-400">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="09a33-401">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="09a33-401">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="09a33-402">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="09a33-402">Parameters - arrangeGuide</span></span>

<span data-ttu-id="09a33-403">値</span><span class="sxs-lookup"><span data-stu-id="09a33-403">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="09a33-404">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="09a33-404">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="09a33-405">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="09a33-405">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="09a33-406">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="09a33-406">Parameters - arrangeMethod</span></span>

<span data-ttu-id="09a33-407">値</span><span class="sxs-lookup"><span data-stu-id="09a33-407">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="09a33-408">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="09a33-408">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="09a33-409">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="09a33-409">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="09a33-410">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="09a33-410">Parameters - arrangeWhen</span></span>

<span data-ttu-id="09a33-411">値</span><span class="sxs-lookup"><span data-stu-id="09a33-411">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="09a33-412">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="09a33-412">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="09a33-413">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="09a33-413">Method autoDeclaration</span></span>

<span data-ttu-id="09a33-414">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-414">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="09a33-415">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="09a33-415">Parameters - autoDeclaration</span></span>

<span data-ttu-id="09a33-416">値</span><span class="sxs-lookup"><span data-stu-id="09a33-416">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="09a33-417">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="09a33-417">Return Value - autoDeclaration</span></span>

<span data-ttu-id="09a33-418">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-418">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="09a33-419">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="09a33-419">Remarks - autoDeclaration</span></span>

<span data-ttu-id="09a33-420">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="09a33-420">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="09a33-421">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="09a33-421">Method backgroundColor</span></span>

<span data-ttu-id="09a33-422">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-422">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="09a33-423">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="09a33-423">Parameters - backgroundColor</span></span>

<span data-ttu-id="09a33-424">値</span><span class="sxs-lookup"><span data-stu-id="09a33-424">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="09a33-425">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="09a33-425">Return Value - backgroundColor</span></span>

<span data-ttu-id="09a33-426">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="09a33-426">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="09a33-427">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="09a33-427">Remarks - backgroundColor</span></span>

<span data-ttu-id="09a33-428">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="09a33-428">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="09a33-429">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="09a33-429">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="09a33-430">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="09a33-430">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="09a33-431">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="09a33-431">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="09a33-432">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="09a33-432">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="09a33-433">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="09a33-433">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="09a33-434">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="09a33-434">Method backStyle</span></span>

<span data-ttu-id="09a33-435">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-435">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="09a33-436">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="09a33-436">Parameters - backStyle</span></span>

<span data-ttu-id="09a33-437">値</span><span class="sxs-lookup"><span data-stu-id="09a33-437">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="09a33-438">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="09a33-438">Return Value - backStyle</span></span>

<span data-ttu-id="09a33-439">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="09a33-439">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="09a33-440">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="09a33-440">Method beginDrag</span></span>

<span data-ttu-id="09a33-441">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-441">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="09a33-442">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="09a33-442">Parameters - beginDrag</span></span>

<span data-ttu-id="09a33-443">x</span><span class="sxs-lookup"><span data-stu-id="09a33-443">x</span></span>  
<span data-ttu-id="09a33-444">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-444">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="09a33-445">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="09a33-445">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="09a33-446">y</span><span class="sxs-lookup"><span data-stu-id="09a33-446">y</span></span>  
<span data-ttu-id="09a33-447">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-447">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="09a33-448">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="09a33-448">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="09a33-449">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="09a33-449">Return Value - beginDrag</span></span>

<span data-ttu-id="09a33-450">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="09a33-450">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="09a33-451">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="09a33-451">Remarks - beginDrag</span></span>

<span data-ttu-id="09a33-452">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="09a33-452">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="09a33-453">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="09a33-453">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="09a33-454">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-454">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="09a33-455">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-455">Parameters - bottomMargin</span></span>

<span data-ttu-id="09a33-456">値</span><span class="sxs-lookup"><span data-stu-id="09a33-456">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-457">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-457">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="09a33-458">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-458">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="09a33-459">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-459">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="09a33-460">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-460">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="09a33-461">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-461">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="09a33-462">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-462">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="09a33-463">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-463">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="09a33-464">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-464">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="09a33-465">値</span><span class="sxs-lookup"><span data-stu-id="09a33-465">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="09a33-466">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-466">Return Value - bottomMarginValue</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="09a33-467">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="09a33-467">Method calcControlSize</span></span>

<span data-ttu-id="09a33-468">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-468">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="09a33-469">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="09a33-469">Parameters - calcControlSize</span></span>

<span data-ttu-id="09a33-470">chars</span><span class="sxs-lookup"><span data-stu-id="09a33-470">chars</span></span>  
<span data-ttu-id="09a33-471">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="09a33-471">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="09a33-472">明細行</span><span class="sxs-lookup"><span data-stu-id="09a33-472">lines</span></span>  
<span data-ttu-id="09a33-473">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="09a33-473">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="09a33-474">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="09a33-474">Return Value - calcControlSize</span></span>

<span data-ttu-id="09a33-475">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="09a33-475">The container that holds the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="09a33-476">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="09a33-476">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="09a33-477">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="09a33-477">Parameters - canAddDataField</span></span>

<span data-ttu-id="09a33-478">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="09a33-478">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="09a33-479">fieldId</span><span class="sxs-lookup"><span data-stu-id="09a33-479">fieldId</span></span>  

<!-- -->

<span data-ttu-id="09a33-480">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="09a33-480">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="09a33-481">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="09a33-481">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="09a33-482">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="09a33-482">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="09a33-483">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="09a33-483">Parameters - canContain</span></span>

<span data-ttu-id="09a33-484">control</span><span class="sxs-lookup"><span data-stu-id="09a33-484">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="09a33-485">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="09a33-485">Return Value - canContain</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="09a33-486">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="09a33-486">Method colorScheme</span></span>

<span data-ttu-id="09a33-487">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-487">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="09a33-488">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="09a33-488">Parameters - colorScheme</span></span>

<span data-ttu-id="09a33-489">値</span><span class="sxs-lookup"><span data-stu-id="09a33-489">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="09a33-490">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="09a33-490">Return Value - colorScheme</span></span>

<span data-ttu-id="09a33-491">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="09a33-491">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="09a33-492">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="09a33-492">Remarks - colorScheme</span></span>

<span data-ttu-id="09a33-493">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-493">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="09a33-494">金額</span><span class="sxs-lookup"><span data-stu-id="09a33-494">Value</span></span> | <span data-ttu-id="09a33-495">スタイル</span><span class="sxs-lookup"><span data-stu-id="09a33-495">Style</span></span>                        |
|-------|------------------------------|
| <span data-ttu-id="09a33-496">0</span><span class="sxs-lookup"><span data-stu-id="09a33-496">0</span></span>     | <span data-ttu-id="09a33-497">既定</span><span class="sxs-lookup"><span data-stu-id="09a33-497">Default</span></span>                      |
| <span data-ttu-id="09a33-498">1</span><span class="sxs-lookup"><span data-stu-id="09a33-498">1</span></span>     | <span data-ttu-id="09a33-499">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="09a33-499">The Microsoft Windows palette</span></span> |
| <span data-ttu-id="09a33-500">2</span><span class="sxs-lookup"><span data-stu-id="09a33-500">2</span></span>     | <span data-ttu-id="09a33-501">真の配色</span><span class="sxs-lookup"><span data-stu-id="09a33-501">The true-color scheme</span></span>        |

## <a name="method-columns"></a><span data-ttu-id="09a33-502">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="09a33-502">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="09a33-503">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="09a33-503">Parameters - columns</span></span>

<span data-ttu-id="09a33-504">値</span><span class="sxs-lookup"><span data-stu-id="09a33-504">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-505">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-505">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="09a33-506">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="09a33-506">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="09a33-507">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="09a33-507">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="09a33-508">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="09a33-508">Parameters - columnsMode</span></span>

<span data-ttu-id="09a33-509">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-509">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="09a33-510">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="09a33-510">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="09a33-511">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="09a33-511">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="09a33-512">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="09a33-512">Parameters - columnspace</span></span>

<span data-ttu-id="09a33-513">値</span><span class="sxs-lookup"><span data-stu-id="09a33-513">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-514">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-514">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="09a33-515">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="09a33-515">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="09a33-516">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="09a33-516">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="09a33-517">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="09a33-517">Parameters - columnspaceMode</span></span>

<span data-ttu-id="09a33-518">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-518">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="09a33-519">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="09a33-519">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="09a33-520">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="09a33-520">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="09a33-521">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="09a33-521">Parameters - columnspaceValue</span></span>

<span data-ttu-id="09a33-522">値</span><span class="sxs-lookup"><span data-stu-id="09a33-522">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="09a33-523">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="09a33-523">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="09a33-524">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="09a33-524">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="09a33-525">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="09a33-525">Parameters - columnsValue</span></span>

<span data-ttu-id="09a33-526">値</span><span class="sxs-lookup"><span data-stu-id="09a33-526">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="09a33-527">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="09a33-527">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="09a33-528">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="09a33-528">Method configurationKey</span></span>

<span data-ttu-id="09a33-529">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-529">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="09a33-530">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="09a33-530">Parameters - configurationKey</span></span>

<span data-ttu-id="09a33-531">値</span><span class="sxs-lookup"><span data-stu-id="09a33-531">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="09a33-532">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="09a33-532">Return Value - configurationKey</span></span>

<span data-ttu-id="09a33-533">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="09a33-533">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="09a33-534">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="09a33-534">Remarks - configurationKey</span></span>

<span data-ttu-id="09a33-535">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-535">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="09a33-536">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="09a33-536">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="09a33-537">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="09a33-537">Method configurationKeyEx</span></span>

<span data-ttu-id="09a33-538">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-538">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="09a33-539">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="09a33-539">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="09a33-540">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="09a33-540">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="09a33-541">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="09a33-541">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="09a33-542">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="09a33-542">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="09a33-543">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="09a33-543">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="09a33-544">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="09a33-544">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-containerscrollhorizontaloffset"></a><span data-ttu-id="09a33-545">メソッド containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="09a33-545">Method containerScrollHorizontalOffset</span></span>

```xpp
public int containerScrollHorizontalOffset([int value])
```

### <a name="parameters---containerscrollhorizontaloffset"></a><span data-ttu-id="09a33-546">パラメーター - containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="09a33-546">Parameters - containerScrollHorizontalOffset</span></span>

<span data-ttu-id="09a33-547">値</span><span class="sxs-lookup"><span data-stu-id="09a33-547">value</span></span>  

### <a name="return-value---containerscrollhorizontaloffset"></a><span data-ttu-id="09a33-548">戻り値 - containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="09a33-548">Return Value - containerScrollHorizontalOffset</span></span>

## <a name="method-containerscrollverticaloffset"></a><span data-ttu-id="09a33-549">メソッド containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="09a33-549">Method containerScrollVerticalOffset</span></span>

```xpp
public int containerScrollVerticalOffset([int value])
```

### <a name="parameters---containerscrollverticaloffset"></a><span data-ttu-id="09a33-550">パラメーター - containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="09a33-550">Parameters - containerScrollVerticalOffset</span></span>

<span data-ttu-id="09a33-551">値</span><span class="sxs-lookup"><span data-stu-id="09a33-551">value</span></span>  

### <a name="return-value---containerscrollverticaloffset"></a><span data-ttu-id="09a33-552">戻り値 - containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="09a33-552">Return Value - containerScrollVerticalOffset</span></span>

## <a name="method-contains"></a><span data-ttu-id="09a33-553">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="09a33-553">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="09a33-554">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="09a33-554">Parameters - contains</span></span>

<span data-ttu-id="09a33-555">control</span><span class="sxs-lookup"><span data-stu-id="09a33-555">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="09a33-556">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="09a33-556">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="09a33-557">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="09a33-557">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="09a33-558">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="09a33-558">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="09a33-559">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="09a33-559">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="09a33-560">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="09a33-560">Parameters - controlNum</span></span>

<span data-ttu-id="09a33-561">controlNo</span><span class="sxs-lookup"><span data-stu-id="09a33-561">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="09a33-562">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="09a33-562">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="09a33-563">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="09a33-563">Method countryRegionCodes</span></span>

<span data-ttu-id="09a33-564">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-564">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="09a33-565">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="09a33-565">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="09a33-566">値</span><span class="sxs-lookup"><span data-stu-id="09a33-566">value</span></span>  
<span data-ttu-id="09a33-567">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-567">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="09a33-568">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="09a33-568">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="09a33-569">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="09a33-569">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="09a33-570">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="09a33-570">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="09a33-571">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="09a33-571">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="09a33-572">値</span><span class="sxs-lookup"><span data-stu-id="09a33-572">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="09a33-573">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="09a33-573">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="09a33-574">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="09a33-574">Method dataRelationPath</span></span>

<span data-ttu-id="09a33-575">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-575">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="09a33-576">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="09a33-576">Parameters - dataRelationPath</span></span>

<span data-ttu-id="09a33-577">値</span><span class="sxs-lookup"><span data-stu-id="09a33-577">value</span></span>  
<span data-ttu-id="09a33-578">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-578">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="09a33-579">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="09a33-579">Return Value - dataRelationPath</span></span>

<span data-ttu-id="09a33-580">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="09a33-580">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="09a33-581">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="09a33-581">Remarks - dataRelationPath</span></span>

<span data-ttu-id="09a33-582">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="09a33-582">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="09a33-583">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="09a33-583">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="09a33-584">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="09a33-584">Method dataSource</span></span>

<span data-ttu-id="09a33-585">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-585">Gets or sets a data source that is used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="09a33-586">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="09a33-586">Parameters - dataSource</span></span>

<span data-ttu-id="09a33-587">値</span><span class="sxs-lookup"><span data-stu-id="09a33-587">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="09a33-588">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="09a33-588">Return Value - dataSource</span></span>

<span data-ttu-id="09a33-589">使用するデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="09a33-589">The ID of the data source to use.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="09a33-590">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="09a33-590">Method displayTarget</span></span>

<span data-ttu-id="09a33-591">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-591">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="09a33-592">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="09a33-592">Parameters - displayTarget</span></span>

<span data-ttu-id="09a33-593">値</span><span class="sxs-lookup"><span data-stu-id="09a33-593">value</span></span>  
<span data-ttu-id="09a33-594">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-594">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="09a33-595">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="09a33-595">Return Value - displayTarget</span></span>

<span data-ttu-id="09a33-596">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="09a33-596">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="09a33-597">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="09a33-597">Method dragDrop</span></span>

<span data-ttu-id="09a33-598">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-598">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="09a33-599">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="09a33-599">Parameters - dragDrop</span></span>

<span data-ttu-id="09a33-600">値</span><span class="sxs-lookup"><span data-stu-id="09a33-600">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="09a33-601">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="09a33-601">Return Value - dragDrop</span></span>

<span data-ttu-id="09a33-602">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="09a33-602">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="09a33-603">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="09a33-603">Method dragOver</span></span>

<span data-ttu-id="09a33-604">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-604">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="09a33-605">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="09a33-605">Parameters - dragOver</span></span>

<span data-ttu-id="09a33-606">dragSource</span><span class="sxs-lookup"><span data-stu-id="09a33-606">dragSource</span></span>  
<span data-ttu-id="09a33-607">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-607">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-608">dragMode</span><span class="sxs-lookup"><span data-stu-id="09a33-608">dragMode</span></span>  
<span data-ttu-id="09a33-609">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-609">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-610">x</span><span class="sxs-lookup"><span data-stu-id="09a33-610">x</span></span>  
<span data-ttu-id="09a33-611">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-611">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-612">y</span><span class="sxs-lookup"><span data-stu-id="09a33-612">y</span></span>  
<span data-ttu-id="09a33-613">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-613">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="09a33-614">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="09a33-614">Return Value - dragOver</span></span>

<span data-ttu-id="09a33-615">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="09a33-615">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="09a33-616">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="09a33-616">Method dragOverEx</span></span>

<span data-ttu-id="09a33-617">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-617">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="09a33-618">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="09a33-618">Parameters - dragOverEx</span></span>

<span data-ttu-id="09a33-619">dragSource</span><span class="sxs-lookup"><span data-stu-id="09a33-619">dragSource</span></span>  
<span data-ttu-id="09a33-620">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-620">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-621">dragMode</span><span class="sxs-lookup"><span data-stu-id="09a33-621">dragMode</span></span>  
<span data-ttu-id="09a33-622">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-622">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-623">x</span><span class="sxs-lookup"><span data-stu-id="09a33-623">x</span></span>  
<span data-ttu-id="09a33-624">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-624">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-625">y</span><span class="sxs-lookup"><span data-stu-id="09a33-625">y</span></span>  
<span data-ttu-id="09a33-626">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-626">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="09a33-627">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="09a33-627">Return Value - dragOverEx</span></span>

<span data-ttu-id="09a33-628">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="09a33-628">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="09a33-629">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="09a33-629">Method dragText</span></span>

<span data-ttu-id="09a33-630">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-630">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="09a33-631">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="09a33-631">Return Value - dragText</span></span>

<span data-ttu-id="09a33-632">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="09a33-632">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="09a33-633">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="09a33-633">Method enabled</span></span>

<span data-ttu-id="09a33-634">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-634">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="09a33-635">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="09a33-635">Parameters - enabled</span></span>

<span data-ttu-id="09a33-636">値</span><span class="sxs-lookup"><span data-stu-id="09a33-636">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="09a33-637">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="09a33-637">Return Value - enabled</span></span>

<span data-ttu-id="09a33-638">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-638">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="09a33-639">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="09a33-639">Remarks - enabled</span></span>

<span data-ttu-id="09a33-640">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="09a33-640">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="09a33-641">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="09a33-641">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="09a33-642">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="09a33-642">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-getactivepage"></a><span data-ttu-id="09a33-643">メソッド getActivePage</span><span class="sxs-lookup"><span data-stu-id="09a33-643">Method getActivePage</span></span>

```xpp
public FormControl getActivePage()
```

### <a name="return-value---getactivepage"></a><span data-ttu-id="09a33-644">戻り値 - getActivePage</span><span class="sxs-lookup"><span data-stu-id="09a33-644">Return Value - getActivePage</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="09a33-645">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="09a33-645">Method hasChanged</span></span>

<span data-ttu-id="09a33-646">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-646">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="09a33-647">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="09a33-647">Parameters - hasChanged</span></span>

<span data-ttu-id="09a33-648">val</span><span class="sxs-lookup"><span data-stu-id="09a33-648">val</span></span>  
<span data-ttu-id="09a33-649">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-649">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="09a33-650">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="09a33-650">Return Value - hasChanged</span></span>

<span data-ttu-id="09a33-651">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-651">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hascontrolpositionoverride"></a><span data-ttu-id="09a33-652">メソッド hasControlPositionOverride</span><span class="sxs-lookup"><span data-stu-id="09a33-652">Method hasControlPositionOverride</span></span>

```xpp
public boolean hasControlPositionOverride()
```

### <a name="return-value---hascontrolpositionoverride"></a><span data-ttu-id="09a33-653">戻り値 - hasControlPositionOverride</span><span class="sxs-lookup"><span data-stu-id="09a33-653">Return Value - hasControlPositionOverride</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="09a33-654">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="09a33-654">Method hasUserSetting</span></span>

<span data-ttu-id="09a33-655">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-655">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="09a33-656">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="09a33-656">Return Value - hasUserSetting</span></span>

<span data-ttu-id="09a33-657">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-657">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="09a33-658">メソッド height</span><span class="sxs-lookup"><span data-stu-id="09a33-658">Method height</span></span>

<span data-ttu-id="09a33-659">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-659">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="09a33-660">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="09a33-660">Parameters - height</span></span>

<span data-ttu-id="09a33-661">値</span><span class="sxs-lookup"><span data-stu-id="09a33-661">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-662">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-662">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="09a33-663">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="09a33-663">Return Value - height</span></span>

<span data-ttu-id="09a33-664">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="09a33-664">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="09a33-665">備考 - height</span><span class="sxs-lookup"><span data-stu-id="09a33-665">Remarks - height</span></span>

<span data-ttu-id="09a33-666">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-666">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="09a33-667">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="09a33-667">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="09a33-668">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-668">Mode</span></span>            | <span data-ttu-id="09a33-669">高さの計算</span><span class="sxs-lookup"><span data-stu-id="09a33-669">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a33-670">-1 正確</span><span class="sxs-lookup"><span data-stu-id="09a33-670">-1 Exact</span></span>        | <span data-ttu-id="09a33-671">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-671">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="09a33-672">0 自動</span><span class="sxs-lookup"><span data-stu-id="09a33-672">0 Auto</span></span>          | <span data-ttu-id="09a33-673">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-673">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="09a33-674">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="09a33-674">1 Column height</span></span> | <span data-ttu-id="09a33-675">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="09a33-675">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="09a33-676">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="09a33-676">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="09a33-677">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="09a33-677">Method heightMode</span></span>

<span data-ttu-id="09a33-678">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-678">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="09a33-679">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="09a33-679">Parameters - heightMode</span></span>

<span data-ttu-id="09a33-680">値</span><span class="sxs-lookup"><span data-stu-id="09a33-680">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="09a33-681">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="09a33-681">Return Value - heightMode</span></span>

<span data-ttu-id="09a33-682">計算モード。</span><span class="sxs-lookup"><span data-stu-id="09a33-682">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="09a33-683">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="09a33-683">Remarks - heightMode</span></span>

<span data-ttu-id="09a33-684">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="09a33-684">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="09a33-685">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-685">Mode</span></span>          | <span data-ttu-id="09a33-686">高さの計算</span><span class="sxs-lookup"><span data-stu-id="09a33-686">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a33-687">正確</span><span class="sxs-lookup"><span data-stu-id="09a33-687">Exact</span></span>         | <span data-ttu-id="09a33-688">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-688">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="09a33-689">自動</span><span class="sxs-lookup"><span data-stu-id="09a33-689">Auto</span></span>          | <span data-ttu-id="09a33-690">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-690">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="09a33-691">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="09a33-691">Column height</span></span> | <span data-ttu-id="09a33-692">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="09a33-692">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="09a33-693">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="09a33-693">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="09a33-694">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="09a33-694">Method heightValue</span></span>

<span data-ttu-id="09a33-695">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-695">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="09a33-696">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="09a33-696">Parameters - heightValue</span></span>

<span data-ttu-id="09a33-697">値</span><span class="sxs-lookup"><span data-stu-id="09a33-697">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="09a33-698">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="09a33-698">Return Value - heightValue</span></span>

<span data-ttu-id="09a33-699">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="09a33-699">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="09a33-700">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="09a33-700">Remarks - heightValue</span></span>

<span data-ttu-id="09a33-701">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="09a33-701">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="09a33-702">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="09a33-702">Method helpField</span></span>

<span data-ttu-id="09a33-703">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-703">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="09a33-704">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="09a33-704">Return Value - helpField</span></span>

<span data-ttu-id="09a33-705">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="09a33-705">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="09a33-706">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="09a33-706">Remarks - helpField</span></span>

<span data-ttu-id="09a33-707">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="09a33-707">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="09a33-708">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="09a33-708">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="09a33-709">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="09a33-709">Method helpText</span></span>

<span data-ttu-id="09a33-710">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-710">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="09a33-711">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="09a33-711">Parameters - helpText</span></span>

<span data-ttu-id="09a33-712">値</span><span class="sxs-lookup"><span data-stu-id="09a33-712">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="09a33-713">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="09a33-713">Return Value - helpText</span></span>

<span data-ttu-id="09a33-714">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="09a33-714">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="09a33-715">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="09a33-715">Remarks - helpText</span></span>

<span data-ttu-id="09a33-716">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-716">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="09a33-717">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="09a33-717">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="09a33-718">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="09a33-718">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="09a33-719">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="09a33-719">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="09a33-720">値</span><span class="sxs-lookup"><span data-stu-id="09a33-720">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="09a33-721">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="09a33-721">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="09a33-722">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="09a33-722">Method hierarchyParent</span></span>

<span data-ttu-id="09a33-723">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-723">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="09a33-724">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="09a33-724">Parameters - hierarchyParent</span></span>

<span data-ttu-id="09a33-725">値</span><span class="sxs-lookup"><span data-stu-id="09a33-725">value</span></span>  
<span data-ttu-id="09a33-726">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="09a33-726">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="09a33-727">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="09a33-727">Return Value - hierarchyParent</span></span>

<span data-ttu-id="09a33-728">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="09a33-728">The HierarchyParent property value of the control.</span></span>

## <a name="method-horizontalscrollbarvisible"></a><span data-ttu-id="09a33-729">メソッド horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="09a33-729">Method horizontalScrollBarVisible</span></span>

```xpp
public boolean horizontalScrollBarVisible([boolean value])
```

### <a name="parameters---horizontalscrollbarvisible"></a><span data-ttu-id="09a33-730">パラメーター - horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="09a33-730">Parameters - horizontalScrollBarVisible</span></span>

<span data-ttu-id="09a33-731">値</span><span class="sxs-lookup"><span data-stu-id="09a33-731">value</span></span>  

### <a name="return-value---horizontalscrollbarvisible"></a><span data-ttu-id="09a33-732">戻り値 - horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="09a33-732">Return Value - horizontalScrollBarVisible</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="09a33-733">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="09a33-733">Method hWnd</span></span>

<span data-ttu-id="09a33-734">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-734">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="09a33-735">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="09a33-735">Return Value - hWnd</span></span>

<span data-ttu-id="09a33-736">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="09a33-736">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="09a33-737">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="09a33-737">Remarks - hWnd</span></span>

<span data-ttu-id="09a33-738">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="09a33-738">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="09a33-739">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="09a33-739">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="09a33-740">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="09a33-740">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="09a33-741">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="09a33-741">Method isDisplayed</span></span>

<span data-ttu-id="09a33-742">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-742">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="09a33-743">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="09a33-743">Return Value - isDisplayed</span></span>

<span data-ttu-id="09a33-744">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="09a33-744">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="09a33-745">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="09a33-745">Remarks - isDisplayed</span></span>

<span data-ttu-id="09a33-746">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="09a33-746">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="09a33-747">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="09a33-747">Method isRestricted</span></span>

<span data-ttu-id="09a33-748">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-748">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="09a33-749">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="09a33-749">Return Value - isRestricted</span></span>

<span data-ttu-id="09a33-750">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="09a33-750">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="09a33-751">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="09a33-751">Method isUserSetupEnabled</span></span>

<span data-ttu-id="09a33-752">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-752">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="09a33-753">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="09a33-753">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="09a33-754">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="09a33-754">neededSetupRights</span></span>  
<span data-ttu-id="09a33-755">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="09a33-755">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="09a33-756">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="09a33-756">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="09a33-757">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-757">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="09a33-758">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="09a33-758">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="09a33-759">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="09a33-759">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a33-760">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="09a33-760">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="09a33-761">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="09a33-761">No changes can be made to the control.</span></span> <span data-ttu-id="09a33-762">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-762">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="09a33-763">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="09a33-763">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="09a33-764">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="09a33-764">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="09a33-765">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="09a33-765">The user cannot move the control.</span></span>   |
| <span data-ttu-id="09a33-766">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="09a33-766">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="09a33-767">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="09a33-767">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="09a33-768">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="09a33-768">The user can also move the control.</span></span> |

<span data-ttu-id="09a33-769">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="09a33-769">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-left"></a><span data-ttu-id="09a33-770">メソッド left</span><span class="sxs-lookup"><span data-stu-id="09a33-770">Method left</span></span>

<span data-ttu-id="09a33-771">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-771">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="09a33-772">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="09a33-772">Parameters - left</span></span>

<span data-ttu-id="09a33-773">値</span><span class="sxs-lookup"><span data-stu-id="09a33-773">value</span></span>  
<span data-ttu-id="09a33-774">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-774">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="09a33-775">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-775">mode</span></span>  
<span data-ttu-id="09a33-776">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-776">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="09a33-777">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="09a33-777">Return Value - left</span></span>

<span data-ttu-id="09a33-778">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="09a33-778">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="09a33-779">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-779">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="09a33-780">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-780">Parameters - leftMargin</span></span>

<span data-ttu-id="09a33-781">値</span><span class="sxs-lookup"><span data-stu-id="09a33-781">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-782">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-782">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="09a33-783">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-783">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="09a33-784">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-784">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="09a33-785">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-785">Parameters - leftMarginMode</span></span>

<span data-ttu-id="09a33-786">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-786">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="09a33-787">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-787">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="09a33-788">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-788">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="09a33-789">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-789">Parameters - leftMarginValue</span></span>

<span data-ttu-id="09a33-790">値</span><span class="sxs-lookup"><span data-stu-id="09a33-790">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="09a33-791">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-791">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="09a33-792">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="09a33-792">Method leftMode</span></span>

<span data-ttu-id="09a33-793">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-793">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="09a33-794">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="09a33-794">Parameters - leftMode</span></span>

<span data-ttu-id="09a33-795">値</span><span class="sxs-lookup"><span data-stu-id="09a33-795">value</span></span>  
<span data-ttu-id="09a33-796">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-796">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="09a33-797">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="09a33-797">Return Value - leftMode</span></span>

<span data-ttu-id="09a33-798">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="09a33-798">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="09a33-799">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="09a33-799">Method leftValue</span></span>

<span data-ttu-id="09a33-800">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-800">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="09a33-801">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="09a33-801">Parameters - leftValue</span></span>

<span data-ttu-id="09a33-802">値</span><span class="sxs-lookup"><span data-stu-id="09a33-802">value</span></span>  
<span data-ttu-id="09a33-803">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-803">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="09a33-804">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="09a33-804">Return Value - leftValue</span></span>

<span data-ttu-id="09a33-805">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="09a33-805">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="09a33-806">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="09a33-806">Method markAsUserAdd</span></span>

<span data-ttu-id="09a33-807">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="09a33-807">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="09a33-808">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="09a33-808">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="09a33-809">値</span><span class="sxs-lookup"><span data-stu-id="09a33-809">value</span></span>  
<span data-ttu-id="09a33-810">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-810">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="09a33-811">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="09a33-811">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="09a33-812">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-812">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="09a33-813">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="09a33-813">Method mouseDblClick</span></span>

<span data-ttu-id="09a33-814">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-814">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="09a33-815">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="09a33-815">Parameters - mouseDblClick</span></span>

<span data-ttu-id="09a33-816">x</span><span class="sxs-lookup"><span data-stu-id="09a33-816">x</span></span>  
<span data-ttu-id="09a33-817">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-817">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-818">y</span><span class="sxs-lookup"><span data-stu-id="09a33-818">y</span></span>  
<span data-ttu-id="09a33-819">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-819">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-820">ボタン</span><span class="sxs-lookup"><span data-stu-id="09a33-820">button</span></span>  
<span data-ttu-id="09a33-821">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-821">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-822">Ctrl</span><span class="sxs-lookup"><span data-stu-id="09a33-822">Ctrl</span></span>  
<span data-ttu-id="09a33-823">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-823">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-824">シフト</span><span class="sxs-lookup"><span data-stu-id="09a33-824">Shift</span></span>  
<span data-ttu-id="09a33-825">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-825">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="09a33-826">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="09a33-826">Return Value - mouseDblClick</span></span>

<span data-ttu-id="09a33-827">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="09a33-827">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="09a33-828">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="09a33-828">Remarks - mouseDblClick</span></span>

<span data-ttu-id="09a33-829">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-829">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="09a33-830">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="09a33-830">Method mouseDown</span></span>

<span data-ttu-id="09a33-831">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-831">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="09a33-832">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="09a33-832">Parameters - mouseDown</span></span>

<span data-ttu-id="09a33-833">x</span><span class="sxs-lookup"><span data-stu-id="09a33-833">x</span></span>  
<span data-ttu-id="09a33-834">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-834">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-835">y</span><span class="sxs-lookup"><span data-stu-id="09a33-835">y</span></span>  
<span data-ttu-id="09a33-836">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-836">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-837">ボタン</span><span class="sxs-lookup"><span data-stu-id="09a33-837">button</span></span>  
<span data-ttu-id="09a33-838">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-838">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-839">Ctrl</span><span class="sxs-lookup"><span data-stu-id="09a33-839">Ctrl</span></span>  
<span data-ttu-id="09a33-840">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-840">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-841">シフト</span><span class="sxs-lookup"><span data-stu-id="09a33-841">Shift</span></span>  
<span data-ttu-id="09a33-842">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-842">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="09a33-843">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="09a33-843">Return Value - mouseDown</span></span>

<span data-ttu-id="09a33-844">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="09a33-844">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="09a33-845">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="09a33-845">Remarks - mouseDown</span></span>

<span data-ttu-id="09a33-846">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-846">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="09a33-847">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-847">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="09a33-848">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="09a33-848">Method mouseMove</span></span>

<span data-ttu-id="09a33-849">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-849">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="09a33-850">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="09a33-850">Parameters - mouseMove</span></span>

<span data-ttu-id="09a33-851">x</span><span class="sxs-lookup"><span data-stu-id="09a33-851">x</span></span>  
<span data-ttu-id="09a33-852">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-852">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-853">y</span><span class="sxs-lookup"><span data-stu-id="09a33-853">y</span></span>  
<span data-ttu-id="09a33-854">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-854">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-855">ボタン</span><span class="sxs-lookup"><span data-stu-id="09a33-855">button</span></span>  
<span data-ttu-id="09a33-856">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-856">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-857">Ctrl</span><span class="sxs-lookup"><span data-stu-id="09a33-857">Ctrl</span></span>  
<span data-ttu-id="09a33-858">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-858">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-859">シフト</span><span class="sxs-lookup"><span data-stu-id="09a33-859">Shift</span></span>  
<span data-ttu-id="09a33-860">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-860">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="09a33-861">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="09a33-861">Return Value - mouseMove</span></span>

<span data-ttu-id="09a33-862">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="09a33-862">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="09a33-863">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="09a33-863">Remarks - mouseMove</span></span>

<span data-ttu-id="09a33-864">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-864">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="09a33-865">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="09a33-865">Method mouseUp</span></span>

<span data-ttu-id="09a33-866">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-866">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="09a33-867">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="09a33-867">Parameters - mouseUp</span></span>

<span data-ttu-id="09a33-868">x</span><span class="sxs-lookup"><span data-stu-id="09a33-868">x</span></span>  
<span data-ttu-id="09a33-869">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-869">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-870">y</span><span class="sxs-lookup"><span data-stu-id="09a33-870">y</span></span>  
<span data-ttu-id="09a33-871">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-871">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-872">ボタン</span><span class="sxs-lookup"><span data-stu-id="09a33-872">button</span></span>  
<span data-ttu-id="09a33-873">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-873">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-874">Ctrl</span><span class="sxs-lookup"><span data-stu-id="09a33-874">Ctrl</span></span>  
<span data-ttu-id="09a33-875">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-875">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-876">シフト</span><span class="sxs-lookup"><span data-stu-id="09a33-876">Shift</span></span>  
<span data-ttu-id="09a33-877">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-877">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="09a33-878">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="09a33-878">Return Value - mouseUp</span></span>

<span data-ttu-id="09a33-879">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="09a33-879">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="09a33-880">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="09a33-880">Remarks - mouseUp</span></span>

<span data-ttu-id="09a33-881">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-881">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="09a33-882">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-882">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="09a33-883">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="09a33-883">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="09a33-884">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="09a33-884">Parameters - moveControl</span></span>

<span data-ttu-id="09a33-885">controlId</span><span class="sxs-lookup"><span data-stu-id="09a33-885">controlId</span></span>  

<!-- -->

<span data-ttu-id="09a33-886">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="09a33-886">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="09a33-887">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="09a33-887">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="09a33-888">メソッド名</span><span class="sxs-lookup"><span data-stu-id="09a33-888">Method name</span></span>

<span data-ttu-id="09a33-889">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-889">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="09a33-890">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="09a33-890">Parameters - name</span></span>

<span data-ttu-id="09a33-891">値</span><span class="sxs-lookup"><span data-stu-id="09a33-891">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="09a33-892">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="09a33-892">Return Value - name</span></span>

<span data-ttu-id="09a33-893">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="09a33-893">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="09a33-894">備考 - name</span><span class="sxs-lookup"><span data-stu-id="09a33-894">Remarks - name</span></span>

<span data-ttu-id="09a33-895">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="09a33-895">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="09a33-896">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="09a33-896">Begins with a letter.</span></span>
-   <span data-ttu-id="09a33-897">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="09a33-897">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="09a33-898">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="09a33-898">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="09a33-899">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="09a33-899">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="09a33-900">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="09a33-900">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="09a33-901">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="09a33-901">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="09a33-902">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="09a33-902">Parameters - neededPermission</span></span>

<span data-ttu-id="09a33-903">値</span><span class="sxs-lookup"><span data-stu-id="09a33-903">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="09a33-904">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="09a33-904">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="09a33-905">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="09a33-905">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="09a33-906">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="09a33-906">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="09a33-907">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="09a33-907">Method parentControl</span></span>

<span data-ttu-id="09a33-908">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-908">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="09a33-909">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="09a33-909">Return Value - parentControl</span></span>

<span data-ttu-id="09a33-910">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="09a33-910">The parent control for the control.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="09a33-911">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-911">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="09a33-912">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-912">Parameters - rightMargin</span></span>

<span data-ttu-id="09a33-913">値</span><span class="sxs-lookup"><span data-stu-id="09a33-913">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-914">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-914">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="09a33-915">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-915">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="09a33-916">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-916">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="09a33-917">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-917">Parameters - rightMarginMode</span></span>

<span data-ttu-id="09a33-918">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-918">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="09a33-919">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-919">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="09a33-920">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-920">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="09a33-921">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-921">Parameters - rightMarginValue</span></span>

<span data-ttu-id="09a33-922">値</span><span class="sxs-lookup"><span data-stu-id="09a33-922">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="09a33-923">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-923">Return Value - rightMarginValue</span></span>

## <a name="method-scrollbars"></a><span data-ttu-id="09a33-924">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="09a33-924">Method scrollbars</span></span>

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a><span data-ttu-id="09a33-925">パラメーター - scrollbars</span><span class="sxs-lookup"><span data-stu-id="09a33-925">Parameters - scrollbars</span></span>

<span data-ttu-id="09a33-926">値</span><span class="sxs-lookup"><span data-stu-id="09a33-926">value</span></span>  

### <a name="return-value---scrollbars"></a><span data-ttu-id="09a33-927">戻り値 - scrollbars</span><span class="sxs-lookup"><span data-stu-id="09a33-927">Return Value - scrollbars</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="09a33-928">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="09a33-928">Method securityKey</span></span>

<span data-ttu-id="09a33-929">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-929">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="09a33-930">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="09a33-930">Parameters - securityKey</span></span>

<span data-ttu-id="09a33-931">値</span><span class="sxs-lookup"><span data-stu-id="09a33-931">value</span></span>  
<span data-ttu-id="09a33-932">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-932">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="09a33-933">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="09a33-933">Return Value - securityKey</span></span>

<span data-ttu-id="09a33-934">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="09a33-934">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-selectcontrol"></a><span data-ttu-id="09a33-935">メソッド selectControl</span><span class="sxs-lookup"><span data-stu-id="09a33-935">Method selectControl</span></span>

```xpp
public boolean selectControl([boolean value])
```

### <a name="parameters---selectcontrol"></a><span data-ttu-id="09a33-936">パラメーター - selectControl</span><span class="sxs-lookup"><span data-stu-id="09a33-936">Parameters - selectControl</span></span>

<span data-ttu-id="09a33-937">値</span><span class="sxs-lookup"><span data-stu-id="09a33-937">value</span></span>  

### <a name="return-value---selectcontrol"></a><span data-ttu-id="09a33-938">戻り値 - selectControl</span><span class="sxs-lookup"><span data-stu-id="09a33-938">Return Value - selectControl</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="09a33-939">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="09a33-939">Method showContextMenu</span></span>

<span data-ttu-id="09a33-940">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-940">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="09a33-941">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="09a33-941">Parameters - showContextMenu</span></span>

<span data-ttu-id="09a33-942">menuHandle</span><span class="sxs-lookup"><span data-stu-id="09a33-942">menuHandle</span></span>  
<span data-ttu-id="09a33-943">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="09a33-943">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="09a33-944">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="09a33-944">Return Value - showContextMenu</span></span>

<span data-ttu-id="09a33-945">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-945">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showtabs"></a><span data-ttu-id="09a33-946">メソッド showTabs</span><span class="sxs-lookup"><span data-stu-id="09a33-946">Method showTabs</span></span>

```xpp
public boolean showTabs([boolean value])
```

### <a name="parameters---showtabs"></a><span data-ttu-id="09a33-947">パラメーター - showTabs</span><span class="sxs-lookup"><span data-stu-id="09a33-947">Parameters - showTabs</span></span>

<span data-ttu-id="09a33-948">値</span><span class="sxs-lookup"><span data-stu-id="09a33-948">value</span></span>  

### <a name="return-value---showtabs"></a><span data-ttu-id="09a33-949">戻り値 - showTabs</span><span class="sxs-lookup"><span data-stu-id="09a33-949">Return Value - showTabs</span></span>

## <a name="method-skip"></a><span data-ttu-id="09a33-950">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="09a33-950">Method skip</span></span>

<span data-ttu-id="09a33-951">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-951">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="09a33-952">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="09a33-952">Parameters - skip</span></span>

<span data-ttu-id="09a33-953">値</span><span class="sxs-lookup"><span data-stu-id="09a33-953">value</span></span>  
<span data-ttu-id="09a33-954">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-954">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="09a33-955">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="09a33-955">Return Value - skip</span></span>

<span data-ttu-id="09a33-956">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09a33-956">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="09a33-957">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="09a33-957">Remarks - skip</span></span>

<span data-ttu-id="09a33-958">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="09a33-958">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="09a33-959">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="09a33-959">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="09a33-960">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="09a33-960">Parameters - sort</span></span>

<span data-ttu-id="09a33-961">sortDirection</span><span class="sxs-lookup"><span data-stu-id="09a33-961">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="09a33-962">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="09a33-962">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="09a33-963">メソッド style</span><span class="sxs-lookup"><span data-stu-id="09a33-963">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="09a33-964">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="09a33-964">Parameters - style</span></span>

<span data-ttu-id="09a33-965">値</span><span class="sxs-lookup"><span data-stu-id="09a33-965">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="09a33-966">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="09a33-966">Return Value - style</span></span>

## <a name="method-stylevalue"></a><span data-ttu-id="09a33-967">メソッド styleValue</span><span class="sxs-lookup"><span data-stu-id="09a33-967">Method styleValue</span></span>

```xpp
public TabStyle styleValue()
```

### <a name="return-value---stylevalue"></a><span data-ttu-id="09a33-968">戻り値 - styleValue</span><span class="sxs-lookup"><span data-stu-id="09a33-968">Return Value - styleValue</span></span>

## <a name="method-tab"></a><span data-ttu-id="09a33-969">メソッド tab</span><span class="sxs-lookup"><span data-stu-id="09a33-969">Method tab</span></span>

```xpp
public int tab([int value], [AutoMode mode])
```

### <a name="parameters---tab"></a><span data-ttu-id="09a33-970">パラメーター - tab</span><span class="sxs-lookup"><span data-stu-id="09a33-970">Parameters - tab</span></span>

<span data-ttu-id="09a33-971">値</span><span class="sxs-lookup"><span data-stu-id="09a33-971">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-972">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-972">mode</span></span>  

### <a name="return-value---tab"></a><span data-ttu-id="09a33-973">戻り値 - tab</span><span class="sxs-lookup"><span data-stu-id="09a33-973">Return Value - tab</span></span>

## <a name="method-tabappearance"></a><span data-ttu-id="09a33-974">メソッド tabAppearance</span><span class="sxs-lookup"><span data-stu-id="09a33-974">Method tabAppearance</span></span>

```xpp
public int tabAppearance([int value])
```

### <a name="parameters---tabappearance"></a><span data-ttu-id="09a33-975">パラメーター - tabAppearance</span><span class="sxs-lookup"><span data-stu-id="09a33-975">Parameters - tabAppearance</span></span>

<span data-ttu-id="09a33-976">値</span><span class="sxs-lookup"><span data-stu-id="09a33-976">value</span></span>  

### <a name="return-value---tabappearance"></a><span data-ttu-id="09a33-977">戻り値 - tabAppearance</span><span class="sxs-lookup"><span data-stu-id="09a33-977">Return Value - tabAppearance</span></span>

## <a name="method-tabautochange"></a><span data-ttu-id="09a33-978">メソッド tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="09a33-978">Method tabAutoChange</span></span>

```xpp
public boolean tabAutoChange([boolean value])
```

### <a name="parameters---tabautochange"></a><span data-ttu-id="09a33-979">パラメーター - tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="09a33-979">Parameters - tabAutoChange</span></span>

<span data-ttu-id="09a33-980">値</span><span class="sxs-lookup"><span data-stu-id="09a33-980">value</span></span>  

### <a name="return-value---tabautochange"></a><span data-ttu-id="09a33-981">戻り値 - tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="09a33-981">Return Value - tabAutoChange</span></span>

## <a name="method-tabchange"></a><span data-ttu-id="09a33-982">メソッド tabChange</span><span class="sxs-lookup"><span data-stu-id="09a33-982">Method tabChange</span></span>

```xpp
public boolean tabChange(int FromTab)
```

### <a name="parameters---tabchange"></a><span data-ttu-id="09a33-983">パラメーター - tabChange</span><span class="sxs-lookup"><span data-stu-id="09a33-983">Parameters - tabChange</span></span>

<span data-ttu-id="09a33-984">FromTab</span><span class="sxs-lookup"><span data-stu-id="09a33-984">FromTab</span></span>  

### <a name="return-value---tabchange"></a><span data-ttu-id="09a33-985">戻り値 - tabChange</span><span class="sxs-lookup"><span data-stu-id="09a33-985">Return Value - tabChange</span></span>

## <a name="method-tablayout"></a><span data-ttu-id="09a33-986">メソッド tabLayout</span><span class="sxs-lookup"><span data-stu-id="09a33-986">Method tabLayout</span></span>

```xpp
public int tabLayout([int value])
```

### <a name="parameters---tablayout"></a><span data-ttu-id="09a33-987">パラメーター - tabLayout</span><span class="sxs-lookup"><span data-stu-id="09a33-987">Parameters - tabLayout</span></span>

<span data-ttu-id="09a33-988">値</span><span class="sxs-lookup"><span data-stu-id="09a33-988">value</span></span>  

### <a name="return-value---tablayout"></a><span data-ttu-id="09a33-989">戻り値 - tabLayout</span><span class="sxs-lookup"><span data-stu-id="09a33-989">Return Value - tabLayout</span></span>

## <a name="method-tabmode"></a><span data-ttu-id="09a33-990">メソッド tabMode</span><span class="sxs-lookup"><span data-stu-id="09a33-990">Method tabMode</span></span>

```xpp
public AutoMode tabMode([AutoMode mode])
```

### <a name="parameters---tabmode"></a><span data-ttu-id="09a33-991">パラメーター - tabMode</span><span class="sxs-lookup"><span data-stu-id="09a33-991">Parameters - tabMode</span></span>

<span data-ttu-id="09a33-992">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-992">mode</span></span>  

### <a name="return-value---tabmode"></a><span data-ttu-id="09a33-993">戻り値 - tabMode</span><span class="sxs-lookup"><span data-stu-id="09a33-993">Return Value - tabMode</span></span>

## <a name="method-tabplacement"></a><span data-ttu-id="09a33-994">メソッド tabPlacement</span><span class="sxs-lookup"><span data-stu-id="09a33-994">Method tabPlacement</span></span>

```xpp
public int tabPlacement([int value])
```

### <a name="parameters---tabplacement"></a><span data-ttu-id="09a33-995">パラメーター - tabPlacement</span><span class="sxs-lookup"><span data-stu-id="09a33-995">Parameters - tabPlacement</span></span>

<span data-ttu-id="09a33-996">値</span><span class="sxs-lookup"><span data-stu-id="09a33-996">value</span></span>  

### <a name="return-value---tabplacement"></a><span data-ttu-id="09a33-997">戻り値 - tabPlacement</span><span class="sxs-lookup"><span data-stu-id="09a33-997">Return Value - tabPlacement</span></span>

## <a name="method-tabs"></a><span data-ttu-id="09a33-998">メソッド tabs</span><span class="sxs-lookup"><span data-stu-id="09a33-998">Method tabs</span></span>

```xpp
public int tabs([int value])
```

### <a name="parameters---tabs"></a><span data-ttu-id="09a33-999">パラメーター - tabs</span><span class="sxs-lookup"><span data-stu-id="09a33-999">Parameters - tabs</span></span>

<span data-ttu-id="09a33-1000">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1000">value</span></span>  

### <a name="return-value---tabs"></a><span data-ttu-id="09a33-1001">戻り値 - tabs</span><span class="sxs-lookup"><span data-stu-id="09a33-1001">Return Value - tabs</span></span>

## <a name="method-tabvalue"></a><span data-ttu-id="09a33-1002">メソッド tabValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1002">Method tabValue</span></span>

```xpp
public int tabValue([int value])
```

### <a name="parameters---tabvalue"></a><span data-ttu-id="09a33-1003">パラメーター - tabValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1003">Parameters - tabValue</span></span>

<span data-ttu-id="09a33-1004">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1004">value</span></span>  

### <a name="return-value---tabvalue"></a><span data-ttu-id="09a33-1005">戻り値 - tabValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1005">Return Value - tabValue</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="09a33-1006">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="09a33-1006">Method toolTip</span></span>

<span data-ttu-id="09a33-1007">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1007">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="09a33-1008">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="09a33-1008">Return Value - toolTip</span></span>

<span data-ttu-id="09a33-1009">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="09a33-1009">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="09a33-1010">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="09a33-1010">Remarks - toolTip</span></span>

<span data-ttu-id="09a33-1011">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1011">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="09a33-1012">メソッド top</span><span class="sxs-lookup"><span data-stu-id="09a33-1012">Method top</span></span>

<span data-ttu-id="09a33-1013">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1013">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="09a33-1014">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="09a33-1014">Parameters - top</span></span>

<span data-ttu-id="09a33-1015">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1015">value</span></span>  
<span data-ttu-id="09a33-1016">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1016">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="09a33-1017">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-1017">mode</span></span>  
<span data-ttu-id="09a33-1018">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1018">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="09a33-1019">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="09a33-1019">Return Value - top</span></span>

<span data-ttu-id="09a33-1020">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="09a33-1020">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="09a33-1021">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-1021">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="09a33-1022">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-1022">Parameters - topMargin</span></span>

<span data-ttu-id="09a33-1023">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1023">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-1024">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-1024">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="09a33-1025">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="09a33-1025">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="09a33-1026">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1026">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="09a33-1027">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1027">Parameters - topMarginMode</span></span>

<span data-ttu-id="09a33-1028">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-1028">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="09a33-1029">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1029">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="09a33-1030">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1030">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="09a33-1031">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1031">Parameters - topMarginValue</span></span>

<span data-ttu-id="09a33-1032">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1032">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="09a33-1033">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1033">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="09a33-1034">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1034">Method topMode</span></span>

<span data-ttu-id="09a33-1035">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1035">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="09a33-1036">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1036">Parameters - topMode</span></span>

<span data-ttu-id="09a33-1037">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1037">value</span></span>  
<span data-ttu-id="09a33-1038">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1038">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="09a33-1039">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1039">Return Value - topMode</span></span>

<span data-ttu-id="09a33-1040">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="09a33-1040">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="09a33-1041">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1041">Method topValue</span></span>

<span data-ttu-id="09a33-1042">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1042">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="09a33-1043">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1043">Parameters - topValue</span></span>

<span data-ttu-id="09a33-1044">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1044">value</span></span>  
<span data-ttu-id="09a33-1045">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1045">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="09a33-1046">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1046">Return Value - topValue</span></span>

<span data-ttu-id="09a33-1047">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="09a33-1047">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="09a33-1048">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="09a33-1048">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="09a33-1049">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="09a33-1049">Parameters - type</span></span>

<span data-ttu-id="09a33-1050">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1050">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="09a33-1051">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="09a33-1051">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="09a33-1052">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="09a33-1052">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="09a33-1053">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="09a33-1053">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="09a33-1054">データ</span><span class="sxs-lookup"><span data-stu-id="09a33-1054">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="09a33-1055">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="09a33-1055">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="09a33-1056">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="09a33-1056">Method userData</span></span>

<span data-ttu-id="09a33-1057">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1057">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="09a33-1058">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="09a33-1058">Parameters - userData</span></span>

<span data-ttu-id="09a33-1059">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1059">value</span></span>  
<span data-ttu-id="09a33-1060">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1060">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="09a33-1061">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="09a33-1061">Return Value - userData</span></span>

<span data-ttu-id="09a33-1062">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="09a33-1062">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="09a33-1063">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="09a33-1063">Method userDataItem</span></span>

<span data-ttu-id="09a33-1064">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1064">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="09a33-1065">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="09a33-1065">Parameters - userDataItem</span></span>

<span data-ttu-id="09a33-1066">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1066">value</span></span>  
<span data-ttu-id="09a33-1067">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1067">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="09a33-1068">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="09a33-1068">Return Value - userDataItem</span></span>

<span data-ttu-id="09a33-1069">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="09a33-1069">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="09a33-1070">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="09a33-1070">Method userDataItems</span></span>

<span data-ttu-id="09a33-1071">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1071">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="09a33-1072">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="09a33-1072">Parameters - userDataItems</span></span>

<span data-ttu-id="09a33-1073">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1073">value</span></span>  
<span data-ttu-id="09a33-1074">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1074">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="09a33-1075">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="09a33-1075">Return Value - userDataItems</span></span>

<span data-ttu-id="09a33-1076">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="09a33-1076">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="09a33-1077">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="09a33-1077">Method userDisable</span></span>

<span data-ttu-id="09a33-1078">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1078">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="09a33-1079">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="09a33-1079">Parameters - userDisable</span></span>

<span data-ttu-id="09a33-1080">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1080">value</span></span>  
<span data-ttu-id="09a33-1081">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1081">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="09a33-1082">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="09a33-1082">Return Value - userDisable</span></span>

<span data-ttu-id="09a33-1083">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="09a33-1083">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="09a33-1084">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="09a33-1084">Method userHeight</span></span>

<span data-ttu-id="09a33-1085">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1085">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="09a33-1086">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="09a33-1086">Parameters - userHeight</span></span>

<span data-ttu-id="09a33-1087">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1087">value</span></span>  
<span data-ttu-id="09a33-1088">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1088">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="09a33-1089">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="09a33-1089">Return Value - userHeight</span></span>

<span data-ttu-id="09a33-1090">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="09a33-1090">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="09a33-1091">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="09a33-1091">Method userHide</span></span>

<span data-ttu-id="09a33-1092">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1092">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="09a33-1093">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="09a33-1093">Parameters - userHide</span></span>

<span data-ttu-id="09a33-1094">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1094">value</span></span>  
<span data-ttu-id="09a33-1095">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1095">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="09a33-1096">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="09a33-1096">Return Value - userHide</span></span>

<span data-ttu-id="09a33-1097">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="09a33-1097">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="09a33-1098">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="09a33-1098">Remarks - userHide</span></span>

<span data-ttu-id="09a33-1099">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1099">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="09a33-1100">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1100">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="09a33-1101">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1101">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="09a33-1102">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="09a33-1102">Method userOrgContainer</span></span>

<span data-ttu-id="09a33-1103">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1103">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="09a33-1104">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="09a33-1104">Parameters - userOrgContainer</span></span>

<span data-ttu-id="09a33-1105">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1105">value</span></span>  
<span data-ttu-id="09a33-1106">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1106">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="09a33-1107">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="09a33-1107">Return Value - userOrgContainer</span></span>

<span data-ttu-id="09a33-1108">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="09a33-1108">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="09a33-1109">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="09a33-1109">Method userOrgSibling</span></span>

<span data-ttu-id="09a33-1110">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1110">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="09a33-1111">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="09a33-1111">Parameters - userOrgSibling</span></span>

<span data-ttu-id="09a33-1112">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1112">value</span></span>  
<span data-ttu-id="09a33-1113">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1113">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="09a33-1114">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="09a33-1114">Return Value - userOrgSibling</span></span>

<span data-ttu-id="09a33-1115">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="09a33-1115">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="09a33-1116">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="09a33-1116">Method userPromptText</span></span>

<span data-ttu-id="09a33-1117">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1117">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="09a33-1118">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="09a33-1118">Parameters - userPromptText</span></span>

<span data-ttu-id="09a33-1119">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1119">value</span></span>  
<span data-ttu-id="09a33-1120">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1120">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="09a33-1121">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="09a33-1121">Return Value - userPromptText</span></span>

<span data-ttu-id="09a33-1122">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="09a33-1122">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="09a33-1123">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="09a33-1123">Method userSecurityLevel</span></span>

<span data-ttu-id="09a33-1124">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1124">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="09a33-1125">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="09a33-1125">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="09a33-1126">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1126">value</span></span>  
<span data-ttu-id="09a33-1127">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1127">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="09a33-1128">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="09a33-1128">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="09a33-1129">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="09a33-1129">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="09a33-1130">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="09a33-1130">Method userSkip</span></span>

<span data-ttu-id="09a33-1131">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1131">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="09a33-1132">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="09a33-1132">Parameters - userSkip</span></span>

<span data-ttu-id="09a33-1133">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1133">value</span></span>  
<span data-ttu-id="09a33-1134">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1134">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="09a33-1135">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="09a33-1135">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="09a33-1136">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="09a33-1136">Return Value - userSkip</span></span>

<span data-ttu-id="09a33-1137">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="09a33-1137">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="09a33-1138">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="09a33-1138">Method userWidth</span></span>

<span data-ttu-id="09a33-1139">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1139">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="09a33-1140">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="09a33-1140">Parameters - userWidth</span></span>

<span data-ttu-id="09a33-1141">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1141">value</span></span>  
<span data-ttu-id="09a33-1142">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1142">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="09a33-1143">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="09a33-1143">Return Value - userWidth</span></span>

<span data-ttu-id="09a33-1144">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1144">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="09a33-1145">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="09a33-1145">Remarks - userWidth</span></span>

<span data-ttu-id="09a33-1146">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1146">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="09a33-1147">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="09a33-1147">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="09a33-1148">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1148">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="09a33-1149">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="09a33-1149">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="09a33-1150">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="09a33-1150">Parameters - useUserLayout</span></span>

<span data-ttu-id="09a33-1151">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1151">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="09a33-1152">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="09a33-1152">Return Value - useUserLayout</span></span>

## <a name="method-verticalscrollbarvisible"></a><span data-ttu-id="09a33-1153">メソッド verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="09a33-1153">Method verticalScrollBarVisible</span></span>

```xpp
public boolean verticalScrollBarVisible([boolean value])
```

### <a name="parameters---verticalscrollbarvisible"></a><span data-ttu-id="09a33-1154">パラメーター - verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="09a33-1154">Parameters - verticalScrollBarVisible</span></span>

<span data-ttu-id="09a33-1155">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1155">value</span></span>  

### <a name="return-value---verticalscrollbarvisible"></a><span data-ttu-id="09a33-1156">戻り値 - verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="09a33-1156">Return Value - verticalScrollBarVisible</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="09a33-1157">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="09a33-1157">Method verticalSpacing</span></span>

<span data-ttu-id="09a33-1158">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1158">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="09a33-1159">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="09a33-1159">Parameters - verticalSpacing</span></span>

<span data-ttu-id="09a33-1160">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1160">value</span></span>  
<span data-ttu-id="09a33-1161">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1161">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="09a33-1162">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-1162">mode</span></span>  
<span data-ttu-id="09a33-1163">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1163">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="09a33-1164">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="09a33-1164">Return Value - verticalSpacing</span></span>

<span data-ttu-id="09a33-1165">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="09a33-1165">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="09a33-1166">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1166">Method verticalSpacingMode</span></span>

<span data-ttu-id="09a33-1167">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1167">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="09a33-1168">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1168">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="09a33-1169">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-1169">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="09a33-1170">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1170">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="09a33-1171">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="09a33-1171">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="09a33-1172">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1172">Method verticalSpacingValue</span></span>

<span data-ttu-id="09a33-1173">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1173">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="09a33-1174">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1174">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="09a33-1175">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1175">value</span></span>  
<span data-ttu-id="09a33-1176">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="09a33-1176">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="09a33-1177">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1177">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="09a33-1178">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="09a33-1178">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="09a33-1179">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1179">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="09a33-1180">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1180">Parameters - viewEditMode</span></span>

<span data-ttu-id="09a33-1181">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1181">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="09a33-1182">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1182">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="09a33-1183">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="09a33-1183">Method visible</span></span>

<span data-ttu-id="09a33-1184">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1184">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="09a33-1185">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="09a33-1185">Parameters - visible</span></span>

<span data-ttu-id="09a33-1186">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1186">value</span></span>  
<span data-ttu-id="09a33-1187">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1187">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="09a33-1188">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="09a33-1188">Return Value - visible</span></span>

<span data-ttu-id="09a33-1189">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="09a33-1189">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="09a33-1190">メソッド width</span><span class="sxs-lookup"><span data-stu-id="09a33-1190">Method width</span></span>

<span data-ttu-id="09a33-1191">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1191">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="09a33-1192">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="09a33-1192">Parameters - width</span></span>

<span data-ttu-id="09a33-1193">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1193">value</span></span>  

<!-- -->

<span data-ttu-id="09a33-1194">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-1194">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="09a33-1195">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="09a33-1195">Return Value - width</span></span>

<span data-ttu-id="09a33-1196">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="09a33-1196">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="09a33-1197">備考 - width</span><span class="sxs-lookup"><span data-stu-id="09a33-1197">Remarks - width</span></span>

<span data-ttu-id="09a33-1198">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1198">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="09a33-1199">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1199">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="09a33-1200">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-1200">Mode</span></span>           | <span data-ttu-id="09a33-1201">幅計算</span><span class="sxs-lookup"><span data-stu-id="09a33-1201">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a33-1202">-1 正確</span><span class="sxs-lookup"><span data-stu-id="09a33-1202">-1 Exact</span></span>       | <span data-ttu-id="09a33-1203">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1203">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="09a33-1204">0 自動</span><span class="sxs-lookup"><span data-stu-id="09a33-1204">0 Auto</span></span>         | <span data-ttu-id="09a33-1205">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1205">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="09a33-1206">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="09a33-1206">1 Column width</span></span> | <span data-ttu-id="09a33-1207">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="09a33-1207">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="09a33-1208">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1208">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="09a33-1209">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1209">Method widthMode</span></span>

<span data-ttu-id="09a33-1210">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1210">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="09a33-1211">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1211">Parameters - widthMode</span></span>

<span data-ttu-id="09a33-1212">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1212">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="09a33-1213">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1213">Return Value - widthMode</span></span>

<span data-ttu-id="09a33-1214">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1214">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="09a33-1215">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1215">Remarks - widthMode</span></span>

<span data-ttu-id="09a33-1216">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1216">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="09a33-1217">モード</span><span class="sxs-lookup"><span data-stu-id="09a33-1217">Mode</span></span>         | <span data-ttu-id="09a33-1218">幅計算</span><span class="sxs-lookup"><span data-stu-id="09a33-1218">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a33-1219">正確</span><span class="sxs-lookup"><span data-stu-id="09a33-1219">Exact</span></span>        | <span data-ttu-id="09a33-1220">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1220">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="09a33-1221">自動</span><span class="sxs-lookup"><span data-stu-id="09a33-1221">Auto</span></span>         | <span data-ttu-id="09a33-1222">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1222">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="09a33-1223">列の幅</span><span class="sxs-lookup"><span data-stu-id="09a33-1223">Column width</span></span> | <span data-ttu-id="09a33-1224">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="09a33-1224">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="09a33-1225">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="09a33-1225">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="09a33-1226">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1226">Method widthValue</span></span>

<span data-ttu-id="09a33-1227">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1227">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="09a33-1228">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1228">Parameters - widthValue</span></span>

<span data-ttu-id="09a33-1229">値</span><span class="sxs-lookup"><span data-stu-id="09a33-1229">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="09a33-1230">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1230">Return Value - widthValue</span></span>

<span data-ttu-id="09a33-1231">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="09a33-1231">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="09a33-1232">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="09a33-1232">Remarks - widthValue</span></span>

<span data-ttu-id="09a33-1233">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1233">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="09a33-1234">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="09a33-1234">Method setFocus</span></span>

<span data-ttu-id="09a33-1235">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1235">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-lostfocus"></a><span data-ttu-id="09a33-1236">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="09a33-1236">Method lostFocus</span></span>

<span data-ttu-id="09a33-1237">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1237">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="09a33-1238">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="09a33-1238">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="09a33-1239">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="09a33-1239">Parameters - OnLostFocus</span></span>

<span data-ttu-id="09a33-1240">sender</span><span class="sxs-lookup"><span data-stu-id="09a33-1240">sender</span></span>  

<!-- -->

<span data-ttu-id="09a33-1241">e</span><span class="sxs-lookup"><span data-stu-id="09a33-1241">e</span></span>  

## <a name="method-drop"></a><span data-ttu-id="09a33-1242">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="09a33-1242">Method drop</span></span>

<span data-ttu-id="09a33-1243">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1243">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="09a33-1244">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="09a33-1244">Parameters - drop</span></span>

<span data-ttu-id="09a33-1245">dragSource</span><span class="sxs-lookup"><span data-stu-id="09a33-1245">dragSource</span></span>  
<span data-ttu-id="09a33-1246">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1246">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-1247">dragMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1247">dragMode</span></span>  
<span data-ttu-id="09a33-1248">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1248">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-1249">x</span><span class="sxs-lookup"><span data-stu-id="09a33-1249">x</span></span>  
<span data-ttu-id="09a33-1250">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1250">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-1251">y</span><span class="sxs-lookup"><span data-stu-id="09a33-1251">y</span></span>  
<span data-ttu-id="09a33-1252">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1252">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="09a33-1253">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="09a33-1253">Method endDrag</span></span>

<span data-ttu-id="09a33-1254">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1254">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="09a33-1255">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="09a33-1255">Remarks - endDrag</span></span>

<span data-ttu-id="09a33-1256">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="09a33-1256">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="09a33-1257">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1257">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="09a33-1258">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="09a33-1258">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="09a33-1259">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="09a33-1259">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="09a33-1260">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="09a33-1260">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="09a33-1261">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="09a33-1261">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="09a33-1262">overrideObject</span><span class="sxs-lookup"><span data-stu-id="09a33-1262">overrideObject</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="09a33-1263">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="09a33-1263">Method gotFocus</span></span>

<span data-ttu-id="09a33-1264">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1264">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="09a33-1265">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="09a33-1265">Method mouseEnter</span></span>

<span data-ttu-id="09a33-1266">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1266">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="09a33-1267">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="09a33-1267">Parameters - mouseEnter</span></span>

<span data-ttu-id="09a33-1268">x</span><span class="sxs-lookup"><span data-stu-id="09a33-1268">x</span></span>  
<span data-ttu-id="09a33-1269">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1269">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-1270">y</span><span class="sxs-lookup"><span data-stu-id="09a33-1270">y</span></span>  
<span data-ttu-id="09a33-1271">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1271">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-1272">ボタン</span><span class="sxs-lookup"><span data-stu-id="09a33-1272">button</span></span>  
<span data-ttu-id="09a33-1273">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1273">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-1274">Ctrl</span><span class="sxs-lookup"><span data-stu-id="09a33-1274">Ctrl</span></span>  
<span data-ttu-id="09a33-1275">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1275">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="09a33-1276">シフト</span><span class="sxs-lookup"><span data-stu-id="09a33-1276">Shift</span></span>  
<span data-ttu-id="09a33-1277">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1277">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-jumpref"></a><span data-ttu-id="09a33-1278">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="09a33-1278">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-paste"></a><span data-ttu-id="09a33-1279">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="09a33-1279">Method paste</span></span>

<span data-ttu-id="09a33-1280">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1280">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-dropex"></a><span data-ttu-id="09a33-1281">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="09a33-1281">Method dropEx</span></span>

<span data-ttu-id="09a33-1282">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1282">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="09a33-1283">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="09a33-1283">Parameters - dropEx</span></span>

<span data-ttu-id="09a33-1284">dragSource</span><span class="sxs-lookup"><span data-stu-id="09a33-1284">dragSource</span></span>  
<span data-ttu-id="09a33-1285">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1285">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-1286">dragMode</span><span class="sxs-lookup"><span data-stu-id="09a33-1286">dragMode</span></span>  
<span data-ttu-id="09a33-1287">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1287">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-1288">x</span><span class="sxs-lookup"><span data-stu-id="09a33-1288">x</span></span>  
<span data-ttu-id="09a33-1289">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1289">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="09a33-1290">y</span><span class="sxs-lookup"><span data-stu-id="09a33-1290">y</span></span>  
<span data-ttu-id="09a33-1291">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09a33-1291">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-arrange"></a><span data-ttu-id="09a33-1292">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="09a33-1292">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="09a33-1293">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="09a33-1293">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="09a33-1294">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="09a33-1294">Parameters - OnGotFocus</span></span>

<span data-ttu-id="09a33-1295">sender</span><span class="sxs-lookup"><span data-stu-id="09a33-1295">sender</span></span>  

<!-- -->

<span data-ttu-id="09a33-1296">e</span><span class="sxs-lookup"><span data-stu-id="09a33-1296">e</span></span>  

## <a name="method-context"></a><span data-ttu-id="09a33-1297">メソッド context</span><span class="sxs-lookup"><span data-stu-id="09a33-1297">Method context</span></span>

<span data-ttu-id="09a33-1298">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1298">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-copy"></a><span data-ttu-id="09a33-1299">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="09a33-1299">Method copy</span></span>

<span data-ttu-id="09a33-1300">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="09a33-1300">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-filter"></a><span data-ttu-id="09a33-1301">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="09a33-1301">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="09a33-1302">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="09a33-1302">Parameters - filter</span></span>

<span data-ttu-id="09a33-1303">filterStr</span><span class="sxs-lookup"><span data-stu-id="09a33-1303">filterStr</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="09a33-1304">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="09a33-1304">Method resetUserSetting</span></span>

<span data-ttu-id="09a33-1305">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="09a33-1305">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-cut"></a><span data-ttu-id="09a33-1306">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="09a33-1306">Method cut</span></span>

<span data-ttu-id="09a33-1307">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="09a33-1307">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-mouseleave"></a><span data-ttu-id="09a33-1308">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="09a33-1308">Method mouseLeave</span></span>

<span data-ttu-id="09a33-1309">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1309">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="09a33-1310">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="09a33-1310">Method displayControl</span></span>

<span data-ttu-id="09a33-1311">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1311">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-ontabchanged"></a><span data-ttu-id="09a33-1312">メソッド OnTabChanged</span><span class="sxs-lookup"><span data-stu-id="09a33-1312">Method OnTabChanged</span></span>

```xpp
private void OnTabChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ontabchanged"></a><span data-ttu-id="09a33-1313">パラメーター - OnTabChanged</span><span class="sxs-lookup"><span data-stu-id="09a33-1313">Parameters - OnTabChanged</span></span>

<span data-ttu-id="09a33-1314">sender</span><span class="sxs-lookup"><span data-stu-id="09a33-1314">sender</span></span>  

<!-- -->

<span data-ttu-id="09a33-1315">e</span><span class="sxs-lookup"><span data-stu-id="09a33-1315">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="09a33-1316">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="09a33-1316">Method inputSearch</span></span>

<span data-ttu-id="09a33-1317">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1317">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="09a33-1318">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="09a33-1318">Parameters - inputSearch</span></span>

<span data-ttu-id="09a33-1319">searchStr</span><span class="sxs-lookup"><span data-stu-id="09a33-1319">searchStr</span></span>  
<span data-ttu-id="09a33-1320">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="09a33-1320">The string value to use to filter data; optional.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="09a33-1321">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="09a33-1321">Method dragLeave</span></span>

<span data-ttu-id="09a33-1322">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="09a33-1322">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-tabchanged"></a><span data-ttu-id="09a33-1323">メソッド tabChanged</span><span class="sxs-lookup"><span data-stu-id="09a33-1323">Method tabChanged</span></span>

```xpp
public void tabChanged(int FromTab, int ToTab)
```

### <a name="parameters---tabchanged"></a><span data-ttu-id="09a33-1324">パラメーター - tabChanged</span><span class="sxs-lookup"><span data-stu-id="09a33-1324">Parameters - tabChanged</span></span>

<span data-ttu-id="09a33-1325">FromTab</span><span class="sxs-lookup"><span data-stu-id="09a33-1325">FromTab</span></span>  

<!-- -->

<span data-ttu-id="09a33-1326">ToTab</span><span class="sxs-lookup"><span data-stu-id="09a33-1326">ToTab</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="09a33-1327">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="09a33-1327">Method prefColumnSize</span></span>

<span data-ttu-id="09a33-1328">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="09a33-1328">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="09a33-1329">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="09a33-1329">Parameters - prefColumnSize</span></span>

<span data-ttu-id="09a33-1330">width</span><span class="sxs-lookup"><span data-stu-id="09a33-1330">width</span></span>  
<span data-ttu-id="09a33-1331">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="09a33-1331">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="09a33-1332">height</span><span class="sxs-lookup"><span data-stu-id="09a33-1332">height</span></span>  
<span data-ttu-id="09a33-1333">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="09a33-1333">The preferred height of the control.</span></span>

