---
title: FormGridControl クラス
description: このトピックでは、FormGridControl クラスについて説明します。
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
ms.openlocfilehash: 75df7c89da125b01c65b14d9d2df957ddaef296a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502938"
---
# <a name="class-formgridcontrol"></a><span data-ttu-id="ff1b1-103">クラス FormGridControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-103">Class FormGridControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormGridControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="ff1b1-104">備考</span><span class="sxs-lookup"><span data-stu-id="ff1b1-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="ff1b1-105">例</span><span class="sxs-lookup"><span data-stu-id="ff1b1-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ff1b1-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="ff1b1-106">Methods</span></span>

| <span data-ttu-id="ff1b1-107">方法</span><span class="sxs-lookup"><span data-stu-id="ff1b1-107">Method</span></span>                                                                                                              | <span data-ttu-id="ff1b1-108">説明</span><span class="sxs-lookup"><span data-stu-id="ff1b1-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b1-109">public int activeBackColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-109">public int activeBackColor(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-110">public int activeForeColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-110">public int activeForeColor(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-111">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-111">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-112">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-112">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-113">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-113">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-114">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-114">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="ff1b1-115">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-115">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ff1b1-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="ff1b1-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-117">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="ff1b1-118">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-118">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="ff1b1-119">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-119">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="ff1b1-120">public int alternateRowShading(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-120">public int alternateRowShading(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-121">public boolean autoDataGroup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-121">public boolean autoDataGroup(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-122">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-122">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="ff1b1-123">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-123">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="ff1b1-124">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-124">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="ff1b1-125">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-125">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="ff1b1-126">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-126">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="ff1b1-127">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-127">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="ff1b1-128">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-128">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="ff1b1-129">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-129">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="ff1b1-130">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-130">public int border(\[int value\])</span></span>                                                                                    | <span data-ttu-id="ff1b1-131">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-131">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="ff1b1-132">public int bottomMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-132">public int bottomMargin(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-133">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-133">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="ff1b1-134">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-134">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="ff1b1-135">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-135">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-136">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-136">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-137">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-137">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="ff1b1-138">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-138">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ff1b1-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="ff1b1-140">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-140">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="ff1b1-141">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-141">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="ff1b1-142">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-142">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="ff1b1-143">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-143">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-144">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-144">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-145">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-145">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-146">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-146">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="ff1b1-147">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-147">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="ff1b1-148">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-148">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-149">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-149">public str dataGroup(\[str value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-150">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-150">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="ff1b1-151">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-151">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="ff1b1-152">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-152">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="ff1b1-153">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-153">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="ff1b1-154">public str defaultAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-154">public str defaultAction(\[str value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-155">public str defaultActionLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-155">public str defaultActionLabel(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-156">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-156">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="ff1b1-157">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-157">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="ff1b1-158">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-158">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="ff1b1-159">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-159">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="ff1b1-160">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-160">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="ff1b1-161">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-161">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="ff1b1-162">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-162">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="ff1b1-163">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-163">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="ff1b1-164">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-164">public str dragText()</span></span>                                                                                               | <span data-ttu-id="ff1b1-165">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-165">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="ff1b1-166">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-166">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="ff1b1-167">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-167">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="ff1b1-168">public boolean exportAllowed(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-168">public boolean exportAllowed(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-169">public str exportLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-169">public str exportLabel(\[str value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-170">public Struct getLineData(int lineNumber)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-170">public Struct getLineData(int lineNumber)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-171">public Struct getSelectedData()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-171">public Struct getSelectedData()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-172">public boolean gridLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-172">public boolean gridLines(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-173">public int gridLinesStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-173">public int gridLinesStyle(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-174">public str groupBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-174">public str groupBy(\[str value\])</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-175">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-175">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="ff1b1-176">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-176">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="ff1b1-177">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-177">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="ff1b1-178">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-178">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="ff1b1-179">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-179">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="ff1b1-180">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-180">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="ff1b1-181">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-181">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="ff1b1-182">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-182">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="ff1b1-183">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-183">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="ff1b1-184">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-184">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="ff1b1-185">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-185">public str helpField()</span></span>                                                                                              | <span data-ttu-id="ff1b1-186">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-186">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ff1b1-187">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-187">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="ff1b1-188">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-188">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="ff1b1-189">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-189">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="ff1b1-190">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-190">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="ff1b1-191">public boolean highlightActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-191">public boolean highlightActive(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-192">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-192">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="ff1b1-193">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-193">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ff1b1-194">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-194">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-195">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-195">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="ff1b1-196">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-196">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="ff1b1-197">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-197">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="ff1b1-198">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-198">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="ff1b1-199">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-199">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="ff1b1-200">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-200">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="ff1b1-201">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-201">public boolean leave()</span></span>                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-202">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-202">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="ff1b1-203">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-203">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="ff1b1-204">public int leftMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-204">public int leftMargin(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-205">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-205">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="ff1b1-206">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-206">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ff1b1-207">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-207">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="ff1b1-208">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-208">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="ff1b1-209">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-209">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="ff1b1-210">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-210">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="ff1b1-211">public int moreRowsIndicator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-211">public int moreRowsIndicator(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-212">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-212">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="ff1b1-213">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-213">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="ff1b1-214">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-214">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="ff1b1-215">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-215">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="ff1b1-216">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-216">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="ff1b1-217">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-217">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="ff1b1-218">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-218">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="ff1b1-219">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-219">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="ff1b1-220">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-220">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-221">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-221">public boolean multiSelect(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-222">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-222">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="ff1b1-223">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-223">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="ff1b1-224">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-224">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-225">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-225">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-226">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-226">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="ff1b1-227">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-227">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ff1b1-228">public int rightMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-228">public int rightMargin(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-229">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-229">public int scrollbars(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-230">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-230">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="ff1b1-231">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-231">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="ff1b1-232">public boolean showColLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-232">public boolean showColLabels(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-233">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-233">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="ff1b1-234">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-234">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ff1b1-235">public boolean showRowLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-235">public boolean showRowLabels(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-236">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-236">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="ff1b1-237">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-237">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="ff1b1-238">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-238">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-239">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-239">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-240">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-240">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="ff1b1-241">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-241">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="ff1b1-242">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-242">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="ff1b1-243">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-243">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="ff1b1-244">public int topMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-244">public int topMargin(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-245">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-245">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="ff1b1-246">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-246">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="ff1b1-247">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-247">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="ff1b1-248">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-248">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="ff1b1-249">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-249">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-250">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-250">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-251">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-251">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="ff1b1-252">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-252">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="ff1b1-253">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-253">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="ff1b1-254">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-254">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="ff1b1-255">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-255">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="ff1b1-256">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-256">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="ff1b1-257">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-257">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="ff1b1-258">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-258">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="ff1b1-259">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-259">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="ff1b1-260">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-260">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="ff1b1-261">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-261">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="ff1b1-262">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-262">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="ff1b1-263">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-263">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="ff1b1-264">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-264">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="ff1b1-265">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-265">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="ff1b1-266">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-266">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ff1b1-267">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-267">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="ff1b1-268">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-268">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="ff1b1-269">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-269">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="ff1b1-270">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-270">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="ff1b1-271">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-271">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="ff1b1-272">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-272">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="ff1b1-273">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-273">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="ff1b1-274">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-274">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="ff1b1-275">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-275">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-276">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-276">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="ff1b1-277">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-277">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ff1b1-278">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-278">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="ff1b1-279">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-279">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="ff1b1-280">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-280">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="ff1b1-281">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-281">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ff1b1-282">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-282">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="ff1b1-283">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-283">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="ff1b1-284">public int visibleCols(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-284">public int visibleCols(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-285">public AutoMode visibleColsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-285">public AutoMode visibleColsMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-286">public int visibleColsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-286">public int visibleColsValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-287">public int visibleRows(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-287">public int visibleRows(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-288">public AutoMode visibleRowsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-288">public AutoMode visibleRowsMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-289">public int visibleRowsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-289">public int visibleRowsValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-290">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-290">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="ff1b1-291">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-291">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="ff1b1-292">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-292">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="ff1b1-293">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-293">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="ff1b1-294">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-294">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="ff1b1-295">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-295">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="ff1b1-296">public void cut()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-296">public void cut()</span></span>                                                                                                   | <span data-ttu-id="ff1b1-297">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-297">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="ff1b1-298">public void applyQuickFilter(\[int controlId\], \[str filterValue\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-298">public void applyQuickFilter(\[int controlId\], \[str filterValue\])</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-299">public void autoSizeColumns(\[boolean autoSizeColumns\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-299">public void autoSizeColumns(\[boolean autoSizeColumns\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-300">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-300">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="ff1b1-301">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-301">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="ff1b1-302">public void context()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-302">public void context()</span></span>                                                                                               | <span data-ttu-id="ff1b1-303">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-303">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ff1b1-304">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-304">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-305">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-305">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                           |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-306">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-306">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-307">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-307">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-308">public void copy()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-308">public void copy()</span></span>                                                                                                  | <span data-ttu-id="ff1b1-309">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-309">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="ff1b1-310">public void enter()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-310">public void enter()</span></span>                                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-311">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-311">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="ff1b1-312">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-312">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="ff1b1-313">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-313">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="ff1b1-314">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-314">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="ff1b1-315">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-315">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-316">public void paste()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-316">public void paste()</span></span>                                                                                                 | <span data-ttu-id="ff1b1-317">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-317">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ff1b1-318">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-318">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="ff1b1-319">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-319">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="ff1b1-320">public void quickFilterProvider(\[GridQuickFilterProvider quickFilterProvider\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-320">public void quickFilterProvider(\[GridQuickFilterProvider quickFilterProvider\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-321">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-321">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="ff1b1-322">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-322">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="ff1b1-323">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-323">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-324">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-324">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="ff1b1-325">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-325">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="ff1b1-326">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-326">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-327">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="ff1b1-327">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="ff1b1-328">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-328">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="ff1b1-329">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-329">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="ff1b1-330">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-330">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="ff1b1-331">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ff1b1-331">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-332">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-332">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="ff1b1-333">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-333">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="ff1b1-334">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-334">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="ff1b1-335">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-335">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="ff1b1-336">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-336">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="ff1b1-337">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-337">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="ff1b1-338">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-338">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="ff1b1-339">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-339">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="ff1b1-340">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-340">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ff1b1-341">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="ff1b1-341">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="ff1b1-342">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-342">Sets the focus on the control.</span></span>                                                                                                                                          |

## <a name="method-activebackcolor"></a><span data-ttu-id="ff1b1-343">メソッド activeBackColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-343">Method activeBackColor</span></span>

```xpp
public int activeBackColor([int value])
```

### <a name="parameters---activebackcolor"></a><span data-ttu-id="ff1b1-344">パラメーター - activeBackColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-344">Parameters - activeBackColor</span></span>

<span data-ttu-id="ff1b1-345">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-345">value</span></span>  

### <a name="return-value---activebackcolor"></a><span data-ttu-id="ff1b1-346">戻り値 - activeBackColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-346">Return Value - activeBackColor</span></span>

## <a name="method-activeforecolor"></a><span data-ttu-id="ff1b1-347">メソッド activeForeColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-347">Method activeForeColor</span></span>

```xpp
public int activeForeColor([int value])
```

### <a name="parameters---activeforecolor"></a><span data-ttu-id="ff1b1-348">パラメーター - activeForeColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-348">Parameters - activeForeColor</span></span>

<span data-ttu-id="ff1b1-349">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-349">value</span></span>  

### <a name="return-value---activeforecolor"></a><span data-ttu-id="ff1b1-350">戻り値 - activeForeColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-350">Return Value - activeForeColor</span></span>

## <a name="method-addcontrol"></a><span data-ttu-id="ff1b1-351">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-351">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="ff1b1-352">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-352">Parameters - addControl</span></span>

<span data-ttu-id="ff1b1-353">controlType</span><span class="sxs-lookup"><span data-stu-id="ff1b1-353">controlType</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-354">controlName</span><span class="sxs-lookup"><span data-stu-id="ff1b1-354">controlName</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-355">insertAfter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-355">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="ff1b1-356">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-356">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="ff1b1-357">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-357">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="ff1b1-358">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-358">Parameters - addControlEx</span></span>

<span data-ttu-id="ff1b1-359">controlClass</span><span class="sxs-lookup"><span data-stu-id="ff1b1-359">controlClass</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-360">controlName</span><span class="sxs-lookup"><span data-stu-id="ff1b1-360">controlName</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-361">insertAfter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-361">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="ff1b1-362">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-362">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="ff1b1-363">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-363">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="ff1b1-364">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-364">Parameters - addDataField</span></span>

<span data-ttu-id="ff1b1-365">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="ff1b1-365">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-366">fieldId</span><span class="sxs-lookup"><span data-stu-id="ff1b1-366">fieldId</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-367">insertAfter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-367">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-368">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ff1b1-368">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="ff1b1-369">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-369">Return Value - addDataField</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="ff1b1-370">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-370">Method alignControl</span></span>

<span data-ttu-id="ff1b1-371">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-371">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="ff1b1-372">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-372">Parameters - alignControl</span></span>

<span data-ttu-id="ff1b1-373">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-373">value</span></span>  
<span data-ttu-id="ff1b1-374">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-374">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="ff1b1-375">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-375">Return Value - alignControl</span></span>

<span data-ttu-id="ff1b1-376">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-376">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="ff1b1-377">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-377">Remarks - alignControl</span></span>

<span data-ttu-id="ff1b1-378">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-378">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="ff1b1-379">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="ff1b1-379">Method allowEdit</span></span>

<span data-ttu-id="ff1b1-380">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-380">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="ff1b1-381">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ff1b1-381">Parameters - allowEdit</span></span>

<span data-ttu-id="ff1b1-382">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-382">value</span></span>  
<span data-ttu-id="ff1b1-383">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-383">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="ff1b1-384">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ff1b1-384">Return Value - allowEdit</span></span>

<span data-ttu-id="ff1b1-385">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-385">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="ff1b1-386">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ff1b1-386">Remarks - allowEdit</span></span>

<span data-ttu-id="ff1b1-387">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-387">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="ff1b1-388">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-388">Method allowSysSetup</span></span>

<span data-ttu-id="ff1b1-389">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-389">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="ff1b1-390">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-390">Return Value - allowSysSetup</span></span>

<span data-ttu-id="ff1b1-391">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-391">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-alternaterowshading"></a><span data-ttu-id="ff1b1-392">メソッド alternateRowShading</span><span class="sxs-lookup"><span data-stu-id="ff1b1-392">Method alternateRowShading</span></span>

```xpp
public int alternateRowShading([int value])
```

### <a name="parameters---alternaterowshading"></a><span data-ttu-id="ff1b1-393">パラメーター - alternateRowShading</span><span class="sxs-lookup"><span data-stu-id="ff1b1-393">Parameters - alternateRowShading</span></span>

<span data-ttu-id="ff1b1-394">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-394">value</span></span>  

### <a name="return-value---alternaterowshading"></a><span data-ttu-id="ff1b1-395">戻り値 - alternateRowShading</span><span class="sxs-lookup"><span data-stu-id="ff1b1-395">Return Value - alternateRowShading</span></span>

## <a name="method-autodatagroup"></a><span data-ttu-id="ff1b1-396">メソッド autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-396">Method autoDataGroup</span></span>

```xpp
public boolean autoDataGroup([boolean value])
```

### <a name="parameters---autodatagroup"></a><span data-ttu-id="ff1b1-397">パラメーター - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-397">Parameters - autoDataGroup</span></span>

<span data-ttu-id="ff1b1-398">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-398">value</span></span>  

### <a name="return-value---autodatagroup"></a><span data-ttu-id="ff1b1-399">戻り値 - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-399">Return Value - autoDataGroup</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="ff1b1-400">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ff1b1-400">Method autoDeclaration</span></span>

<span data-ttu-id="ff1b1-401">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-401">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="ff1b1-402">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ff1b1-402">Parameters - autoDeclaration</span></span>

<span data-ttu-id="ff1b1-403">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-403">value</span></span>  
<span data-ttu-id="ff1b1-404">プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-404">The value to assign to the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="ff1b1-405">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ff1b1-405">Return Value - autoDeclaration</span></span>

<span data-ttu-id="ff1b1-406">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-406">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="ff1b1-407">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ff1b1-407">Remarks - autoDeclaration</span></span>

<span data-ttu-id="ff1b1-408">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-408">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="ff1b1-409">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-409">Method backgroundColor</span></span>

<span data-ttu-id="ff1b1-410">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-410">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="ff1b1-411">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-411">Parameters - backgroundColor</span></span>

<span data-ttu-id="ff1b1-412">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-412">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="ff1b1-413">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-413">Return Value - backgroundColor</span></span>

<span data-ttu-id="ff1b1-414">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-414">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="ff1b1-415">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ff1b1-415">Remarks - backgroundColor</span></span>

<span data-ttu-id="ff1b1-416">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-416">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="ff1b1-417">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-417">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="ff1b1-418">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-418">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="ff1b1-419">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-419">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="ff1b1-420">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-420">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="ff1b1-421">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-421">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="ff1b1-422">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="ff1b1-422">Method backStyle</span></span>

<span data-ttu-id="ff1b1-423">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-423">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="ff1b1-424">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="ff1b1-424">Parameters - backStyle</span></span>

<span data-ttu-id="ff1b1-425">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-425">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="ff1b1-426">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="ff1b1-426">Return Value - backStyle</span></span>

<span data-ttu-id="ff1b1-427">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-427">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="ff1b1-428">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="ff1b1-428">Method beginDrag</span></span>

<span data-ttu-id="ff1b1-429">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-429">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="ff1b1-430">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ff1b1-430">Parameters - beginDrag</span></span>

<span data-ttu-id="ff1b1-431">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-431">x</span></span>  
<span data-ttu-id="ff1b1-432">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-432">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="ff1b1-433">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-433">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-434">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-434">y</span></span>  
<span data-ttu-id="ff1b1-435">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-435">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="ff1b1-436">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-436">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="ff1b1-437">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ff1b1-437">Return Value - beginDrag</span></span>

<span data-ttu-id="ff1b1-438">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-438">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="ff1b1-439">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ff1b1-439">Remarks - beginDrag</span></span>

<span data-ttu-id="ff1b1-440">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-440">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="ff1b1-441">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-441">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-border"></a><span data-ttu-id="ff1b1-442">メソッド border</span><span class="sxs-lookup"><span data-stu-id="ff1b1-442">Method border</span></span>

<span data-ttu-id="ff1b1-443">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-443">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="ff1b1-444">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="ff1b1-444">Parameters - border</span></span>

<span data-ttu-id="ff1b1-445">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-445">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="ff1b1-446">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="ff1b1-446">Return Value - border</span></span>

<span data-ttu-id="ff1b1-447">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-447">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="ff1b1-448">備考 - border</span><span class="sxs-lookup"><span data-stu-id="ff1b1-448">Remarks - border</span></span>

<span data-ttu-id="ff1b1-449">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-449">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="ff1b1-450">値です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-450">Value.</span></span> | <span data-ttu-id="ff1b1-451">説明。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-451">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="ff1b1-452">0</span><span class="sxs-lookup"><span data-stu-id="ff1b1-452">0</span></span>      | <span data-ttu-id="ff1b1-453">自動。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-453">Auto.</span></span>        |
| <span data-ttu-id="ff1b1-454">1</span><span class="sxs-lookup"><span data-stu-id="ff1b1-454">1</span></span>      | <span data-ttu-id="ff1b1-455">3D。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-455">3D.</span></span>          |
| <span data-ttu-id="ff1b1-456">2</span><span class="sxs-lookup"><span data-stu-id="ff1b1-456">2</span></span>      | <span data-ttu-id="ff1b1-457">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-457">Single line.</span></span> |
| <span data-ttu-id="ff1b1-458">3</span><span class="sxs-lookup"><span data-stu-id="ff1b1-458">3</span></span>      | <span data-ttu-id="ff1b1-459">均一。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-459">Flat.</span></span>        |
| <span data-ttu-id="ff1b1-460">4</span><span class="sxs-lookup"><span data-stu-id="ff1b1-460">4</span></span>      | <span data-ttu-id="ff1b1-461">なし。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-461">None.</span></span>        |

## <a name="method-bottommargin"></a><span data-ttu-id="ff1b1-462">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-462">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="ff1b1-463">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-463">Parameters - bottomMargin</span></span>

<span data-ttu-id="ff1b1-464">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-464">value</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="ff1b1-465">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-465">Return Value - bottomMargin</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="ff1b1-466">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ff1b1-466">Method calcControlSize</span></span>

<span data-ttu-id="ff1b1-467">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-467">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="ff1b1-468">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ff1b1-468">Parameters - calcControlSize</span></span>

<span data-ttu-id="ff1b1-469">chars</span><span class="sxs-lookup"><span data-stu-id="ff1b1-469">chars</span></span>  
<span data-ttu-id="ff1b1-470">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-470">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-471">明細行</span><span class="sxs-lookup"><span data-stu-id="ff1b1-471">lines</span></span>  
<span data-ttu-id="ff1b1-472">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-472">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="ff1b1-473">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ff1b1-473">Return Value - calcControlSize</span></span>

<span data-ttu-id="ff1b1-474">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-474">The container that holds the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="ff1b1-475">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-475">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="ff1b1-476">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-476">Parameters - canAddDataField</span></span>

<span data-ttu-id="ff1b1-477">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="ff1b1-477">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-478">fieldId</span><span class="sxs-lookup"><span data-stu-id="ff1b1-478">fieldId</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-479">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ff1b1-479">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="ff1b1-480">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-480">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="ff1b1-481">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="ff1b1-481">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="ff1b1-482">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="ff1b1-482">Parameters - canContain</span></span>

<span data-ttu-id="ff1b1-483">control</span><span class="sxs-lookup"><span data-stu-id="ff1b1-483">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="ff1b1-484">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="ff1b1-484">Return Value - canContain</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="ff1b1-485">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="ff1b1-485">Method colorScheme</span></span>

<span data-ttu-id="ff1b1-486">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-486">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="ff1b1-487">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ff1b1-487">Parameters - colorScheme</span></span>

<span data-ttu-id="ff1b1-488">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-488">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="ff1b1-489">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ff1b1-489">Return Value - colorScheme</span></span>

<span data-ttu-id="ff1b1-490">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-490">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="ff1b1-491">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ff1b1-491">Remarks - colorScheme</span></span>

<span data-ttu-id="ff1b1-492">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-492">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="ff1b1-493">値です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-493">Value.</span></span> | <span data-ttu-id="ff1b1-494">スタイル。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-494">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="ff1b1-495">0</span><span class="sxs-lookup"><span data-stu-id="ff1b1-495">0</span></span>      | <span data-ttu-id="ff1b1-496">既定。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-496">Default.</span></span>                      |
| <span data-ttu-id="ff1b1-497">1</span><span class="sxs-lookup"><span data-stu-id="ff1b1-497">1</span></span>      | <span data-ttu-id="ff1b1-498">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-498">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="ff1b1-499">2</span><span class="sxs-lookup"><span data-stu-id="ff1b1-499">2</span></span>      | <span data-ttu-id="ff1b1-500">真の配色。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-500">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="ff1b1-501">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="ff1b1-501">Method configurationKey</span></span>

<span data-ttu-id="ff1b1-502">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-502">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="ff1b1-503">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ff1b1-503">Parameters - configurationKey</span></span>

<span data-ttu-id="ff1b1-504">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-504">value</span></span>  
<span data-ttu-id="ff1b1-505">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-505">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="ff1b1-506">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ff1b1-506">Return Value - configurationKey</span></span>

<span data-ttu-id="ff1b1-507">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-507">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="ff1b1-508">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ff1b1-508">Remarks - configurationKey</span></span>

<span data-ttu-id="ff1b1-509">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-509">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="ff1b1-510">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-510">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="ff1b1-511">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-511">Method configurationKeyEx</span></span>

<span data-ttu-id="ff1b1-512">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-512">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="ff1b1-513">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-513">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="ff1b1-514">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-514">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="ff1b1-515">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-515">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="ff1b1-516">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-516">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="ff1b1-517">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-517">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="ff1b1-518">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-518">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-contains"></a><span data-ttu-id="ff1b1-519">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="ff1b1-519">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="ff1b1-520">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="ff1b1-520">Parameters - contains</span></span>

<span data-ttu-id="ff1b1-521">control</span><span class="sxs-lookup"><span data-stu-id="ff1b1-521">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="ff1b1-522">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="ff1b1-522">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="ff1b1-523">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="ff1b1-523">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="ff1b1-524">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="ff1b1-524">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="ff1b1-525">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="ff1b1-525">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="ff1b1-526">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="ff1b1-526">Parameters - controlNum</span></span>

<span data-ttu-id="ff1b1-527">controlNo</span><span class="sxs-lookup"><span data-stu-id="ff1b1-527">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="ff1b1-528">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="ff1b1-528">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="ff1b1-529">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ff1b1-529">Method countryRegionCodes</span></span>

<span data-ttu-id="ff1b1-530">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-530">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="ff1b1-531">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ff1b1-531">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="ff1b1-532">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-532">value</span></span>  
<span data-ttu-id="ff1b1-533">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-533">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="ff1b1-534">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ff1b1-534">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="ff1b1-535">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-535">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="ff1b1-536">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-536">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="ff1b1-537">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-537">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="ff1b1-538">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-538">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="ff1b1-539">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-539">Return Value - countryRegionContextField</span></span>

## <a name="method-datagroup"></a><span data-ttu-id="ff1b1-540">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-540">Method dataGroup</span></span>

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a><span data-ttu-id="ff1b1-541">パラメーター - dataGroup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-541">Parameters - dataGroup</span></span>

<span data-ttu-id="ff1b1-542">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-542">value</span></span>  

### <a name="return-value---datagroup"></a><span data-ttu-id="ff1b1-543">戻り値 - dataGroup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-543">Return Value - dataGroup</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="ff1b1-544">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ff1b1-544">Method dataRelationPath</span></span>

<span data-ttu-id="ff1b1-545">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-545">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="ff1b1-546">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ff1b1-546">Parameters - dataRelationPath</span></span>

<span data-ttu-id="ff1b1-547">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-547">value</span></span>  
<span data-ttu-id="ff1b1-548">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-548">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="ff1b1-549">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ff1b1-549">Return Value - dataRelationPath</span></span>

<span data-ttu-id="ff1b1-550">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-550">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="ff1b1-551">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ff1b1-551">Remarks - dataRelationPath</span></span>

<span data-ttu-id="ff1b1-552">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-552">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="ff1b1-553">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-553">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="ff1b1-554">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="ff1b1-554">Method dataSource</span></span>

<span data-ttu-id="ff1b1-555">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-555">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="ff1b1-556">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="ff1b1-556">Parameters - dataSource</span></span>

<span data-ttu-id="ff1b1-557">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-557">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="ff1b1-558">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="ff1b1-558">Return Value - dataSource</span></span>

<span data-ttu-id="ff1b1-559">使用する必要のあるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-559">The identifier of the data source that must be used.</span></span>

## <a name="method-defaultaction"></a><span data-ttu-id="ff1b1-560">メソッド defaultAction</span><span class="sxs-lookup"><span data-stu-id="ff1b1-560">Method defaultAction</span></span>

```xpp
public str defaultAction([str value])
```

### <a name="parameters---defaultaction"></a><span data-ttu-id="ff1b1-561">パラメーター - defaultAction</span><span class="sxs-lookup"><span data-stu-id="ff1b1-561">Parameters - defaultAction</span></span>

<span data-ttu-id="ff1b1-562">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-562">value</span></span>  

### <a name="return-value---defaultaction"></a><span data-ttu-id="ff1b1-563">戻り値 - defaultAction</span><span class="sxs-lookup"><span data-stu-id="ff1b1-563">Return Value - defaultAction</span></span>

## <a name="method-defaultactionlabel"></a><span data-ttu-id="ff1b1-564">メソッド defaultActionLabel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-564">Method defaultActionLabel</span></span>

```xpp
public str defaultActionLabel([str value])
```

### <a name="parameters---defaultactionlabel"></a><span data-ttu-id="ff1b1-565">パラメーター - defaultActionLabel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-565">Parameters - defaultActionLabel</span></span>

<span data-ttu-id="ff1b1-566">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-566">value</span></span>  

### <a name="return-value---defaultactionlabel"></a><span data-ttu-id="ff1b1-567">戻り値 - defaultActionLabel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-567">Return Value - defaultActionLabel</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="ff1b1-568">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="ff1b1-568">Method displayTarget</span></span>

<span data-ttu-id="ff1b1-569">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-569">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="ff1b1-570">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="ff1b1-570">Parameters - displayTarget</span></span>

<span data-ttu-id="ff1b1-571">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-571">value</span></span>  
<span data-ttu-id="ff1b1-572">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-572">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="ff1b1-573">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="ff1b1-573">Return Value - displayTarget</span></span>

<span data-ttu-id="ff1b1-574">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-574">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="ff1b1-575">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="ff1b1-575">Method dragDrop</span></span>

<span data-ttu-id="ff1b1-576">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-576">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="ff1b1-577">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ff1b1-577">Parameters - dragDrop</span></span>

<span data-ttu-id="ff1b1-578">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-578">value</span></span>  
<span data-ttu-id="ff1b1-579">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-579">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="ff1b1-580">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ff1b1-580">Return Value - dragDrop</span></span>

<span data-ttu-id="ff1b1-581">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-581">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="ff1b1-582">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ff1b1-582">Remarks - dragDrop</span></span>

<span data-ttu-id="ff1b1-583">dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-583">Use the dragLeave Method, dragOver Method, and dragOverEx Method methods to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="ff1b1-584">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="ff1b1-584">Method dragOver</span></span>

<span data-ttu-id="ff1b1-585">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-585">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="ff1b1-586">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="ff1b1-586">Parameters - dragOver</span></span>

<span data-ttu-id="ff1b1-587">dragSource</span><span class="sxs-lookup"><span data-stu-id="ff1b1-587">dragSource</span></span>  
<span data-ttu-id="ff1b1-588">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-588">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-589">dragMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-589">dragMode</span></span>  
<span data-ttu-id="ff1b1-590">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-590">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-591">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-591">x</span></span>  
<span data-ttu-id="ff1b1-592">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-592">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-593">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-593">y</span></span>  
<span data-ttu-id="ff1b1-594">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-594">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="ff1b1-595">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="ff1b1-595">Return Value - dragOver</span></span>

<span data-ttu-id="ff1b1-596">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-596">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="ff1b1-597">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-597">Method dragOverEx</span></span>

<span data-ttu-id="ff1b1-598">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-598">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="ff1b1-599">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-599">Parameters - dragOverEx</span></span>

<span data-ttu-id="ff1b1-600">dragSource</span><span class="sxs-lookup"><span data-stu-id="ff1b1-600">dragSource</span></span>  
<span data-ttu-id="ff1b1-601">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-601">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-602">dragMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-602">dragMode</span></span>  
<span data-ttu-id="ff1b1-603">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-603">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-604">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-604">x</span></span>  
<span data-ttu-id="ff1b1-605">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-605">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-606">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-606">y</span></span>  
<span data-ttu-id="ff1b1-607">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-607">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="ff1b1-608">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-608">Return Value - dragOverEx</span></span>

<span data-ttu-id="ff1b1-609">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-609">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="ff1b1-610">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-610">Method dragText</span></span>

<span data-ttu-id="ff1b1-611">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-611">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="ff1b1-612">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-612">Return Value - dragText</span></span>

<span data-ttu-id="ff1b1-613">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-613">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="ff1b1-614">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="ff1b1-614">Method enabled</span></span>

<span data-ttu-id="ff1b1-615">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-615">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="ff1b1-616">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="ff1b1-616">Parameters - enabled</span></span>

<span data-ttu-id="ff1b1-617">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-617">value</span></span>  
<span data-ttu-id="ff1b1-618">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-618">A Boolean value that indicates whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="ff1b1-619">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="ff1b1-619">Return Value - enabled</span></span>

<span data-ttu-id="ff1b1-620">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-620">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="ff1b1-621">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="ff1b1-621">Remarks - enabled</span></span>

<span data-ttu-id="ff1b1-622">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-622">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="ff1b1-623">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-623">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="ff1b1-624">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-624">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-exportallowed"></a><span data-ttu-id="ff1b1-625">メソッド exportAllowed</span><span class="sxs-lookup"><span data-stu-id="ff1b1-625">Method exportAllowed</span></span>

```xpp
public boolean exportAllowed([boolean value])
```

### <a name="parameters---exportallowed"></a><span data-ttu-id="ff1b1-626">パラメーター - exportAllowed</span><span class="sxs-lookup"><span data-stu-id="ff1b1-626">Parameters - exportAllowed</span></span>

<span data-ttu-id="ff1b1-627">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-627">value</span></span>  

### <a name="return-value---exportallowed"></a><span data-ttu-id="ff1b1-628">戻り値 - exportAllowed</span><span class="sxs-lookup"><span data-stu-id="ff1b1-628">Return Value - exportAllowed</span></span>

## <a name="method-exportlabel"></a><span data-ttu-id="ff1b1-629">メソッド exportLabel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-629">Method exportLabel</span></span>

```xpp
public str exportLabel([str value])
```

### <a name="parameters---exportlabel"></a><span data-ttu-id="ff1b1-630">パラメーター - exportLabel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-630">Parameters - exportLabel</span></span>

<span data-ttu-id="ff1b1-631">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-631">value</span></span>  

### <a name="return-value---exportlabel"></a><span data-ttu-id="ff1b1-632">戻り値 - exportLabel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-632">Return Value - exportLabel</span></span>

## <a name="method-getlinedata"></a><span data-ttu-id="ff1b1-633">メソッド getLineData</span><span class="sxs-lookup"><span data-stu-id="ff1b1-633">Method getLineData</span></span>

```xpp
public Struct getLineData(int lineNumber)
```

### <a name="parameters---getlinedata"></a><span data-ttu-id="ff1b1-634">パラメーター - getLineData</span><span class="sxs-lookup"><span data-stu-id="ff1b1-634">Parameters - getLineData</span></span>

<span data-ttu-id="ff1b1-635">lineNumber</span><span class="sxs-lookup"><span data-stu-id="ff1b1-635">lineNumber</span></span>  

### <a name="return-value---getlinedata"></a><span data-ttu-id="ff1b1-636">戻り値 - getLineData</span><span class="sxs-lookup"><span data-stu-id="ff1b1-636">Return Value - getLineData</span></span>

## <a name="method-getselecteddata"></a><span data-ttu-id="ff1b1-637">メソッド getSelectedData</span><span class="sxs-lookup"><span data-stu-id="ff1b1-637">Method getSelectedData</span></span>

```xpp
public Struct getSelectedData()
```

### <a name="return-value---getselecteddata"></a><span data-ttu-id="ff1b1-638">戻り値 - getSelectedData</span><span class="sxs-lookup"><span data-stu-id="ff1b1-638">Return Value - getSelectedData</span></span>

## <a name="method-gridlines"></a><span data-ttu-id="ff1b1-639">メソッド gridLines</span><span class="sxs-lookup"><span data-stu-id="ff1b1-639">Method gridLines</span></span>

```xpp
public boolean gridLines([boolean value])
```

### <a name="parameters---gridlines"></a><span data-ttu-id="ff1b1-640">パラメーター - gridLines</span><span class="sxs-lookup"><span data-stu-id="ff1b1-640">Parameters - gridLines</span></span>

<span data-ttu-id="ff1b1-641">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-641">value</span></span>  

### <a name="return-value---gridlines"></a><span data-ttu-id="ff1b1-642">戻り値 - gridLines</span><span class="sxs-lookup"><span data-stu-id="ff1b1-642">Return Value - gridLines</span></span>

## <a name="method-gridlinesstyle"></a><span data-ttu-id="ff1b1-643">メソッド gridLinesStyle</span><span class="sxs-lookup"><span data-stu-id="ff1b1-643">Method gridLinesStyle</span></span>

```xpp
public int gridLinesStyle([int value])
```

### <a name="parameters---gridlinesstyle"></a><span data-ttu-id="ff1b1-644">パラメーター - gridLinesStyle</span><span class="sxs-lookup"><span data-stu-id="ff1b1-644">Parameters - gridLinesStyle</span></span>

<span data-ttu-id="ff1b1-645">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-645">value</span></span>  

### <a name="return-value---gridlinesstyle"></a><span data-ttu-id="ff1b1-646">戻り値 - gridLinesStyle</span><span class="sxs-lookup"><span data-stu-id="ff1b1-646">Return Value - gridLinesStyle</span></span>

## <a name="method-groupby"></a><span data-ttu-id="ff1b1-647">メソッド groupBy</span><span class="sxs-lookup"><span data-stu-id="ff1b1-647">Method groupBy</span></span>

```xpp
public str groupBy([str value])
```

### <a name="parameters---groupby"></a><span data-ttu-id="ff1b1-648">パラメーター - groupBy</span><span class="sxs-lookup"><span data-stu-id="ff1b1-648">Parameters - groupBy</span></span>

<span data-ttu-id="ff1b1-649">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-649">value</span></span>  

### <a name="return-value---groupby"></a><span data-ttu-id="ff1b1-650">戻り値 - groupBy</span><span class="sxs-lookup"><span data-stu-id="ff1b1-650">Return Value - groupBy</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="ff1b1-651">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="ff1b1-651">Method hasChanged</span></span>

<span data-ttu-id="ff1b1-652">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-652">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="ff1b1-653">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="ff1b1-653">Parameters - hasChanged</span></span>

<span data-ttu-id="ff1b1-654">val</span><span class="sxs-lookup"><span data-stu-id="ff1b1-654">val</span></span>  
<span data-ttu-id="ff1b1-655">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-655">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="ff1b1-656">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="ff1b1-656">Return Value - hasChanged</span></span>

<span data-ttu-id="ff1b1-657">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-657">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="ff1b1-658">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="ff1b1-658">Method hasUserSetting</span></span>

<span data-ttu-id="ff1b1-659">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-659">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="ff1b1-660">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="ff1b1-660">Return Value - hasUserSetting</span></span>

<span data-ttu-id="ff1b1-661">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-661">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="ff1b1-662">メソッド height</span><span class="sxs-lookup"><span data-stu-id="ff1b1-662">Method height</span></span>

<span data-ttu-id="ff1b1-663">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-663">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="ff1b1-664">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="ff1b1-664">Parameters - height</span></span>

<span data-ttu-id="ff1b1-665">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-665">value</span></span>  
<span data-ttu-id="ff1b1-666">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-666">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-667">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-667">mode</span></span>  
<span data-ttu-id="ff1b1-668">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-668">An integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="ff1b1-669">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="ff1b1-669">Return Value - height</span></span>

<span data-ttu-id="ff1b1-670">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-670">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="ff1b1-671">備考 - height</span><span class="sxs-lookup"><span data-stu-id="ff1b1-671">Remarks - height</span></span>

<span data-ttu-id="ff1b1-672">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-672">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="ff1b1-673">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="ff1b1-673">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="ff1b1-674">モード。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-674">Mode.</span></span>            | <span data-ttu-id="ff1b1-675">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-675">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b1-676">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-676">-1 Exact.</span></span>        | <span data-ttu-id="ff1b1-677">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-677">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ff1b1-678">0 自動。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-678">0 Auto.</span></span>          | <span data-ttu-id="ff1b1-679">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-679">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ff1b1-680">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-680">1 Column height.</span></span> | <span data-ttu-id="ff1b1-681">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-681">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="ff1b1-682">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-682">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="ff1b1-683">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-683">Method heightMode</span></span>

<span data-ttu-id="ff1b1-684">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-684">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="ff1b1-685">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-685">Parameters - heightMode</span></span>

<span data-ttu-id="ff1b1-686">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-686">value</span></span>  
<span data-ttu-id="ff1b1-687">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-687">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="ff1b1-688">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-688">Return Value - heightMode</span></span>

<span data-ttu-id="ff1b1-689">計算モード。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-689">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="ff1b1-690">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-690">Remarks - heightMode</span></span>

<span data-ttu-id="ff1b1-691">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="ff1b1-691">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="ff1b1-692">モード。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-692">Mode.</span></span>          | <span data-ttu-id="ff1b1-693">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-693">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b1-694">正確。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-694">Exact.</span></span>         | <span data-ttu-id="ff1b1-695">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-695">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ff1b1-696">自動。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-696">Auto.</span></span>          | <span data-ttu-id="ff1b1-697">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-697">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ff1b1-698">列の高さ</span><span class="sxs-lookup"><span data-stu-id="ff1b1-698">Column height.</span></span> | <span data-ttu-id="ff1b1-699">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-699">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="ff1b1-700">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-700">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="ff1b1-701">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-701">Method heightValue</span></span>

<span data-ttu-id="ff1b1-702">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-702">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="ff1b1-703">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-703">Parameters - heightValue</span></span>

<span data-ttu-id="ff1b1-704">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-704">value</span></span>  
<span data-ttu-id="ff1b1-705">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-705">An Integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="ff1b1-706">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-706">Return Value - heightValue</span></span>

<span data-ttu-id="ff1b1-707">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-707">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="ff1b1-708">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-708">Remarks - heightValue</span></span>

<span data-ttu-id="ff1b1-709">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-709">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="ff1b1-710">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-710">Method helpField</span></span>

<span data-ttu-id="ff1b1-711">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-711">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="ff1b1-712">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-712">Return Value - helpField</span></span>

<span data-ttu-id="ff1b1-713">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-713">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="ff1b1-714">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="ff1b1-714">Remarks - helpField</span></span>

<span data-ttu-id="ff1b1-715">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-715">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="ff1b1-716">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-716">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="ff1b1-717">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-717">Method helpText</span></span>

<span data-ttu-id="ff1b1-718">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-718">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="ff1b1-719">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-719">Parameters - helpText</span></span>

<span data-ttu-id="ff1b1-720">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-720">value</span></span>  
<span data-ttu-id="ff1b1-721">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-721">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="ff1b1-722">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-722">Return Value - helpText</span></span>

<span data-ttu-id="ff1b1-723">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-723">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="ff1b1-724">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-724">Remarks - helpText</span></span>

<span data-ttu-id="ff1b1-725">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-725">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="ff1b1-726">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-726">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="ff1b1-727">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ff1b1-727">Method hierarchyParent</span></span>

<span data-ttu-id="ff1b1-728">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-728">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="ff1b1-729">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ff1b1-729">Parameters - hierarchyParent</span></span>

<span data-ttu-id="ff1b1-730">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-730">value</span></span>  
<span data-ttu-id="ff1b1-731">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-731">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="ff1b1-732">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ff1b1-732">Return Value - hierarchyParent</span></span>

<span data-ttu-id="ff1b1-733">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-733">The HierarchyParent property value of the control.</span></span>

## <a name="method-highlightactive"></a><span data-ttu-id="ff1b1-734">メソッド highlightActive</span><span class="sxs-lookup"><span data-stu-id="ff1b1-734">Method highlightActive</span></span>

```xpp
public boolean highlightActive([boolean value])
```

### <a name="parameters---highlightactive"></a><span data-ttu-id="ff1b1-735">パラメーター - highlightActive</span><span class="sxs-lookup"><span data-stu-id="ff1b1-735">Parameters - highlightActive</span></span>

<span data-ttu-id="ff1b1-736">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-736">value</span></span>  

### <a name="return-value---highlightactive"></a><span data-ttu-id="ff1b1-737">戻り値 - highlightActive</span><span class="sxs-lookup"><span data-stu-id="ff1b1-737">Return Value - highlightActive</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="ff1b1-738">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="ff1b1-738">Method hWnd</span></span>

<span data-ttu-id="ff1b1-739">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-739">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="ff1b1-740">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="ff1b1-740">Return Value - hWnd</span></span>

<span data-ttu-id="ff1b1-741">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-741">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="ff1b1-742">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="ff1b1-742">Remarks - hWnd</span></span>

<span data-ttu-id="ff1b1-743">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-743">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="ff1b1-744">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="ff1b1-744">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="ff1b1-745">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="ff1b1-745">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="ff1b1-746">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ff1b1-746">Method isDisplayed</span></span>

<span data-ttu-id="ff1b1-747">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-747">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="ff1b1-748">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ff1b1-748">Return Value - isDisplayed</span></span>

<span data-ttu-id="ff1b1-749">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-749">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="ff1b1-750">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ff1b1-750">Remarks - isDisplayed</span></span>

<span data-ttu-id="ff1b1-751">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-751">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="ff1b1-752">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="ff1b1-752">Method isRestricted</span></span>

<span data-ttu-id="ff1b1-753">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-753">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="ff1b1-754">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="ff1b1-754">Return Value - isRestricted</span></span>

<span data-ttu-id="ff1b1-755">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-755">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="ff1b1-756">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ff1b1-756">Method isUserSetupEnabled</span></span>

<span data-ttu-id="ff1b1-757">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-757">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="ff1b1-758">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ff1b1-758">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="ff1b1-759">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="ff1b1-759">neededSetupRights</span></span>  
<span data-ttu-id="ff1b1-760">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-760">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="ff1b1-761">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ff1b1-761">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="ff1b1-762">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-762">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="ff1b1-763">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-763">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="ff1b1-764">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ff1b1-764">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="ff1b1-765">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-765">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b1-766">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="ff1b1-766">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="ff1b1-767">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-767">No changes can be made to the control.</span></span> <span data-ttu-id="ff1b1-768">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-768">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="ff1b1-769">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="ff1b1-769">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="ff1b1-770">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-770">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="ff1b1-771">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-771">The user cannot move the control.</span></span>   |
| <span data-ttu-id="ff1b1-772">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="ff1b1-772">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="ff1b1-773">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-773">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="ff1b1-774">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-774">The user can also move the control.</span></span> |

## <a name="method-leave"></a><span data-ttu-id="ff1b1-775">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="ff1b1-775">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="ff1b1-776">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="ff1b1-776">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="ff1b1-777">メソッド left</span><span class="sxs-lookup"><span data-stu-id="ff1b1-777">Method left</span></span>

<span data-ttu-id="ff1b1-778">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-778">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="ff1b1-779">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="ff1b1-779">Parameters - left</span></span>

<span data-ttu-id="ff1b1-780">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-780">value</span></span>  
<span data-ttu-id="ff1b1-781">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-781">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-782">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-782">mode</span></span>  
<span data-ttu-id="ff1b1-783">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-783">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="ff1b1-784">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="ff1b1-784">Return Value - left</span></span>

<span data-ttu-id="ff1b1-785">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-785">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="ff1b1-786">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-786">Method leftMargin</span></span>

```xpp
public int leftMargin([int value])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="ff1b1-787">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-787">Parameters - leftMargin</span></span>

<span data-ttu-id="ff1b1-788">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-788">value</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="ff1b1-789">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-789">Return Value - leftMargin</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="ff1b1-790">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-790">Method leftMode</span></span>

<span data-ttu-id="ff1b1-791">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-791">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="ff1b1-792">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-792">Parameters - leftMode</span></span>

<span data-ttu-id="ff1b1-793">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-793">value</span></span>  
<span data-ttu-id="ff1b1-794">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-794">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="ff1b1-795">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-795">Return Value - leftMode</span></span>

<span data-ttu-id="ff1b1-796">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-796">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="ff1b1-797">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-797">Method leftValue</span></span>

<span data-ttu-id="ff1b1-798">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-798">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="ff1b1-799">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-799">Parameters - leftValue</span></span>

<span data-ttu-id="ff1b1-800">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-800">value</span></span>  
<span data-ttu-id="ff1b1-801">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-801">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="ff1b1-802">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-802">Return Value - leftValue</span></span>

<span data-ttu-id="ff1b1-803">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-803">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="ff1b1-804">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ff1b1-804">Method markAsUserAdd</span></span>

<span data-ttu-id="ff1b1-805">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-805">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="ff1b1-806">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ff1b1-806">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="ff1b1-807">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-807">value</span></span>  
<span data-ttu-id="ff1b1-808">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-808">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="ff1b1-809">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ff1b1-809">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="ff1b1-810">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-810">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-morerowsindicator"></a><span data-ttu-id="ff1b1-811">メソッド moreRowsIndicator</span><span class="sxs-lookup"><span data-stu-id="ff1b1-811">Method moreRowsIndicator</span></span>

```xpp
public int moreRowsIndicator([int value])
```

### <a name="parameters---morerowsindicator"></a><span data-ttu-id="ff1b1-812">パラメーター - moreRowsIndicator</span><span class="sxs-lookup"><span data-stu-id="ff1b1-812">Parameters - moreRowsIndicator</span></span>

<span data-ttu-id="ff1b1-813">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-813">value</span></span>  

### <a name="return-value---morerowsindicator"></a><span data-ttu-id="ff1b1-814">戻り値 - moreRowsIndicator</span><span class="sxs-lookup"><span data-stu-id="ff1b1-814">Return Value - moreRowsIndicator</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="ff1b1-815">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ff1b1-815">Method mouseDblClick</span></span>

<span data-ttu-id="ff1b1-816">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-816">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="ff1b1-817">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ff1b1-817">Parameters - mouseDblClick</span></span>

<span data-ttu-id="ff1b1-818">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-818">x</span></span>  
<span data-ttu-id="ff1b1-819">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-819">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-820">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-820">y</span></span>  
<span data-ttu-id="ff1b1-821">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-821">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-822">ボタン</span><span class="sxs-lookup"><span data-stu-id="ff1b1-822">button</span></span>  
<span data-ttu-id="ff1b1-823">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-823">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-824">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-824">Ctrl</span></span>  
<span data-ttu-id="ff1b1-825">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-825">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-826">シフト</span><span class="sxs-lookup"><span data-stu-id="ff1b1-826">Shift</span></span>  
<span data-ttu-id="ff1b1-827">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-827">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="ff1b1-828">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ff1b1-828">Return Value - mouseDblClick</span></span>

<span data-ttu-id="ff1b1-829">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-829">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="ff1b1-830">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ff1b1-830">Remarks - mouseDblClick</span></span>

<span data-ttu-id="ff1b1-831">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-831">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="ff1b1-832">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="ff1b1-832">Method mouseDown</span></span>

<span data-ttu-id="ff1b1-833">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-833">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="ff1b1-834">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ff1b1-834">Parameters - mouseDown</span></span>

<span data-ttu-id="ff1b1-835">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-835">x</span></span>  
<span data-ttu-id="ff1b1-836">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-836">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-837">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-837">y</span></span>  
<span data-ttu-id="ff1b1-838">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-838">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-839">ボタン</span><span class="sxs-lookup"><span data-stu-id="ff1b1-839">button</span></span>  
<span data-ttu-id="ff1b1-840">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-840">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-841">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-841">Ctrl</span></span>  
<span data-ttu-id="ff1b1-842">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-842">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-843">シフト</span><span class="sxs-lookup"><span data-stu-id="ff1b1-843">Shift</span></span>  
<span data-ttu-id="ff1b1-844">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-844">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="ff1b1-845">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ff1b1-845">Return Value - mouseDown</span></span>

<span data-ttu-id="ff1b1-846">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-846">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="ff1b1-847">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ff1b1-847">Remarks - mouseDown</span></span>

<span data-ttu-id="ff1b1-848">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-848">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="ff1b1-849">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-849">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="ff1b1-850">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="ff1b1-850">Method mouseMove</span></span>

<span data-ttu-id="ff1b1-851">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-851">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="ff1b1-852">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ff1b1-852">Parameters - mouseMove</span></span>

<span data-ttu-id="ff1b1-853">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-853">x</span></span>  
<span data-ttu-id="ff1b1-854">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-854">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-855">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-855">y</span></span>  
<span data-ttu-id="ff1b1-856">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-856">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-857">ボタン</span><span class="sxs-lookup"><span data-stu-id="ff1b1-857">button</span></span>  
<span data-ttu-id="ff1b1-858">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-858">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-859">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-859">Ctrl</span></span>  
<span data-ttu-id="ff1b1-860">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-860">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-861">シフト</span><span class="sxs-lookup"><span data-stu-id="ff1b1-861">Shift</span></span>  
<span data-ttu-id="ff1b1-862">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-862">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="ff1b1-863">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ff1b1-863">Return Value - mouseMove</span></span>

<span data-ttu-id="ff1b1-864">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-864">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="ff1b1-865">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ff1b1-865">Remarks - mouseMove</span></span>

<span data-ttu-id="ff1b1-866">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-866">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="ff1b1-867">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="ff1b1-867">Method mouseUp</span></span>

<span data-ttu-id="ff1b1-868">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-868">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="ff1b1-869">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ff1b1-869">Parameters - mouseUp</span></span>

<span data-ttu-id="ff1b1-870">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-870">x</span></span>  
<span data-ttu-id="ff1b1-871">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-871">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-872">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-872">y</span></span>  
<span data-ttu-id="ff1b1-873">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-873">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-874">ボタン</span><span class="sxs-lookup"><span data-stu-id="ff1b1-874">button</span></span>  
<span data-ttu-id="ff1b1-875">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-875">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-876">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-876">Ctrl</span></span>  
<span data-ttu-id="ff1b1-877">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-877">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-878">シフト</span><span class="sxs-lookup"><span data-stu-id="ff1b1-878">Shift</span></span>  
<span data-ttu-id="ff1b1-879">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-879">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="ff1b1-880">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ff1b1-880">Return Value - mouseUp</span></span>

<span data-ttu-id="ff1b1-881">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-881">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="ff1b1-882">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ff1b1-882">Remarks - mouseUp</span></span>

<span data-ttu-id="ff1b1-883">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-883">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="ff1b1-884">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-884">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="ff1b1-885">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-885">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="ff1b1-886">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-886">Parameters - moveControl</span></span>

<span data-ttu-id="ff1b1-887">controlId</span><span class="sxs-lookup"><span data-stu-id="ff1b1-887">controlId</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-888">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="ff1b1-888">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="ff1b1-889">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-889">Return Value - moveControl</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="ff1b1-890">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="ff1b1-890">Method multiSelect</span></span>

```xpp
public boolean multiSelect([boolean value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="ff1b1-891">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="ff1b1-891">Parameters - multiSelect</span></span>

<span data-ttu-id="ff1b1-892">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-892">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="ff1b1-893">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="ff1b1-893">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="ff1b1-894">メソッド名</span><span class="sxs-lookup"><span data-stu-id="ff1b1-894">Method name</span></span>

<span data-ttu-id="ff1b1-895">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-895">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="ff1b1-896">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="ff1b1-896">Parameters - name</span></span>

<span data-ttu-id="ff1b1-897">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-897">value</span></span>  
<span data-ttu-id="ff1b1-898">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-898">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="ff1b1-899">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="ff1b1-899">Return Value - name</span></span>

<span data-ttu-id="ff1b1-900">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-900">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="ff1b1-901">備考 - name</span><span class="sxs-lookup"><span data-stu-id="ff1b1-901">Remarks - name</span></span>

<span data-ttu-id="ff1b1-902">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-902">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="ff1b1-903">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-903">It must begin with a letter.</span></span>
-   <span data-ttu-id="ff1b1-904">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-904">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="ff1b1-905">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-905">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="ff1b1-906">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-906">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="ff1b1-907">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-907">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="ff1b1-908">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="ff1b1-908">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="ff1b1-909">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="ff1b1-909">Parameters - neededPermission</span></span>

<span data-ttu-id="ff1b1-910">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-910">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="ff1b1-911">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="ff1b1-911">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="ff1b1-912">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ff1b1-912">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="ff1b1-913">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ff1b1-913">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="ff1b1-914">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-914">Method parentControl</span></span>

<span data-ttu-id="ff1b1-915">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-915">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="ff1b1-916">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-916">Return Value - parentControl</span></span>

<span data-ttu-id="ff1b1-917">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-917">The parent control for the control.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="ff1b1-918">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-918">Method rightMargin</span></span>

```xpp
public int rightMargin([int value])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="ff1b1-919">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-919">Parameters - rightMargin</span></span>

<span data-ttu-id="ff1b1-920">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-920">value</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="ff1b1-921">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-921">Return Value - rightMargin</span></span>

## <a name="method-scrollbars"></a><span data-ttu-id="ff1b1-922">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="ff1b1-922">Method scrollbars</span></span>

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a><span data-ttu-id="ff1b1-923">パラメーター - scrollbars</span><span class="sxs-lookup"><span data-stu-id="ff1b1-923">Parameters - scrollbars</span></span>

<span data-ttu-id="ff1b1-924">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-924">value</span></span>  

### <a name="return-value---scrollbars"></a><span data-ttu-id="ff1b1-925">戻り値 - scrollbars</span><span class="sxs-lookup"><span data-stu-id="ff1b1-925">Return Value - scrollbars</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="ff1b1-926">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="ff1b1-926">Method securityKey</span></span>

<span data-ttu-id="ff1b1-927">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-927">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="ff1b1-928">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="ff1b1-928">Parameters - securityKey</span></span>

<span data-ttu-id="ff1b1-929">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-929">value</span></span>  
<span data-ttu-id="ff1b1-930">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-930">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="ff1b1-931">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="ff1b1-931">Return Value - securityKey</span></span>

<span data-ttu-id="ff1b1-932">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-932">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcollabels"></a><span data-ttu-id="ff1b1-933">メソッド showColLabels</span><span class="sxs-lookup"><span data-stu-id="ff1b1-933">Method showColLabels</span></span>

```xpp
public boolean showColLabels([boolean value])
```

### <a name="parameters---showcollabels"></a><span data-ttu-id="ff1b1-934">パラメーター - showColLabels</span><span class="sxs-lookup"><span data-stu-id="ff1b1-934">Parameters - showColLabels</span></span>

<span data-ttu-id="ff1b1-935">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-935">value</span></span>  

### <a name="return-value---showcollabels"></a><span data-ttu-id="ff1b1-936">戻り値 - showColLabels</span><span class="sxs-lookup"><span data-stu-id="ff1b1-936">Return Value - showColLabels</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="ff1b1-937">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ff1b1-937">Method showContextMenu</span></span>

<span data-ttu-id="ff1b1-938">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-938">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="ff1b1-939">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ff1b1-939">Parameters - showContextMenu</span></span>

<span data-ttu-id="ff1b1-940">menuHandle</span><span class="sxs-lookup"><span data-stu-id="ff1b1-940">menuHandle</span></span>  
<span data-ttu-id="ff1b1-941">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-941">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="ff1b1-942">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ff1b1-942">Return Value - showContextMenu</span></span>

<span data-ttu-id="ff1b1-943">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-943">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showrowlabels"></a><span data-ttu-id="ff1b1-944">メソッド showRowLabels</span><span class="sxs-lookup"><span data-stu-id="ff1b1-944">Method showRowLabels</span></span>

```xpp
public boolean showRowLabels([boolean value])
```

### <a name="parameters---showrowlabels"></a><span data-ttu-id="ff1b1-945">パラメーター - showRowLabels</span><span class="sxs-lookup"><span data-stu-id="ff1b1-945">Parameters - showRowLabels</span></span>

<span data-ttu-id="ff1b1-946">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-946">value</span></span>  

### <a name="return-value---showrowlabels"></a><span data-ttu-id="ff1b1-947">戻り値 - showRowLabels</span><span class="sxs-lookup"><span data-stu-id="ff1b1-947">Return Value - showRowLabels</span></span>

## <a name="method-skip"></a><span data-ttu-id="ff1b1-948">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-948">Method skip</span></span>

<span data-ttu-id="ff1b1-949">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-949">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="ff1b1-950">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-950">Parameters - skip</span></span>

<span data-ttu-id="ff1b1-951">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-951">value</span></span>  
<span data-ttu-id="ff1b1-952">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-952">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="ff1b1-953">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-953">Return Value - skip</span></span>

<span data-ttu-id="ff1b1-954">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-954">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="ff1b1-955">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="ff1b1-955">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="ff1b1-956">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="ff1b1-956">Parameters - sort</span></span>

<span data-ttu-id="ff1b1-957">sortDirection</span><span class="sxs-lookup"><span data-stu-id="ff1b1-957">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="ff1b1-958">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="ff1b1-958">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="ff1b1-959">メソッド style</span><span class="sxs-lookup"><span data-stu-id="ff1b1-959">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="ff1b1-960">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="ff1b1-960">Parameters - style</span></span>

<span data-ttu-id="ff1b1-961">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-961">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="ff1b1-962">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="ff1b1-962">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="ff1b1-963">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-963">Method toolTip</span></span>

<span data-ttu-id="ff1b1-964">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-964">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="ff1b1-965">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-965">Return Value - toolTip</span></span>

<span data-ttu-id="ff1b1-966">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-966">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="ff1b1-967">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-967">Remarks - toolTip</span></span>

<span data-ttu-id="ff1b1-968">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-968">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="ff1b1-969">メソッド top</span><span class="sxs-lookup"><span data-stu-id="ff1b1-969">Method top</span></span>

<span data-ttu-id="ff1b1-970">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-970">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="ff1b1-971">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="ff1b1-971">Parameters - top</span></span>

<span data-ttu-id="ff1b1-972">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-972">value</span></span>  
<span data-ttu-id="ff1b1-973">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-973">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-974">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-974">mode</span></span>  
<span data-ttu-id="ff1b1-975">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-975">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="ff1b1-976">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="ff1b1-976">Return Value - top</span></span>

<span data-ttu-id="ff1b1-977">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-977">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="ff1b1-978">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-978">Method topMargin</span></span>

```xpp
public int topMargin([int value])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="ff1b1-979">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-979">Parameters - topMargin</span></span>

<span data-ttu-id="ff1b1-980">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-980">value</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="ff1b1-981">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="ff1b1-981">Return Value - topMargin</span></span>

## <a name="method-topmode"></a><span data-ttu-id="ff1b1-982">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-982">Method topMode</span></span>

<span data-ttu-id="ff1b1-983">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-983">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="ff1b1-984">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-984">Parameters - topMode</span></span>

<span data-ttu-id="ff1b1-985">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-985">value</span></span>  
<span data-ttu-id="ff1b1-986">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-986">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="ff1b1-987">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-987">Return Value - topMode</span></span>

<span data-ttu-id="ff1b1-988">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-988">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="ff1b1-989">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-989">Method topValue</span></span>

<span data-ttu-id="ff1b1-990">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-990">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="ff1b1-991">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-991">Parameters - topValue</span></span>

<span data-ttu-id="ff1b1-992">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-992">value</span></span>  
<span data-ttu-id="ff1b1-993">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-993">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="ff1b1-994">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-994">Return Value - topValue</span></span>

<span data-ttu-id="ff1b1-995">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-995">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="ff1b1-996">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="ff1b1-996">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="ff1b1-997">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="ff1b1-997">Parameters - type</span></span>

<span data-ttu-id="ff1b1-998">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-998">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="ff1b1-999">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="ff1b1-999">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="ff1b1-1000">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1000">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="ff1b1-1001">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1001">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="ff1b1-1002">データ</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1002">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="ff1b1-1003">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1003">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="ff1b1-1004">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1004">Method userData</span></span>

<span data-ttu-id="ff1b1-1005">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1005">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="ff1b1-1006">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1006">Parameters - userData</span></span>

<span data-ttu-id="ff1b1-1007">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1007">value</span></span>  
<span data-ttu-id="ff1b1-1008">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1008">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="ff1b1-1009">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1009">Return Value - userData</span></span>

<span data-ttu-id="ff1b1-1010">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1010">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="ff1b1-1011">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1011">Method userDataItem</span></span>

<span data-ttu-id="ff1b1-1012">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1012">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="ff1b1-1013">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1013">Parameters - userDataItem</span></span>

<span data-ttu-id="ff1b1-1014">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1014">value</span></span>  
<span data-ttu-id="ff1b1-1015">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1015">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="ff1b1-1016">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1016">Return Value - userDataItem</span></span>

<span data-ttu-id="ff1b1-1017">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1017">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="ff1b1-1018">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1018">Method userDataItems</span></span>

<span data-ttu-id="ff1b1-1019">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1019">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="ff1b1-1020">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1020">Parameters - userDataItems</span></span>

<span data-ttu-id="ff1b1-1021">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1021">value</span></span>  
<span data-ttu-id="ff1b1-1022">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1022">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="ff1b1-1023">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1023">Return Value - userDataItems</span></span>

<span data-ttu-id="ff1b1-1024">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1024">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="ff1b1-1025">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1025">Method userDisable</span></span>

<span data-ttu-id="ff1b1-1026">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1026">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="ff1b1-1027">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1027">Parameters - userDisable</span></span>

<span data-ttu-id="ff1b1-1028">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1028">value</span></span>  
<span data-ttu-id="ff1b1-1029">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1029">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="ff1b1-1030">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1030">Return Value - userDisable</span></span>

<span data-ttu-id="ff1b1-1031">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1031">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="ff1b1-1032">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1032">Method userHeight</span></span>

<span data-ttu-id="ff1b1-1033">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1033">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="ff1b1-1034">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1034">Parameters - userHeight</span></span>

<span data-ttu-id="ff1b1-1035">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1035">value</span></span>  
<span data-ttu-id="ff1b1-1036">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1036">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="ff1b1-1037">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1037">Return Value - userHeight</span></span>

<span data-ttu-id="ff1b1-1038">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1038">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="ff1b1-1039">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1039">Method userHide</span></span>

<span data-ttu-id="ff1b1-1040">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1040">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="ff1b1-1041">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1041">Parameters - userHide</span></span>

<span data-ttu-id="ff1b1-1042">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1042">value</span></span>  
<span data-ttu-id="ff1b1-1043">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1043">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="ff1b1-1044">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1044">Return Value - userHide</span></span>

<span data-ttu-id="ff1b1-1045">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1045">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="ff1b1-1046">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1046">Remarks - userHide</span></span>

<span data-ttu-id="ff1b1-1047">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1047">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="ff1b1-1048">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1048">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="ff1b1-1049">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1049">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="ff1b1-1050">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1050">Method userOrgContainer</span></span>

<span data-ttu-id="ff1b1-1051">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1051">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="ff1b1-1052">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1052">Parameters - userOrgContainer</span></span>

<span data-ttu-id="ff1b1-1053">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1053">value</span></span>  
<span data-ttu-id="ff1b1-1054">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1054">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="ff1b1-1055">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1055">Return Value - userOrgContainer</span></span>

<span data-ttu-id="ff1b1-1056">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1056">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="ff1b1-1057">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1057">Method userOrgSibling</span></span>

<span data-ttu-id="ff1b1-1058">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1058">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="ff1b1-1059">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1059">Parameters - userOrgSibling</span></span>

<span data-ttu-id="ff1b1-1060">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1060">value</span></span>  
<span data-ttu-id="ff1b1-1061">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1061">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="ff1b1-1062">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1062">Return Value - userOrgSibling</span></span>

<span data-ttu-id="ff1b1-1063">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1063">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="ff1b1-1064">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1064">Method userPromptText</span></span>

<span data-ttu-id="ff1b1-1065">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1065">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="ff1b1-1066">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1066">Parameters - userPromptText</span></span>

<span data-ttu-id="ff1b1-1067">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1067">value</span></span>  
<span data-ttu-id="ff1b1-1068">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1068">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="ff1b1-1069">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1069">Return Value - userPromptText</span></span>

<span data-ttu-id="ff1b1-1070">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1070">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="ff1b1-1071">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1071">Method userSecurityLevel</span></span>

<span data-ttu-id="ff1b1-1072">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1072">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="ff1b1-1073">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1073">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="ff1b1-1074">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1074">value</span></span>  
<span data-ttu-id="ff1b1-1075">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1075">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="ff1b1-1076">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1076">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="ff1b1-1077">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1077">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="ff1b1-1078">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1078">Method userSkip</span></span>

<span data-ttu-id="ff1b1-1079">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1079">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="ff1b1-1080">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1080">Parameters - userSkip</span></span>

<span data-ttu-id="ff1b1-1081">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1081">value</span></span>  
<span data-ttu-id="ff1b1-1082">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1082">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="ff1b1-1083">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1083">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="ff1b1-1084">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1084">Return Value - userSkip</span></span>

<span data-ttu-id="ff1b1-1085">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1085">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="ff1b1-1086">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1086">Method userWidth</span></span>

<span data-ttu-id="ff1b1-1087">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1087">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="ff1b1-1088">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1088">Parameters - userWidth</span></span>

<span data-ttu-id="ff1b1-1089">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1089">value</span></span>  
<span data-ttu-id="ff1b1-1090">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1090">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="ff1b1-1091">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1091">Return Value - userWidth</span></span>

<span data-ttu-id="ff1b1-1092">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1092">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="ff1b1-1093">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1093">Remarks - userWidth</span></span>

<span data-ttu-id="ff1b1-1094">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1094">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="ff1b1-1095">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1095">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="ff1b1-1096">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1096">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="ff1b1-1097">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1097">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="ff1b1-1098">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1098">Parameters - useUserLayout</span></span>

<span data-ttu-id="ff1b1-1099">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1099">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="ff1b1-1100">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1100">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="ff1b1-1101">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1101">Method verticalSpacing</span></span>

<span data-ttu-id="ff1b1-1102">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1102">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="ff1b1-1103">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1103">Parameters - verticalSpacing</span></span>

<span data-ttu-id="ff1b1-1104">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1104">value</span></span>  
<span data-ttu-id="ff1b1-1105">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1105">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1106">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1106">mode</span></span>  
<span data-ttu-id="ff1b1-1107">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1107">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="ff1b1-1108">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1108">Return Value - verticalSpacing</span></span>

<span data-ttu-id="ff1b1-1109">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1109">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="ff1b1-1110">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1110">Method verticalSpacingMode</span></span>

<span data-ttu-id="ff1b1-1111">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1111">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="ff1b1-1112">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1112">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="ff1b1-1113">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1113">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="ff1b1-1114">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1114">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="ff1b1-1115">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1115">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="ff1b1-1116">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1116">Method verticalSpacingValue</span></span>

<span data-ttu-id="ff1b1-1117">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1117">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="ff1b1-1118">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1118">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="ff1b1-1119">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1119">value</span></span>  
<span data-ttu-id="ff1b1-1120">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1120">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="ff1b1-1121">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1121">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="ff1b1-1122">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1122">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="ff1b1-1123">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1123">Method visible</span></span>

<span data-ttu-id="ff1b1-1124">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1124">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="ff1b1-1125">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1125">Parameters - visible</span></span>

<span data-ttu-id="ff1b1-1126">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1126">value</span></span>  
<span data-ttu-id="ff1b1-1127">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1127">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="ff1b1-1128">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1128">Return Value - visible</span></span>

<span data-ttu-id="ff1b1-1129">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1129">true if the control is visible; otherwise, false.</span></span>

## <a name="method-visiblecols"></a><span data-ttu-id="ff1b1-1130">メソッド visibleCols</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1130">Method visibleCols</span></span>

```xpp
public int visibleCols([int value], [AutoMode mode])
```

### <a name="parameters---visiblecols"></a><span data-ttu-id="ff1b1-1131">パラメーター - visibleCols</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1131">Parameters - visibleCols</span></span>

<span data-ttu-id="ff1b1-1132">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1132">value</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1133">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1133">mode</span></span>  

### <a name="return-value---visiblecols"></a><span data-ttu-id="ff1b1-1134">戻り値 - visibleCols</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1134">Return Value - visibleCols</span></span>

## <a name="method-visiblecolsmode"></a><span data-ttu-id="ff1b1-1135">メソッド visibleColsMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1135">Method visibleColsMode</span></span>

```xpp
public AutoMode visibleColsMode([AutoMode mode])
```

### <a name="parameters---visiblecolsmode"></a><span data-ttu-id="ff1b1-1136">パラメーター - visibleColsMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1136">Parameters - visibleColsMode</span></span>

<span data-ttu-id="ff1b1-1137">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1137">mode</span></span>  

### <a name="return-value---visiblecolsmode"></a><span data-ttu-id="ff1b1-1138">戻り値 - visibleColsMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1138">Return Value - visibleColsMode</span></span>

## <a name="method-visiblecolsvalue"></a><span data-ttu-id="ff1b1-1139">メソッド visibleColsValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1139">Method visibleColsValue</span></span>

```xpp
public int visibleColsValue([int value])
```

### <a name="parameters---visiblecolsvalue"></a><span data-ttu-id="ff1b1-1140">パラメーター - visibleColsValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1140">Parameters - visibleColsValue</span></span>

<span data-ttu-id="ff1b1-1141">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1141">value</span></span>  

### <a name="return-value---visiblecolsvalue"></a><span data-ttu-id="ff1b1-1142">戻り値 - visibleColsValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1142">Return Value - visibleColsValue</span></span>

## <a name="method-visiblerows"></a><span data-ttu-id="ff1b1-1143">メソッド visibleRows</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1143">Method visibleRows</span></span>

```xpp
public int visibleRows([int value], [AutoMode mode])
```

### <a name="parameters---visiblerows"></a><span data-ttu-id="ff1b1-1144">パラメーター - visibleRows</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1144">Parameters - visibleRows</span></span>

<span data-ttu-id="ff1b1-1145">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1145">value</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1146">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1146">mode</span></span>  

### <a name="return-value---visiblerows"></a><span data-ttu-id="ff1b1-1147">戻り値 - visibleRows</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1147">Return Value - visibleRows</span></span>

## <a name="method-visiblerowsmode"></a><span data-ttu-id="ff1b1-1148">メソッド visibleRowsMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1148">Method visibleRowsMode</span></span>

```xpp
public AutoMode visibleRowsMode([AutoMode mode])
```

### <a name="parameters---visiblerowsmode"></a><span data-ttu-id="ff1b1-1149">パラメーター - visibleRowsMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1149">Parameters - visibleRowsMode</span></span>

<span data-ttu-id="ff1b1-1150">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1150">mode</span></span>  

### <a name="return-value---visiblerowsmode"></a><span data-ttu-id="ff1b1-1151">戻り値 - visibleRowsMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1151">Return Value - visibleRowsMode</span></span>

## <a name="method-visiblerowsvalue"></a><span data-ttu-id="ff1b1-1152">メソッド visibleRowsValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1152">Method visibleRowsValue</span></span>

```xpp
public int visibleRowsValue([int value])
```

### <a name="parameters---visiblerowsvalue"></a><span data-ttu-id="ff1b1-1153">パラメーター - visibleRowsValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1153">Parameters - visibleRowsValue</span></span>

<span data-ttu-id="ff1b1-1154">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1154">value</span></span>  

### <a name="return-value---visiblerowsvalue"></a><span data-ttu-id="ff1b1-1155">戻り値 - visibleRowsValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1155">Return Value - visibleRowsValue</span></span>

## <a name="method-width"></a><span data-ttu-id="ff1b1-1156">メソッド width</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1156">Method width</span></span>

<span data-ttu-id="ff1b1-1157">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1157">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="ff1b1-1158">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1158">Parameters - width</span></span>

<span data-ttu-id="ff1b1-1159">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1159">value</span></span>  
<span data-ttu-id="ff1b1-1160">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1160">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1161">モード</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1161">mode</span></span>  
<span data-ttu-id="ff1b1-1162">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1162">An Integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="ff1b1-1163">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1163">Return Value - width</span></span>

<span data-ttu-id="ff1b1-1164">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1164">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="ff1b1-1165">備考 - width</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1165">Remarks - width</span></span>

<span data-ttu-id="ff1b1-1166">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1166">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="ff1b1-1167">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1167">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="ff1b1-1168">モード。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1168">Mode.</span></span>           | <span data-ttu-id="ff1b1-1169">幅計算。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1169">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b1-1170">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1170">-1 Exact.</span></span>       | <span data-ttu-id="ff1b1-1171">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1171">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ff1b1-1172">0 自動。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1172">0 Auto.</span></span>         | <span data-ttu-id="ff1b1-1173">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1173">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ff1b1-1174">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1174">1 Column width.</span></span> | <span data-ttu-id="ff1b1-1175">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1175">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="ff1b1-1176">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1176">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="ff1b1-1177">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1177">Method widthMode</span></span>

<span data-ttu-id="ff1b1-1178">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1178">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="ff1b1-1179">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1179">Parameters - widthMode</span></span>

<span data-ttu-id="ff1b1-1180">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1180">value</span></span>  
<span data-ttu-id="ff1b1-1181">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1181">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="ff1b1-1182">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1182">Return Value - widthMode</span></span>

<span data-ttu-id="ff1b1-1183">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1183">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="ff1b1-1184">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1184">Remarks - widthMode</span></span>

<span data-ttu-id="ff1b1-1185">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1185">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="ff1b1-1186">モード。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1186">Mode.</span></span>         | <span data-ttu-id="ff1b1-1187">幅計算。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1187">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b1-1188">正確。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1188">Exact.</span></span>        | <span data-ttu-id="ff1b1-1189">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1189">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ff1b1-1190">自動。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1190">Auto.</span></span>         | <span data-ttu-id="ff1b1-1191">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1191">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ff1b1-1192">列の幅。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1192">Column width.</span></span> | <span data-ttu-id="ff1b1-1193">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1193">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="ff1b1-1194">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1194">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="ff1b1-1195">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1195">Method widthValue</span></span>

<span data-ttu-id="ff1b1-1196">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1196">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="ff1b1-1197">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1197">Parameters - widthValue</span></span>

<span data-ttu-id="ff1b1-1198">値</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1198">value</span></span>  
<span data-ttu-id="ff1b1-1199">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1199">An Integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="ff1b1-1200">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1200">Return Value - widthValue</span></span>

<span data-ttu-id="ff1b1-1201">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1201">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="ff1b1-1202">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1202">Remarks - widthValue</span></span>

<span data-ttu-id="ff1b1-1203">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1203">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-cut"></a><span data-ttu-id="ff1b1-1204">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1204">Method cut</span></span>

<span data-ttu-id="ff1b1-1205">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1205">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-applyquickfilter"></a><span data-ttu-id="ff1b1-1206">メソッド applyQuickFilter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1206">Method applyQuickFilter</span></span>

```xpp
public void applyQuickFilter([int controlId], [str filterValue])
```

### <a name="parameters---applyquickfilter"></a><span data-ttu-id="ff1b1-1207">パラメーター - applyQuickFilter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1207">Parameters - applyQuickFilter</span></span>

<span data-ttu-id="ff1b1-1208">controlId</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1208">controlId</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1209">filterValue</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1209">filterValue</span></span>  

## <a name="method-autosizecolumns"></a><span data-ttu-id="ff1b1-1210">メソッド autoSizeColumns</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1210">Method autoSizeColumns</span></span>

```xpp
public void autoSizeColumns([boolean autoSizeColumns])
```

### <a name="parameters---autosizecolumns"></a><span data-ttu-id="ff1b1-1211">パラメーター - autoSizeColumns</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1211">Parameters - autoSizeColumns</span></span>

<span data-ttu-id="ff1b1-1212">autoSizeColumns</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1212">autoSizeColumns</span></span>  

## <a name="method-drop"></a><span data-ttu-id="ff1b1-1213">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1213">Method drop</span></span>

<span data-ttu-id="ff1b1-1214">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1214">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="ff1b1-1215">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1215">Parameters - drop</span></span>

<span data-ttu-id="ff1b1-1216">dragSource</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1216">dragSource</span></span>  
<span data-ttu-id="ff1b1-1217">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1217">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1218">dragMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1218">dragMode</span></span>  
<span data-ttu-id="ff1b1-1219">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1219">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1220">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1220">x</span></span>  
<span data-ttu-id="ff1b1-1221">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1221">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1222">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1222">y</span></span>  
<span data-ttu-id="ff1b1-1223">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1223">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-context"></a><span data-ttu-id="ff1b1-1224">メソッド context</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1224">Method context</span></span>

<span data-ttu-id="ff1b1-1225">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1225">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-jumpref"></a><span data-ttu-id="ff1b1-1226">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1226">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-onlookup"></a><span data-ttu-id="ff1b1-1227">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1227">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="ff1b1-1228">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1228">Parameters - OnLookup</span></span>

<span data-ttu-id="ff1b1-1229">sender</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1229">sender</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1230">e</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1230">e</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="ff1b1-1231">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1231">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="ff1b1-1232">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1232">Parameters - OnLostFocus</span></span>

<span data-ttu-id="ff1b1-1233">sender</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1233">sender</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1234">e</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1234">e</span></span>  

## <a name="method-registeroverridemethod"></a><span data-ttu-id="ff1b1-1235">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1235">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="ff1b1-1236">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1236">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="ff1b1-1237">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1237">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1238">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1238">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1239">overrideObject</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1239">overrideObject</span></span>  

## <a name="method-copy"></a><span data-ttu-id="ff1b1-1240">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1240">Method copy</span></span>

<span data-ttu-id="ff1b1-1241">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1241">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-enter"></a><span data-ttu-id="ff1b1-1242">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1242">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-mouseenter"></a><span data-ttu-id="ff1b1-1243">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1243">Method mouseEnter</span></span>

<span data-ttu-id="ff1b1-1244">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1244">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="ff1b1-1245">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1245">Parameters - mouseEnter</span></span>

<span data-ttu-id="ff1b1-1246">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1246">x</span></span>  
<span data-ttu-id="ff1b1-1247">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1247">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1248">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1248">y</span></span>  
<span data-ttu-id="ff1b1-1249">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1249">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1250">ボタン</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1250">button</span></span>  
<span data-ttu-id="ff1b1-1251">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1251">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1252">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1252">Ctrl</span></span>  
<span data-ttu-id="ff1b1-1253">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1253">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1254">シフト</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1254">Shift</span></span>  
<span data-ttu-id="ff1b1-1255">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1255">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="ff1b1-1256">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1256">Method displayControl</span></span>

<span data-ttu-id="ff1b1-1257">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1257">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-onleaving"></a><span data-ttu-id="ff1b1-1258">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1258">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="ff1b1-1259">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1259">Parameters - OnLeaving</span></span>

<span data-ttu-id="ff1b1-1260">sender</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1260">sender</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1261">e</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1261">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="ff1b1-1262">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1262">Method paste</span></span>

<span data-ttu-id="ff1b1-1263">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1263">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="ff1b1-1264">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1264">Method resetUserSetting</span></span>

<span data-ttu-id="ff1b1-1265">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1265">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-quickfilterprovider"></a><span data-ttu-id="ff1b1-1266">メソッド quickFilterProvider</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1266">Method quickFilterProvider</span></span>

```xpp
public void quickFilterProvider([GridQuickFilterProvider quickFilterProvider])
```

### <a name="parameters---quickfilterprovider"></a><span data-ttu-id="ff1b1-1267">パラメーター - quickFilterProvider</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1267">Parameters - quickFilterProvider</span></span>

<span data-ttu-id="ff1b1-1268">quickFilterProvider</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1268">quickFilterProvider</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="ff1b1-1269">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1269">Method dropEx</span></span>

<span data-ttu-id="ff1b1-1270">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1270">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="ff1b1-1271">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1271">Parameters - dropEx</span></span>

<span data-ttu-id="ff1b1-1272">dragSource</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1272">dragSource</span></span>  
<span data-ttu-id="ff1b1-1273">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1273">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1274">dragMode</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1274">dragMode</span></span>  
<span data-ttu-id="ff1b1-1275">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1275">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1276">x</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1276">x</span></span>  
<span data-ttu-id="ff1b1-1277">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1277">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1278">y</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1278">y</span></span>  
<span data-ttu-id="ff1b1-1279">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1279">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onenter"></a><span data-ttu-id="ff1b1-1280">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1280">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="ff1b1-1281">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1281">Parameters - OnEnter</span></span>

<span data-ttu-id="ff1b1-1282">sender</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1282">sender</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1283">e</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1283">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="ff1b1-1284">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1284">Method inputSearch</span></span>

<span data-ttu-id="ff1b1-1285">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1285">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="ff1b1-1286">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1286">Parameters - inputSearch</span></span>

<span data-ttu-id="ff1b1-1287">searchStr</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1287">searchStr</span></span>  
<span data-ttu-id="ff1b1-1288">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1288">The string value to use to filter data; optional.</span></span>

## <a name="method-filter"></a><span data-ttu-id="ff1b1-1289">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1289">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="ff1b1-1290">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1290">Parameters - filter</span></span>

<span data-ttu-id="ff1b1-1291">filterStr</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1291">filterStr</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="ff1b1-1292">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1292">Method prefColumnSize</span></span>

<span data-ttu-id="ff1b1-1293">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1293">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="ff1b1-1294">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1294">Parameters - prefColumnSize</span></span>

<span data-ttu-id="ff1b1-1295">width</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1295">width</span></span>  
<span data-ttu-id="ff1b1-1296">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1296">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="ff1b1-1297">height</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1297">height</span></span>  
<span data-ttu-id="ff1b1-1298">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1298">The preferred height of the control.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="ff1b1-1299">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1299">Method dragLeave</span></span>

<span data-ttu-id="ff1b1-1300">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1300">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="ff1b1-1301">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1301">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="ff1b1-1302">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1302">Parameters - OnGotFocus</span></span>

<span data-ttu-id="ff1b1-1303">sender</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1303">sender</span></span>  

<!-- -->

<span data-ttu-id="ff1b1-1304">e</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1304">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="ff1b1-1305">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1305">Method lostFocus</span></span>

<span data-ttu-id="ff1b1-1306">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1306">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-enddrag"></a><span data-ttu-id="ff1b1-1307">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1307">Method endDrag</span></span>

<span data-ttu-id="ff1b1-1308">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1308">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="ff1b1-1309">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1309">Remarks - endDrag</span></span>

<span data-ttu-id="ff1b1-1310">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1310">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="ff1b1-1311">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1311">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-arrange"></a><span data-ttu-id="ff1b1-1312">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1312">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-gotfocus"></a><span data-ttu-id="ff1b1-1313">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1313">Method gotFocus</span></span>

<span data-ttu-id="ff1b1-1314">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1314">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-mouseleave"></a><span data-ttu-id="ff1b1-1315">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1315">Method mouseLeave</span></span>

<span data-ttu-id="ff1b1-1316">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1316">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-setfocus"></a><span data-ttu-id="ff1b1-1317">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1317">Method setFocus</span></span>

<span data-ttu-id="ff1b1-1318">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-1318">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```


